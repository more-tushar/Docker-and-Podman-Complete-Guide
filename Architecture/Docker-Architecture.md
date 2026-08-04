# Docker Architecture

## Introduction

Docker Architecture explains how Docker works to build, run, and manage containers. It consists of different components that work together.

> **In simple words:** Docker Architecture shows how Docker creates and runs containers.

---

## Main Components

### Docker Client

The Docker Client is the command-line tool that users interact with.

Example:

```bash
docker build
docker run
docker ps
```

---

### Docker Daemon

The Docker Daemon is a background service that manages Docker images, containers, networks, and volumes.

---

### Docker Image

A Docker Image is a read-only template that contains everything needed to run an application.

---

### Docker Container

A Docker Container is a running instance of a Docker Image.

---

### Docker Registry

A Docker Registry stores Docker images.

Example:

- Docker Hub
- Private Registry

---

## How Docker Works

```text
User
   │
   ▼
Docker Client
   │
   ▼
Docker Daemon
   │
   ├── Builds Images
   ├── Runs Containers
   ├── Manages Networks
   └── Manages Volumes
```

---

## Summary

Docker Architecture consists of the Docker Client, Docker Daemon, Docker Images, Containers, and a Docker Registry. These components work together to build, run, and manage containerized applications.

---

## 📖 Next Topic

➡️ **Podman-Architecture.md**

In the next chapter, we'll learn how Podman Architecture works and how it differs from Docker Architecture.