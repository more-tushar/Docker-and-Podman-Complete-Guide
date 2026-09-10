# CMD vs ENTRYPOINT

## Introduction

`CMD` and `ENTRYPOINT` are Dockerfile instructions used to define what happens when a container starts.

> **In simple words:** Both `CMD` and `ENTRYPOINT` tell Docker what to run when the container starts.

---

## What is CMD?

The `CMD` instruction specifies the **default command** to run when a container starts.

### Example

```dockerfile
FROM ubuntu:24.04

CMD ["echo", "Hello Docker"]
```

When the container starts, it prints:

```text
Hello Docker
```

---

## What is ENTRYPOINT?

The `ENTRYPOINT` instruction specifies the **main command** that always runs when the container starts.

### Example

```dockerfile
FROM ubuntu:24.04

ENTRYPOINT ["echo", "Hello Docker"]
```

When the container starts, it prints:

```text
Hello Docker
```

---

## Difference

| CMD | ENTRYPOINT |
|-----|------------|
| Sets the default command | Sets the main command |
| Can be overridden | Runs every time the container starts |
| Used for default behavior | Used when the container should always perform one task |

---

## Summary

Use **CMD** when you want to provide a default command that users can change.

Use **ENTRYPOINT** when the container should always run the same main command.

---