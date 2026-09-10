# Container Exit Code 137

## Problem

Container stopped with:

```text
Exited (137)
```

## Meaning

Exit code `137` usually means the process was killed with `SIGKILL`.

One common reason is **Out Of Memory (OOM)**.

## Check

```bash
docker inspect <container>
```

Podman:

```bash
podman inspect <container>
```

Check system memory:

```bash
free -h
```

Check container resources:

```bash
podman stats
```

## Possible Solution

Increase available memory or reduce application memory usage.

You can also set a memory limit:

```bash
podman run --memory=512m nginx
```

## Lesson Learned

For exit code `137`, always check **memory usage and container resource limits**.
