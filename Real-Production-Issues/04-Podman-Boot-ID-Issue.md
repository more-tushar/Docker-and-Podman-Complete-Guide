# Podman Boot ID Issue

## Problem

Podman showed an error similar to:

```text
current system boot ID differs from cached boot ID
unhandled reboot occurred
```

## Cause

The system was rebooted, but Podman had old cached boot information.

## Check

Check the current boot ID:

```bash
cat /proc/sys/kernel/random/boot_id
```

Check Podman:

```bash
podman info
```

## Solution

Restart the required Podman services/containers and verify the system state.

```bash
podman ps
podman info
```

If required, restart the Podman-related service/environment according to the server configuration.

## Lesson Learned

After a server reboot, always verify **Podman status, containers, and runtime configuration** before starting the application.
