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

## 📖 Next Topic

➡️ **Containers/01-What-is-a-Container.md**