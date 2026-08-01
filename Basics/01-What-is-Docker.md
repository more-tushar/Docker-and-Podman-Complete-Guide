# What is Docker?

## Introduction

Docker is an open-source containerization platform that packages an application along with its code, libraries, dependencies, runtime, and configuration into a **container**. This allows the application to run consistently across different environments.

> **In simple words:** Docker helps you build an application once and run it anywhere.

---

## Why was Docker created?

Before Docker, applications often worked on a developer's machine but failed on testing or production servers because of different operating systems, library versions, or dependencies.

Docker solves this problem by packaging everything the application needs into a container, ensuring consistent behavior across different environments.

---

## Why do we use Docker?

- Consistent development and production environments
- Easy application deployment
- Dependency isolation
- Lightweight and fast
- Easy to scale and manage

---

## How Docker Works

```text
Application
     │
     ▼
Dockerfile
     │
     ▼
Docker Image
     │
     ▼
Docker Container
```

---

## Basic Docker Commands

### Build an Image

```bash
docker build -t my-app .
```

### Run a Container

```bash
docker run -d -p 8080:80 my-app
```

### View Running Containers

```bash
docker ps
```

---

## Summary

Docker is a containerization platform that packages applications and their dependencies into portable containers, making deployment faster, more reliable, and consistent across different environments.