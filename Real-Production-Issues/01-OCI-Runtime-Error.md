# OCI Runtime Error

## Problem

Podman container failed to start with:

```text
crun: systemd failed to install eBPF device filter on cgroup
```

## Cause

The issue was related to the **OCI runtime (`crun`) and cgroup configuration**.

## Solution

Changed the OCI runtime from:

```text
crun
```

to:

```text
runc
```

Check:

```bash
podman info
```

Restart containers:

```bash
podman compose down
podman compose up -d
```

## Lesson Learned

For OCI runtime errors, check:

* OCI runtime
* Cgroup configuration
* Podman configuration
* Container logs
