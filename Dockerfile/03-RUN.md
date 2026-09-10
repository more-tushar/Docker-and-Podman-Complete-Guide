# RUN Instruction

## What is the RUN Instruction?

The `RUN` instruction is used to execute commands while building a Docker image.

> **In simple words:** `RUN` executes commands during the image build process.

---

## Why do we use RUN?

We use the `RUN` instruction to:

- Install software and packages
- Update the operating system
- Create directories
- Configure the application environment

---

## Syntax

```dockerfile
RUN <command>
```

---

## Example 1

Update the package list:

```dockerfile
RUN apt-get update
```

---

## Example 2

Install Nginx:

```dockerfile
RUN apt-get update && apt-get install -y nginx
```

---

## Example 3

Create a directory:

```dockerfile
RUN mkdir /app
```

---

## Common RUN Commands

| Command | Purpose |
|---------|---------|
| `RUN apt-get update` | Updates the package list |
| `RUN apt-get install -y nginx` | Installs Nginx |
| `RUN mkdir /app` | Creates a directory |
| `RUN pip install -r requirements.txt` | Installs Python packages |
| `RUN npm install` | Installs Node.js packages |

---

## Summary

The `RUN` instruction executes commands while building a Docker image. It is commonly used to install software, create directories, and prepare the application environment.

---