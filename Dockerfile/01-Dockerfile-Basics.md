# Dockerfile Basics

## What is a Dockerfile?

A Dockerfile is a text file that contains instructions for building a Docker image. It tells Docker what steps to follow, such as copying files, installing packages, and starting the application.

> **In simple words:** A Dockerfile is a set of instructions used to create a Docker image.

---

## Why do we use a Dockerfile?

We use a Dockerfile to:

- Build Docker images automatically
- Install required software and dependencies
- Copy application files
- Run applications inside containers
- Create the same image every time

---

## Simple Dockerfile Example

```dockerfile
FROM ubuntu:24.04

RUN apt-get update

CMD ["echo", "Hello, Docker!"]
```

---

## Common Dockerfile Instructions

| Instruction | Purpose |
|-------------|---------|
| `FROM` | Selects the base image |
| `RUN` | Executes commands while building the image |
| `COPY` | Copies files into the image |
| `CMD` | Sets the default command when the container starts |
| `WORKDIR` | Sets the working directory |
| `EXPOSE` | Documents the port used by the application |

---

## How Dockerfile Works

```text
Dockerfile
     │
     ▼
docker build
     │
     ▼
Docker Image
     │
     ▼
Docker Container
```

---

## Build an Image

```bash
docker build -t my-app .
```

---

## Run a Container

```bash
docker run my-app
```

---

## Summary

A Dockerfile is a text file that contains instructions to build a Docker image. It helps create consistent and reusable images for running applications in containers.

---

## 📖 Next Topic

➡️ **02-FROM.md**

In the next chapter, we'll learn about the **FROM** instruction and why every Dockerfile starts with it.