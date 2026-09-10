# Container Exit Code 135

## Problem

Container stopped with:

```text
Exited (135)
```

## Meaning

Exit code `135` indicates the process was terminated by a signal.

It commonly maps to:

```text
128 + 7 = 135
```

Signal `7` is `SIGBUS`.

## Check Logs

```bash
podman logs <container>
```

Check container details:

```bash
podman inspect <container>
```

## Possible Causes

* Application crash
* Memory or system issue
* Invalid memory access
* Runtime-related issue

## Troubleshooting

Check:

```bash
podman logs <container>
podman inspect <container>
podman stats
```

Then check the application and system logs.

## Lesson Learned

For exit code `135`, check **application logs, system resources, and OCI runtime issues**.