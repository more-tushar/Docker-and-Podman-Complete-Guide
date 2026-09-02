# Docker Compose YAML File

## What is `docker-compose.yml`?

`docker-compose.yml` is a YAML file used to define and configure multiple services/containers.

**In simple words:**
It tells Docker or Podman **which containers to run and how to configure them**.

## Basic Example

```yaml
services:
  frontend:
    image: my-frontend
    ports:
      - "8080:80"

  backend:
    image: my-backend
    ports:
      - "8000:8000"

  database:
    image: postgres
```

In this example, we have three services:

* Frontend
* Backend
* Database

## Common Options

### 1. `services`

Defines the containers/services.

```yaml
services:
  backend:
    image: my-backend
```

### 2. `image`

Specifies the container image.

```yaml
image: nginx:latest
```

### 3. `container_name`

Sets a custom container name.

```yaml
container_name: my-backend
```

### 4. `ports`

Maps the host port to the container port.

```yaml
ports:
  - "8080:80"
```

Meaning:

```text
Host Port 8080 → Container Port 80
```

### 5. `environment`

Defines environment variables.

```yaml
environment:
  APP_ENV: production
  PORT: 8000
```

### 6. `volumes`

Used to mount or store data.

```yaml
volumes:
  - my-volume:/app/data
```

### 7. `networks`

Connects containers to a network.

```yaml
networks:
  - my-network
```

### 8. `restart`

Controls container restart behavior.

```yaml
restart: always
```

Common values:

* `always`
* `unless-stopped`
* `no`

### 9. `depends_on`

Defines a dependency between services.

```yaml
backend:
  image: my-backend
  depends_on:
    - database
```

Here, the backend depends on the database service.

## External Network

Example:

```yaml
networks:
  idbi-network:
    external: true
```

`external: true` means Compose will use an **existing network** instead of creating a new one.

Example:

```bash
docker network create idbi-network
```

> **Note:** `external: true` does not define the network type. Use `docker network inspect <network-name>` to check the network type.

## Docker Compose and Podman Compose

The same Compose YAML concepts can generally be used with Docker and Podman.

Docker:

```bash
docker compose up -d
```

Podman:

```bash
podman compose up -d
```

## Summary

| Option           | Purpose                    |
| ---------------- | -------------------------- |
| `services`       | Defines containers         |
| `image`          | Specifies image            |
| `container_name` | Sets container name        |
| `ports`          | Maps ports                 |
| `environment`    | Sets environment variables |
| `volumes`        | Mounts/stores data         |
| `networks`       | Connects containers        |
| `restart`        | Controls restart behavior  |
| `depends_on`     | Defines dependencies       |

### Key Point

**Compose YAML file = Configuration for multiple containers.**
