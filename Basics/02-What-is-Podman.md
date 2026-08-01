# What is Podman?

## Introduction

Podman is an open-source container engine used to build, run, and manage containers. It allows developers and system administrators to run applications in isolated environments.

> **In simple words:** Podman helps you build and run containers without needing a background service (daemon).

---

## Why was Podman created?

Podman was created to provide a more secure and flexible way to manage containers. It supports **rootless containers**, allowing users to run containers without root privileges, which improves security.

It also provides a Docker-compatible command-line interface, making it easy for Docker users to switch to Podman.

---

## Why do we use Podman?

- Daemonless architecture
- Supports rootless containers
- Improved security
- Docker-compatible commands
- Lightweight and easy to manage

---

## How Podman Works

```text
Application
     │
     ▼
Containerfile / Dockerfile
     │
     ▼
Container Image
     │
     ▼
Podman Container
```

---

## Basic Podman Commands

### Build an Image

```bash
podman build -t my-app .
```

### Run a Container

```bash
podman run -d -p 8080:80 my-app
```

### View Running Containers

```bash
podman ps
```

---

## Summary

Podman is a daemonless container engine that allows you to build, run, and manage containers securely. It supports rootless containers and is compatible with most Docker commands, making it a great alternative to Docker.