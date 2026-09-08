# Container Exit Codes

Exit codes tell us why a container stopped.

## Common Exit Codes

| Exit Code | Meaning                       |
| --------- | ----------------------------- |
| `0`       | Success                       |
| `1`       | General error                 |
| `126`     | Command cannot execute        |
| `127`     | Command not found             |
| `137`     | Process killed / OOM possible |
| `143`     | Process terminated            |

## Check Exit Code

```bash
docker ps -a
```

Podman:

```bash
podman ps -a
```

Or:

```bash
docker inspect <container> --format='{{.State.ExitCode}}'
```

### Key Point

**Exit Code `0` = Success**
**Non-zero = Error or abnormal termination**
