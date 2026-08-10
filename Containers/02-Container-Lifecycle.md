# Container Lifecycle

## Introduction

A Docker Container goes through different stages during its lifecycle.

> **In simple words:** A container is created, started, stopped, and removed.

---

## Container Lifecycle

```text
Docker Image
      │
      ▼
Container Created
      │
      ▼
Container Running
      │
      ▼
Container Stopped
      │
      ▼
Container Removed
```

---

## Common Commands

### Create a Container

```bash
docker create nginx
```

---

### Start a Container

```bash
docker start <container-id>
```

---

### Stop a Container

```bash
docker stop <container-id>
```

---

### Restart a Container

```bash
docker restart <container-id>
```

---

### Remove a Container

```bash
docker rm <container-id>
```

---

## Summary

A Docker Container moves through different stages, such as create, start, stop, restart, and remove.

---

## 📖 Next Topic

➡️ **Volumes/01-What-is-a-Volume.md**