# FROM Instruction

## What is the FROM Instruction?

The `FROM` instruction is used to specify the **base image** for a Docker image. Every Dockerfile starts with a `FROM` instruction.

> **In simple words:** `FROM` tells Docker which image to use as the starting point.

---

## Why do we use FROM?

We use the `FROM` instruction to:

- Choose a base operating system or runtime
- Build applications on an existing image
- Avoid creating everything from scratch

---

## Syntax

```dockerfile
FROM <image-name>:<tag>
```

---

## Example 1

```dockerfile
FROM ubuntu:24.04
```

This uses the Ubuntu 24.04 image as the base image.

---

## Example 2

```dockerfile
FROM python:3.12
```

This uses the Python 3.12 image, which already includes Python.

---

## Example 3

```dockerfile
FROM node:24
```

This uses the Node.js 24 image, which already includes Node.js.

---

## Common Base Images

| Base Image | Used For |
|------------|----------|
| `ubuntu:24.04` | Ubuntu applications |
| `python:3.12` | Python applications |
| `node:24` | Node.js applications |
| `nginx:latest` | Nginx web server |
| `alpine:latest` | Lightweight Linux image |

---

## Summary

The `FROM` instruction is the first instruction in a Dockerfile. It tells Docker which base image to use for building your application.

---

## 📖 Next Topic

➡️ **03-RUN.md**

In the next chapter, we'll learn about the **RUN** instruction and how it is used to install packages and execute commands while building a Docker image.