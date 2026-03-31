---
layout: default
---

# 🔐 Linux User & Permission Management

This section covers user, group, and permission management used in Linux system administration.

---

## 👤 User Management

| Command | Usage & Options |
|--------|----------------|
| `useradd testuser` | Create a new user |
| `passwd testuser` | Set password for user |
| `userdel testuser` | Delete a user |
| `id testuser` | Show user ID, group ID, and groups |

---

## 👥 Group Management

| Command | Usage & Options |
|--------|----------------|
| `groupadd devgroup` | Create a new group |
| `usermod -aG devgroup testuser` | Add user to group; `-a` → append (do not remove existing groups), `-G` → group |
| `groups testuser` | Show groups of a user |

---

## 🔐 File Permissions

| Command | Usage & Options |
|--------|----------------|
| `ls -l` | List file permissions; `-l` → long format (permissions, owner, size, date) |
| `chmod 755 file.sh` | Change permissions; 7 → rwx (owner), 5 → r-x (group), 5 → r-x (others) |
| `chmod u+x file.sh` | Add execute permission; `u` → user, `+` → add, `x` → execute |
| `chown user:group file.txt` | Change file ownership; `user:group` → owner:group |

---

## 🔢 Permission Breakdown

| Value | Meaning |
|------|--------|
| 7 | Read (r) + Write (w) + Execute (x) |
| 6 | Read (r) + Write (w) |
| 5 | Read (r) + Execute (x) |
| 4 | Read only |
| 0 | No permission |

---

## 🔥 Useful Example

| Command | Usage & Options |
|--------|----------------|
| `useradd devuser` | Create user |
| `passwd devuser` | Set password |
| `usermod -aG developers devuser` | Add user to group |
| `chmod 750 project/` | Restrict access; owner → full, group → read/execute, others → no access |

---

## 🎯 Summary

- Manage users using `useradd`, `passwd`, `userdel`
- Control access using `chmod` and `chown`
- Use groups to manage permissions efficiently
- Always follow the principle of least privilege for security
