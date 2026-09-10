# Bind Mount vs Volume

## Introduction

Docker provides two common ways to store data outside a container:

- Volumes
- Bind Mounts

Both can keep data outside the container, but they work differently.

---

## Volume

A volume is managed by Docker.

```bash
docker run -v my-volume:/app/data nginx
```

> **In simple words:** Docker manages where the data is stored.

---

## Bind Mount

A bind mount uses a directory from your computer.

```bash
docker run -v /home/user/data:/app/data nginx
```

> **In simple words:** You choose the directory on your computer where the data is stored.

---

## Difference

| Volume | Bind Mount |
|--------|------------|
| Managed by Docker | Managed by the user |
| Docker chooses the storage location | User chooses the storage location |
| Good for application and database data | Good for development and local files |
| Easier to manage | More control over files |

---

## Simple Example

### Volume

```text
Docker
  │
  ▼
Volume
  │
  ▼
Container
```

### Bind Mount

```text
Your Computer
      │
      ▼
  /home/user/data
      │
      ▼
  Container
```

---

## Summary

Use **Volumes** when you want Docker to manage persistent data.

Use **Bind Mounts** when you need direct access to files on your computer.

---