# Podman Commands

This file contains commonly used Podman commands for building, running, and managing containers.

---

## 1. Check Podman Version

```bash
podman --version
```

---

## 2. Pull an Image

```bash
podman pull nginx
```

---

## 3. List Images

```bash
podman images
```

---

## 4. Build an Image

```bash
podman build -t my-app .
```

---

## 5. Run a Container

```bash
podman run -d --name my-container nginx
```

---

## 6. List Running Containers

```bash
podman ps
```

---

## 7. List All Containers

```bash
podman ps -a
```

---

## 8. Stop a Container

```bash
podman stop my-container
```

---

## 9. Start a Container

```bash
podman start my-container
```

---

## 10. Restart a Container

```bash
podman restart my-container
```

---

## 11. Remove a Container

```bash
podman rm my-container
```

---

## 12. Remove an Image

```bash
podman rmi my-app
```

---

## 13. Check Container Logs

```bash
podman logs my-container
```

Follow logs:

```bash
podman logs -f my-container
```

---

## 14. Inspect a Container

```bash
podman inspect my-container
```

---

## 15. Execute Command Inside Container

```bash
podman exec -it my-container bash
```

For Alpine images:

```bash
podman exec -it my-container sh
```

---

## 16. Check Container Resource Usage

```bash
podman stats
```

---

## 17. List Networks

```bash
podman network ls
```

---

## 18. List Volumes

```bash
podman volume ls
```

---

## Common Podman Commands

| Command          | Purpose                          |
| ---------------- | -------------------------------- |
| `podman pull`    | Download image                   |
| `podman images`  | List images                      |
| `podman build`   | Build image                      |
| `podman run`     | Create and start container       |
| `podman ps`      | List running containers          |
| `podman stop`    | Stop container                   |
| `podman start`   | Start container                  |
| `podman restart` | Restart container                |
| `podman rm`      | Remove container                 |
| `podman rmi`     | Remove image                     |
| `podman logs`    | View logs                        |
| `podman exec`    | Execute command inside container |
| `podman inspect` | View detailed information        |
| `podman stats`   | View resource usage              |

### Key Point

**Podman CLI = Main tool used to manage Podman images, containers, networks, and volumes.**
