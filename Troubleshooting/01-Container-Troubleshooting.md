# Container Troubleshooting

## Common Problems

### Container Not Starting

```bash
docker ps -a
docker logs <container>
```

### Container Exits Immediately

Check:

```bash
docker logs <container>
docker inspect <container>
```

Common reasons:

* Application error
* Wrong `CMD` or `ENTRYPOINT`
* Missing environment variable

### Port Already in Use

Check:

```bash
ss -tulpn | grep 8080
```

Or check containers:

```bash
docker ps
```

### Build Failed

```bash
docker build -t my-app .
```

Check the Dockerfile step where the error occurred.

## Basic Troubleshooting Flow

```text
Check Status
     ↓
Check Logs
     ↓
Check Exit Code
     ↓
Check Configuration
     ↓
Fix & Restart
```

### Key Point

**Logs + Exit Code + Inspect = First steps for troubleshooting.**
