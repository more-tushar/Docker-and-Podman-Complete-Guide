# What is a Docker Volume?

## Introduction

A Docker Volume is used to store data outside the container.

> **In simple words:** A volume keeps your data safe even if the container is removed.

---

## Why do we use Volumes?

Containers are temporary. If a container is removed, the data inside it can also be lost.

Volumes help us to:

- Keep data after a container is removed
- Store database data
- Share data between containers
- Keep application data separate from the container

---

## How a Volume Works

```text
Docker Container
       │
       ▼
    Volume
       │
       ▼
 Persistent Data
```

---

## Create a Volume

```bash
docker volume create my-volume
```

---

## View Volumes

```bash
docker volume ls
```

---

## Use a Volume

```bash
docker run -d \
  --name my-container \
  -v my-volume:/app/data \
  nginx
```

Here:

- `my-volume` → Docker volume
- `/app/data` → Directory inside the container

---

## Remove a Volume

```bash
docker volume rm my-volume
```

---

## Summary

A Docker Volume is used to store persistent data outside a container. It helps keep important data safe even when a container is removed.

---