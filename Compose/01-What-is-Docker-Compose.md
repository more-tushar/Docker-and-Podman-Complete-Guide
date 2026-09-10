# What is Docker Compose?

## Introduction

Docker Compose is a tool used to define and manage multiple containers using a single YAML file.

> **In simple words:** Docker Compose helps us manage multiple containers together.

---

## Why do we use Docker Compose?

Without Compose, we may need to run many Docker commands separately.

For example:

```bash
docker run ...
docker run ...
docker run ...
```

With Docker Compose, we can define all the services in one file and start them together.

---

## Example

Suppose an application has:

```text
Frontend
   │
   ▼
Backend
   │
   ▼
Database
```

We can define these services in one Compose file.

```yaml
services:
  frontend:
    image: my-frontend

  backend:
    image: my-backend

  database:
    image: postgres
```

Then start everything with:

```bash
docker compose up -d  Or podman compose up -d
```

---

## Benefits

- Manage multiple containers together
- Simple configuration
- Easy application startup
- Easy to stop and restart services
- Useful for development and deployment

---

## Summary

Docker Compose allows us to define multiple containers and their configuration in one YAML file. It makes it easier to start, stop, and manage an application with multiple services.

---