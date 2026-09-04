# Rootless Containers

## What are Rootless Containers?

Rootless containers are containers that run **without requiring root privileges**.

**In simple words:**
Rootless means running containers as a **normal user instead of the root user**.

---

## Root vs Rootless

### Root Containers

Containers are managed by the `root` user.

```bash
sudo podman run nginx
```

### Rootless Containers

Containers are managed by a normal user.

```bash
podman run nginx
```

No `sudo` is required.

---

## Why Use Rootless Containers?

Rootless containers provide better security.

If a container is compromised, the attacker has fewer privileges on the host system.

### Benefits

* Better security
* Reduced privileges
* No need for root access
* Safer container execution
* Useful in shared environments

---

## Rootless Podman

Podman is designed to support rootless containers.

Check the current user:

```bash
whoami
```

Run a container:

```bash
podman run -d --name my-nginx nginx
```

Check the container:

```bash
podman ps
```

---

## Rootless vs Rootful

| Rootless              | Rootful            |
| --------------------- | ------------------ |
| Runs as normal user   | Runs as root       |
| No `sudo` required    | May require `sudo` |
| Better security       | Higher privileges  |
| Limited system access | More system access |

---

## Important Point

Rootless containers do **not** mean the container has no privileges at all.

They mean the container process is not running with root privileges on the host.

---

## Summary

**Rootless Containers = Containers running without root privileges.**

Podman provides strong support for running containers in rootless mode.

### Key Point

**Rootless = Normal User + Container + Reduced Host Privileges**
