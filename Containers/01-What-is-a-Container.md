# What is a Container?

## Introduction

A Docker Container is a running instance of a Docker Image. It runs the application in an isolated environment.

> **In simple words:** A container is a running application created from a Docker Image.

---

## Why do we use Containers?

We use containers to:

- Run applications
- Isolate applications
- Keep environments consistent
- Deploy applications easily

---

## How Containers Work

```text
Docker Image
      │
      ▼
Docker Container
      │
      ▼
Running Application
```

---

## Basic Commands

### Run a Container

```bash
docker run my-app
```

---

### View Running Containers

```bash
docker ps
```

---

### Stop a Container

```bash
docker stop <container-id>
```

---

### Remove a Container

```bash
docker rm <container-id>
```

---

## Summary

A Docker Container is a running instance of a Docker Image. It allows applications to run in an isolated and consistent environment.

---