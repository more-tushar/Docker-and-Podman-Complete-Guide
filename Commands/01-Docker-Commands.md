# Docker Commands

This file contains commonly used Docker commands for building, running, and managing containers.

---

## 1. Check Docker Version

```bash
docker --version
```

---

## 2. Pull an Image

```bash
docker pull nginx
```

---

## 3. List Images

```bash
docker images
```

---

## 4. Build an Image

```bash
docker build -t my-app .
```

* `-t` = image name/tag
* `.` = current directory

---

## 5. Run a Container

```bash
docker run -d --name my-container nginx
```

---

## 6. List Running Containers

```bash
docker ps
```

---

## 7. List All Containers

```bash
docker ps -a
```

---

## 8. Stop a Container

```bash
docker stop my-container
```

---

## 9. Start a Container

```bash
docker start my-container
```

---

## 10. Restart a Container

```bash
docker restart my-container
```

---

## 11. Remove a Container

```bash
docker rm my-container
```

---

## 12. Remove an Image

```bash
docker rmi my-app
```

---

## 13. Check Container Logs

```bash
docker logs my-container
```

Follow logs:

```bash
docker logs -f my-container
```

---

## 14. Inspect a Container

```bash
docker inspect my-container
```

---

## 15. Execute Command Inside Container

```bash
docker exec -it my-container bash
```

For Alpine images:

```bash
docker exec -it my-container sh
```

---

## 16. Check Container Resource Usage

```bash
docker stats
```

---

## 17. List Networks

```bash
docker network ls
```

---

## 18. List Volumes

```bash
docker volume ls
```

---

## Common Docker Commands

| Command          | Purpose                          |
| ---------------- | -------------------------------- |
| `docker pull`    | Download image                   |
| `docker images`  | List images                      |
| `docker build`   | Build image                      |
| `docker run`     | Create and start container       |
| `docker ps`      | List running containers          |
| `docker stop`    | Stop container                   |
| `docker start`   | Start container                  |
| `docker restart` | Restart container                |
| `docker rm`      | Remove container                 |
| `docker rmi`     | Remove image                     |
| `docker logs`    | View logs                        |
| `docker exec`    | Execute command inside container |
| `docker inspect` | View detailed information        |
| `docker stats`   | View resource usage              |

### Key Point

**Docker CLI = Main tool used to manage Docker images, containers, networks, and volumes.**
