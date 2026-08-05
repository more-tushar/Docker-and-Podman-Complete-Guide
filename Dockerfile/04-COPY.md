# COPY Instruction

## What is the COPY Instruction?

The `COPY` instruction is used to copy files and folders from your local machine into a Docker image.

> **In simple words:** `COPY` copies files from your computer to the Docker image.

---

## Why do we use COPY?

We use the `COPY` instruction to:

- Copy application source code
- Copy configuration files
- Copy scripts
- Copy other required files

---

## Syntax

```dockerfile
COPY <source> <destination>
```

---

## Example 1

Copy a single file:

```dockerfile
COPY app.py /app/
```

This copies `app.py` from your local machine to the `/app/` directory inside the Docker image.

---

## Example 2

Copy all files:

```dockerfile
COPY . .
```

This copies all files from the current directory to the current working directory inside the Docker image.

---

## Example 3

Copy a folder:

```dockerfile
COPY static/ /app/static/
```

This copies the `static` folder into the `/app/static/` directory inside the Docker image.

---

## Common COPY Examples

| Command | Purpose |
|---------|---------|
| `COPY . .` | Copies all files |
| `COPY app.py /app/` | Copies a single file |
| `COPY requirements.txt /app/` | Copies the requirements file |
| `COPY static/ /app/static/` | Copies a folder |

---

## Summary

The `COPY` instruction is used to copy files and folders from your local machine into a Docker image. It helps include your application code and other required files in the image.

---

## 📖 Next Topic

➡️ **05-CMD-vs-ENTRYPOINT.md**

In the next chapter, we'll learn the difference between the **CMD** and **ENTRYPOINT** instructions and when to use each one.