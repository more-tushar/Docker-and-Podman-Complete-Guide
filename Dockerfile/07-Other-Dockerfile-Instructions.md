# Other Dockerfile Instructions

## Introduction

Docker provides several additional instructions that help configure and manage your Docker images.

---

# WORKDIR

The `WORKDIR` instruction sets the working directory inside the Docker image.

> **In simple words:** It tells Docker where to run the next commands.

### Example

```dockerfile
WORKDIR /app
```

---

# EXPOSE

The `EXPOSE` instruction documents the port that the application uses.

> **In simple words:** It tells Docker which port the application listens on.

### Example

```dockerfile
EXPOSE 8080
```

---

# ENV

The `ENV` instruction sets environment variables inside the Docker image.

> **In simple words:** It stores values that the application can use.

### Example

```dockerfile
ENV NODE_ENV=production
```

---

# ARG

The `ARG` instruction defines variables that are available only during the image build process.

> **In simple words:** It passes values while building the image.

### Example

```dockerfile
ARG VERSION=1.0
```

---

# LABEL

The `LABEL` instruction adds information (metadata) to a Docker image.

> **In simple words:** It stores information about the image.

### Example

```dockerfile
LABEL author="Tushar More"
```

---

# USER

The `USER` instruction specifies which user runs the application inside the container.

> **In simple words:** It tells Docker which user should run the container.

### Example

```dockerfile
USER appuser
```

---

# VOLUME

The `VOLUME` instruction creates a mount point for storing persistent data.

> **In simple words:** It keeps data even if the container is removed.

### Example

```dockerfile
VOLUME ["/data"]
```

---

# Multi-Stage Build

A Multi-Stage Build uses multiple `FROM` instructions to create a smaller and cleaner Docker image.

> **In simple words:** It removes unnecessary files and reduces image size.

### Example

```dockerfile
FROM node:24 AS build

WORKDIR /app

COPY . .

RUN npm install

FROM nginx:latest

COPY --from=build /app/dist /usr/share/nginx/html
```

---

# Summary

| Instruction | Purpose |
|------------|---------|
| `WORKDIR` | Sets the working directory |
| `EXPOSE` | Documents the application port |
| `ENV` | Sets environment variables |
| `ARG` | Defines build-time variables |
| `LABEL` | Adds image metadata |
| `USER` | Specifies the container user |
| `VOLUME` | Stores persistent data |
| `Multi-Stage Build` | Creates smaller Docker images |

---