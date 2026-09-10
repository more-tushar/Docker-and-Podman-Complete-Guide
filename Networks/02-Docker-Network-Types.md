# Docker Network Types

## Introduction

Docker provides different types of networks for different use cases.

> **In simple words:** Different network types control how containers communicate.

---

## 1. Bridge Network

The **Bridge** network is the default network type for Docker containers.

It allows containers on the same network to communicate with each other.

```bash
docker network create my-network
```

Example:

```text
Container 1
     │
     ├── Docker Bridge Network
     │
Container 2
```

> **Commonly used for:** Applications running on a single Docker host.

---

## 2. Host Network

The **Host** network allows a container to use the host machine's network directly.

```bash
docker run --network host nginx
```

> **In simple words:** The container uses the host's network instead of having its own separate network.

---

## 3. None Network

The **None** network disables network access for the container.

```bash
docker run --network none nginx
```

> **In simple words:** The container has no network connection.

---

## 4. Overlay Network

The **Overlay** network connects containers running on different Docker hosts.

> **In simple words:** Overlay networks allow containers on different machines to communicate.

They are commonly associated with Docker Swarm.

---

## Network Types Summary

| Network | Simple Meaning |
|---------|----------------|
| Bridge | Containers communicate on the same Docker host |
| Host | Container uses the host network |
| None | No network connection |
| Overlay | Connects containers across multiple Docker hosts |

---

## Summary

Docker provides different network types depending on how containers need to communicate. **Bridge** is commonly used for containers on the same host, while **Overlay** can connect containers across multiple hosts.

---