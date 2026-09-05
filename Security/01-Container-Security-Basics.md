# Container Security Basics

Container security means protecting **container images, containers, applications, and the host system**.

**In simple words:**
Make sure containers are running safely and do not get unnecessary access to the host system.

---

## Why Container Security is Important?

Containers run applications and may have access to:

* Files
* Networks
* Environment variables
* Volumes
* System resources

If a container is not configured properly, it can create security risks.

---

## Basic Security Practices

### 1. Use Trusted Images

Use images from trusted sources.

Example:

```bash
docker pull nginx:latest
```

Avoid using unknown or untrusted images.

---

### 2. Do Not Run as Root

Whenever possible, run applications using a non-root user.

Dockerfile example:

```dockerfile
USER appuser
```

Podman also supports rootless containers.

```bash
podman run nginx
```

---

### 3. Use Specific Image Tags

Instead of:

```dockerfile
FROM nginx:latest
```

Use a specific version when appropriate:

```dockerfile
FROM nginx:1.27
```

This helps make deployments more predictable.

---

### 4. Do Not Store Secrets in Images

Avoid putting passwords, API keys, or tokens directly inside a Dockerfile.

Bad example:

```dockerfile
ENV DB_PASSWORD=mysecretpassword
```

Use environment variables, secret-management systems, or other secure methods instead.

---

### 5. Give Only Required Permissions

Do not give containers unnecessary privileges.

Avoid using:

```bash
docker run --privileged ...
```

unless it is specifically required.

---

### 6. Keep Images Small

Use smaller base images when suitable.

Smaller images can have:

* Fewer packages
* Fewer vulnerabilities
* Faster downloads
* Smaller attack surface

---

## Summary

Important container security practices:

* Use trusted images
* Avoid running as root
* Use specific image versions
* Do not store secrets in images
* Avoid unnecessary privileges
* Keep images small

### Key Point

**Container Security = Minimum Access + Trusted Images + Secure Configuration**
