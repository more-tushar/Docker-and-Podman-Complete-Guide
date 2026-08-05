## Summary

### Use `COPY`

Use `COPY` when you only want to copy files or folders from your local machine into the Docker image.

**Example:**

```dockerfile
COPY app.py /app/
```

This copies `app.py` into the `/app/` directory inside the Docker image.

---

### Use `ADD`

Use `ADD` when you need its extra features, such as automatically extracting a local `.tar` archive.

**Example:**

```dockerfile
ADD project.tar.gz /app/
```

This copies `project.tar.gz` and automatically extracts it into the `/app/` directory.

---
## Difference

| COPY | ADD |
|------|-----|
| Copies files and folders | Copies files and folders |
| Simple and commonly used | Has extra features |
| Does not extract `.tar` files | Automatically extracts local `.tar` files |
| Recommended for most Dockerfiles | Use only when extra features are needed |

### Easy Way to Remember

- **COPY** → Simply copies files and folders.
- **ADD** → Copies files and also has extra features (like extracting local `.tar` files).

> **Recommendation:** In most Dockerfiles, use **COPY**. Use **ADD** only when you need its additional features.