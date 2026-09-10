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

Check the configuration:

```bash
podman info
```

Then restart:

```bash
podman compose down
podman compose up -d
```

## Lesson Learned

When a Podman container fails with an OCI runtime error, check:

* OCI runtime
* Cgroup configuration
* Podman configuration
* Container logs
