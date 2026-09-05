# Container Security Best Practices

Here are some simple best practices for running containers securely.

## Best Practices

### 1. Run Containers as Non-Root

Use a non-root user whenever possible.

Dockerfile:

```dockerfile
USER appuser
```

---

### 2. Use Rootless Containers

Podman supports rootless containers.

```bash
podman run -d nginx
```

---

### 3. Avoid `--privileged`

Do not use privileged mode unless it is required.

```bash
docker run --privileged nginx
```

`--privileged` gives the container additional access and should be avoided when unnecessary.

---

### 4. Limit Resources

Containers can be limited for CPU and memory.

Example:

```bash
docker run -d --memory=512m --cpus=1 nginx
```

This limits the container to approximately:

* 512 MB memory
* 1 CPU

---

### 5. Protect Sensitive Data

Do not expose passwords, tokens, or API keys unnecessarily.

Use secure secret-management methods.

---

### 6. Keep Host and Container Runtime Updated

Regularly update:

* Host operating system
* Docker
* Podman
* Container images
* Application dependencies

---

### 7. Monitor Container Logs

Check logs regularly.

```bash
docker logs <container>
```

Podman:

```bash
podman logs <container>
```

---

## Security Checklist

```text
✓ Use trusted images
✓ Scan images
✓ Keep images updated
✓ Run as non-root
✓ Use rootless containers
✓ Avoid privileged containers
✓ Limit CPU and memory
✓ Protect secrets
✓ Update Docker/Podman
✓ Monitor logs
```

## Summary

Container security is mainly about **reducing unnecessary access and keeping everything updated**.

### Key Point

**Give containers only the permissions and resources they actually need.**
