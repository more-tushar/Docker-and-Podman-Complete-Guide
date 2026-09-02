# Docker Compose Commands

Docker Compose commands are used to **start, stop, restart, and manage multiple containers**.

## 1. Start Containers

Start all services:

```bash
docker compose up -d
```

For Podman:

```bash
podman compose up -d
```

`-d` means run the containers in the background.

## 2. Stop and Remove Containers

```bash
docker compose down
```

Podman:

```bash
podman compose down
```

This stops and removes the containers created by Compose.

## 3. Check Container Status

```bash
docker compose ps
```

Podman:

```bash
podman compose ps
```

## 4. Check Logs

View logs:

```bash
docker compose logs
```

Follow logs continuously:

```bash
docker compose logs -f
```

Check logs for a specific service:

```bash
docker compose logs -f backend
```

Podman:

```bash
podman compose logs -f backend
```

## 5. Restart Containers

Restart all services:

```bash
docker compose restart
```

Restart a specific service:

```bash
docker compose restart backend
```

## 6. Start a Specific Service

```bash
docker compose up -d backend
```

This starts only the `backend` service.

## 7. Stop a Specific Service

```bash
docker compose stop backend
```

## 8. Build Images

If the Compose file contains a `build` configuration:

```bash
docker compose build
```

Build a specific service:

```bash
docker compose build backend
```

## 9. Pull Images

Pull images from a container registry:

```bash
docker compose pull
```

## 10. Common Production Flow

A simple deployment flow can be:

```bash
podman compose down
podman compose up -d
podman compose ps
podman compose logs -f
```

### Flow

```text
Stop old containers
        ↓
Start new containers
        ↓
Check container status
        ↓
Check logs
```

## Docker vs Podman Commands

| Purpose | Docker                   | Podman                   |
| ------- | ------------------------ | ------------------------ |
| Start   | `docker compose up -d`   | `podman compose up -d`   |
| Stop    | `docker compose down`    | `podman compose down`    |
| Status  | `docker compose ps`      | `podman compose ps`      |
| Logs    | `docker compose logs`    | `podman compose logs`    |
| Restart | `docker compose restart` | `podman compose restart` |
| Build   | `docker compose build`   | `podman compose build`   |
| Pull    | `docker compose pull`    | `podman compose pull`    |

## Summary

The most commonly used Compose commands are:

```bash
docker compose up -d
docker compose down
docker compose ps
docker compose logs -f
docker compose restart
```

For Podman:

```bash
podman compose up -d
podman compose down
podman compose ps
podman compose logs -f
podman compose restart
```

### Key Point

**Compose commands = Easy way to manage multiple containers together.**
