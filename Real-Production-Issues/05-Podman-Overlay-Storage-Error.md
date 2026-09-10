# Podman Container Cannot Be Removed – Overlay Storage Error

## Problem

During deployment, `podman compose down` failed to remove a container.

The same issue occurred with multiple frontend applications, so it was **not application-specific**.

---

## Error

```text
Error: cleaning up storage:
removing container root filesystem:
replacing mount point ".../overlay/.../merged":
file exists
```

The error appeared during:

```bash
podman compose down
```

and:

```bash
podman rm
```

---

## Root Cause

The Podman **overlay storage filesystem** was stale, mounted incorrectly, or corrupted.

Podman could stop the container but could not properly clean up its overlay filesystem.

This indicates a **Podman storage/runtime issue**, not an application or code issue.

---

## How to Identify

Look for errors containing:

```text
file exists
removing container root filesystem
replacing mount point
```

especially when running:

```bash
podman rm
podman compose down
```

---

## Solution

### Step 1 – Stop the Container

```bash
podman stop <container_name>
```

### Step 2 – Try Normal Removal

```bash
podman rm -f <container_name>
```

If successful, no further action is required.

### Step 3 – Find the Stale Overlay Directory

If the error continues, check the overlay path shown in the error.

Example:

```text
/u01/containers/storage/overlay/16090ce4...
```

### Step 4 – Remove the Stale Overlay Directory

> **Warning:** Manually deleting Podman storage is a high-risk operation. Confirm the exact stale overlay path before removing anything, especially on production servers.

```bash
rm -rf /u01/containers/storage/overlay/<overlay_id>
```

### Step 5 – Remove the Container Again

```bash
podman rm -f <container_name>
```

### Step 6 – Start the Application

```bash
podman compose up -d
```

---

## Verification

Check the container status:

```bash
podman ps
```

The new container should be running:

```text
Up
```

Also check the logs:

```bash
podman logs -f <container_name>
```

---

## Lesson Learned

* This was **not a code issue**.
* This was **not a Next.js issue**.
* The root cause was a **Podman overlay storage problem**.
* The same issue affected multiple applications, confirming it was an **infrastructure/runtime issue**.
* When `podman rm` or `podman compose down` fails with overlay filesystem errors, investigate **Podman storage** first.
