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