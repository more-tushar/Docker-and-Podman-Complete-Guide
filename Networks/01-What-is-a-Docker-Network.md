# What is a Docker Network?

## Introduction

A Docker Network allows containers to communicate with each other and with other systems.

> **In simple words:** A Docker Network helps containers talk to each other.

---

## Why do we use Docker Networks?

Docker Networks are used to:

- Connect multiple containers
- Allow containers to communicate with each other
- Separate application traffic
- Connect containers to the internet
- Improve container security

---

## Simple Example

Suppose we have:

```text
Frontend Container
       │
       ▼
Backend Container
       │
       ▼
Database Container
```

All three containers can communicate through a Docker Network.

---

## Create a Network

```bash
docker network create my-network
```

---

## View Networks

```bash
docker network ls
```

---

## Run a Container on a Network

```bash
docker run -d \
  --name my-container \
  --network my-network \
  nginx
```

---

## Inspect a Network

```bash
docker network inspect my-network
```

---

## Remove a Network

```bash
docker network rm my-network
```

---

## Summary

A Docker Network connects containers and allows them to communicate with each other. It is commonly used when multiple containers work together as one application.

---

## 📖 Next Topic

➡️ **02-Docker-Network-Types.md**

In the next chapter, we'll learn about the different types of Docker Networks, such as **Bridge, Host, None, and Overlay**.