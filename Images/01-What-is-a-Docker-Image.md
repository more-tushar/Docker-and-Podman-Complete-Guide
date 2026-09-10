# What is a Docker Image?

## Introduction

A Docker Image is a read-only template used to create Docker containers. It contains everything an application needs to run, such as the application code, libraries, dependencies, and configuration.

> **In simple words:** A Docker Image is a blueprint used to create containers.

---

## Why do we use Docker Images?

We use Docker Images to:

- Create containers
- Share applications easily
- Keep the same environment everywhere
- Deploy applications quickly

---

## How Docker Images Work

```text
Dockerfile
     │
     ▼
Docker Image
     │
     ▼
Docker Container
```

---

## Basic Commands

### Build an Image

```bash
docker build -t my-app .
```

---

### View Images

```bash
docker images
```

---

### Remove an Image

```bash
docker rmi my-app
```

---

## Summary

A Docker Image is a blueprint that contains everything needed to run an application. It is used to create Docker containers.

---

## 📖 Next Topic

➡️ **02-Image-Layers.md**

In the next chapter, we'll learn how Docker Images are built using layers and why layers make Docker fast and efficient.  

# Docker Image Layers

## Introduction

A Docker Image is made up of multiple layers. Each instruction in a Dockerfile creates a new layer.

> **In simple words:** A Docker Image is built layer by layer.

---

## Example

Dockerfile:

```dockerfile
FROM ubuntu:24.04

RUN apt-get update

COPY . .

CMD ["python", "app.py"]
```

Layers:

```text
Layer 4 → CMD
Layer 3 → COPY
Layer 2 → RUN
Layer 1 → FROM
```

---

## Why are Layers Important?

- Faster image builds
- Reuses existing layers
- Saves disk space
- Speeds up image downloads

---

## Summary

Docker Images are built using layers. Docker reuses these layers whenever possible, making builds faster and more efficient.

---