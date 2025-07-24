# 🔐 File & Directory Permissions in Linux

## 🧩 Permission Structure

Each file/directory has **three permission sets**:

- **User (u)** – the file's owner
- **Group (g)** – users in the file's group
- **Others (o)** – all other users

### 🔤 Symbolic Notation:
-rwxr-xr--
│ │ │ │ │
│ │ │ │ └── Others: read (r)
│ │ │ └──── Group: read (r), execute (x)
│ │ └────── User: read (r), write (w), execute (x)
│ └──────── File (-) or Directory (d)


---

## 🔢 Numeric (Octal) Notation:

| Symbolic | Numeric | Description                     |
|----------|---------|---------------------------------|
| `r--`    | `4`     | Read                            |
| `-w-`    | `2`     | Write                           |
| `--x`    | `1`     | Execute                         |
| `rwx`    | `7`     | Read, write, and execute        |

**Example:**
- `chmod 755 filename`  
  → `rwxr-xr-x`  
  → Owner can read/write/execute, others can read/execute

---

## 🛠️ Common Commands:

| Command                            | Description                                   |
|------------------------------------|-----------------------------------------------|
| `ls -l`                            | View permissions of files/directories         |
| `chmod [mode] [file]`              | Change permissions (e.g., `chmod 755 file`)   |
| `chmod u+x [file]`                 | Add execute permission for the user           |
| `chmod g-w [file]`                 | Remove write permission for group             |
| `chown user:group [file]`          | Change owner and group                        |
| `chgrp [group] [file]`             | Change group ownership                        |

---
