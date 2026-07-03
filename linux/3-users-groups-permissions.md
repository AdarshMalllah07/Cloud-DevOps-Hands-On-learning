# Linux Fundamentals - Module 3

# Users, Groups & Permissions

## Learning Objectives

After completing this module, you will understand:

- Linux Users
- Root User
- Normal User
- System Users
- UID & GID
- Groups
- File Ownership
- Linux Permissions
- chmod
- chown
- chgrp
- sudo
- /etc/passwd
- /etc/shadow
- Real-world Cloud Examples
- Hands-on Practice
- Interview Questions

---

# 1. Why do Users exist?

Imagine a production server used by multiple people:

- DevOps Engineer
- Backend Developer
- Frontend Developer
- Database Administrator
- QA Engineer

If everyone logged in as **root**, anyone could:

- Delete system files
- Stop services
- Remove databases
- Shut down the server

To prevent this, Linux supports multiple users with different permission levels.

---

# 2. Types of Users

## Root User

The root user is the administrator of the Linux system.

Characteristics:

- UID = 0
- Full system access
- Can install software
- Can create/delete users
- Can modify any file
- Can start/stop services

Check current user:

```bash
whoami
```

---

## Normal User

A normal user has limited permissions.

Examples:

- adarsh
- ubuntu
- developer
- ec2-user

Normal users cannot modify critical system files unless they use `sudo`.

---

## System Users

These accounts are created for running services.

Examples:

- www-data
- mysql
- postgres
- nginx
- systemd-network

These users usually cannot log in.

Purpose:

Run services with minimum privileges for better security.

---

# 3. User ID (UID)

Every Linux user has a unique numeric ID.

Example:

root → UID 0

adarsh → UID 1000

ubuntu → UID 1001

Check UID:

```bash
id
```

Example Output:

```
uid=1000(adarsh)
gid=1000(adarsh)
groups=1000(adarsh),27(sudo)
```

---

# 4. Groups

A Group is a collection of users.

Instead of giving permissions to each user individually, permissions are assigned to the group.

Example:

developers

devops

docker

sudo

finance

---

# Real Example

Suppose:

```
/var/www/html
```

Owner:

```
www-data
```

Group:

```
developers
```

Any user belonging to the **developers** group can update website files.

---

# 5. User Information

Linux stores user information inside:

```
/etc/passwd
```

View file:

```bash
cat /etc/passwd
```

Example:

```
adarsh:x:1000:1000:Adarsh:/home/adarsh:/bin/bash
```

Meaning:

| Field | Description |
|--------|-------------|
| adarsh | Username |
| x | Password placeholder |
| 1000 | UID |
| 1000 | GID |
| Adarsh | User description |
| /home/adarsh | Home Directory |
| /bin/bash | Default Shell |

---

# 6. Password Storage

Passwords are NOT stored inside `/etc/passwd`.

Instead they are stored securely inside:

```
/etc/shadow
```

Only the root user can access this file.

---

# 7. Home Directory

Each normal user gets a personal directory.

Example:

```
/home/adarsh
```

Check your home directory:

```bash
echo $HOME
```

---

# 8. sudo

A normal user cannot perform administrative tasks directly.

Example:

```bash
apt update
```

Permission denied.

Using:

```bash
sudo apt update
```

temporarily grants administrator privileges.

sudo = Super User Do

---

# 9. File Ownership

Every file has:

- Owner
- Group

Check ownership:

```bash
ls -l
```

Example:

```
-rw-r--r-- 1 adarsh developers 1200 notes.txt
```

Owner:

adarsh

Group:

developers

---

# 10. Linux Permissions

Permission format:

```
-rwxr-xr--
```

Split into:

```
rwx | r-x | r--
```

Meaning:

Owner

Group

Others

---

Permission values:

Read = 4

Write = 2

Execute = 1

Examples:

| Number | Permission |
|----------|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 0 | --- |

---

# 11. chmod

Change file permissions.

Example:

```bash
chmod 755 deploy.sh
```

Meaning:

Owner → rwx

Group → r-x

Others → r-x

Grant execute permission:

```bash
chmod +x deploy.sh
```

Remove execute permission:

```bash
chmod -x deploy.sh
```

---

# 12. chown

Change file owner.

```bash
sudo chown ubuntu file.txt
```

Change owner and group:

```bash
sudo chown ubuntu:developers file.txt
```

---

# 13. chgrp

Change group ownership.

```bash
sudo chgrp developers file.txt
```

---

# 14. Cloud Example

Suppose Nginx serves your application.

Website files:

```
/var/www/html
```

Service user:

```
www-data
```

If ownership or permissions are incorrect:

Users receive:

```
403 Forbidden
```

This is one of the most common production issues.

---

# 15. Hands-on Lab

Check current user:

```bash
whoami
```

User details:

```bash
id
```

Groups:

```bash
groups
```

Home directory:

```bash
echo $HOME
```

View user database:

```bash
cat /etc/passwd
```

Create a file:

```bash
touch demo.txt
```

Check permissions:

```bash
ls -l demo.txt
```

Make executable:

```bash
chmod +x demo.txt
```

Set permission:

```bash
chmod 644 demo.txt
```

---

# 16. Interview Questions

1. Difference between Root User and Normal User.
2. What is UID?
3. What is GID?
4. Difference between User and Group.
5. Purpose of `/etc/passwd`.
6. Why is `/etc/shadow` protected?
7. Explain Linux permissions.
8. Difference between chmod, chown and chgrp.
9. What does 755 mean?
10. Why shouldn't services run as root?

---

# 17. Key Takeaways

- Root user has UID 0.
- Every user has a unique UID.
- Groups simplify permission management.
- File ownership consists of Owner and Group.
- Linux permissions control access using Read, Write and Execute.
- sudo provides temporary administrator privileges.
- Passwords are stored in `/etc/shadow`.
- Services like Nginx and PostgreSQL run using dedicated system users.

---

# Module Completion Checklist

- [ ] Understand Root User
- [ ] Understand Normal Users
- [ ] Understand System Users
- [ ] Explain UID & GID
- [ ] Understand Groups
- [ ] Explain Linux Permissions
- [ ] Use chmod confidently
- [ ] Use chown confidently
- [ ] Use chgrp confidently
- [ ] Complete Hands-on Lab
- [ ] Answer Interview Questions