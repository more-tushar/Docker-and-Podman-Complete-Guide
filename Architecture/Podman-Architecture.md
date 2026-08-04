# Podman Architecture

## Introduction

Podman Architecture explains how Podman builds, runs, and manages containers. Unlike Docker, Podman does not use a background service (daemon).

> **In simple words:** Podman runs containers directly without using a daemon.

---

## Main Components

### Podman CLI

The Podman CLI is the command-line tool that users interact with.

Example:

```bash
podman build
podman run
podman ps
```

---

### Container Engine

Podman directly manages container images, containers, networks, and volumes without requiring a background daemon.

---

### Container Image

A Container Image is a template that contains everything needed to run an application.

---

### Container

A Container is a running instance of a container image.

---

### Container Registry

A Container Registry stores container images.

Example:

- Docker Hub
- Quay.io
- Private Registry

---

## How Podman Works

```text
User
   │
   ▼
Podman CLI
   │
   ▼
Container Engine
   │
   ├── Builds Images
   ├── Runs Containers
   ├── Manages Networks
   └── Manages Volumes
```

---

## Summary

Podman Architecture consists of the Podman CLI, Container Engine, Container Images, Containers, and a Container Registry. Since Podman is daemonless, it can run and manage containers directly.

---

## 📖 Next Topic

➡️ **Dockerfile/01-Dockerfile-Basics.md**

In the next chapter, we'll learn what a Dockerfile is, why it is used, and how to create your first Docker image.