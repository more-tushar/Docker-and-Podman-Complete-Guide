# Docker Image Security

Docker image security means making sure the images used to create containers are safe.

**In simple words:**
Before running an image, make sure it is **trusted, updated, and free from known vulnerabilities**.

---

## Why Image Security is Important?

A container gets its software and dependencies from the image.

If the image contains vulnerable packages, the running container may also be affected.

---

## 1. Use Trusted Images

Use official or trusted images whenever possible.

Example:

```bash
docker pull nginx
```

---

## 2. Keep Images Updated

Regularly update the base image and application dependencies.

Example:

```dockerfile
FROM ubuntu:24.04
```

Then rebuild the image when updates are available.

---

## 3. Scan Images

Image scanning helps identify known vulnerabilities.

For example, with Docker Scout:

```bash
docker scout quickview my-app
```

You can also use security scanning tools such as:

* Trivy
* Docker Scout
* Clair

---

## 4. Avoid Unnecessary Packages

Only install the packages required by the application.

Example:

```dockerfile
RUN apt-get update && \
    apt-get install -y nginx
```

Avoid installing unnecessary software.

---

## 5. Use Small Base Images

Example:

```dockerfile
FROM python:3.12-slim
```

A smaller image can reduce the number of packages that need to be maintained.

---

## 6. Do Not Store Secrets

Never put passwords or API keys directly into the image.

Avoid:

```dockerfile
ENV PASSWORD=my-password
```

Use a secure secret-management approach instead.

---

## Summary

For better image security:

* Use trusted images
* Keep images updated
* Scan images
* Remove unnecessary packages
* Use smaller base images when appropriate
* Never store secrets in images

### Key Point

**Secure Image = Trusted + Updated + Scanned + Minimal**
