# Linux Permissions

## Objective

Learn how Linux file permissions work and how to modify them using chmod and chown.

---

# What are Linux Permissions?

Linux uses permissions to control who can read, write, or execute files and directories.

There are three types of users:

- Owner (u)
- Group (g)
- Others (o)

There are three permission types:

- Read (r)
- Write (w)
- Execute (x)

---

# Commands

## 1. ls -l

### Purpose

Display file permissions.

### Syntax

ls -l
### My Practice

ls -l
### Output

```total 20
-rw-rw-r-- 1 havva havva 6518 Jul 14 14:55 01-navigation.md
-rw-rw-r-- 1 havva havva 3628 Jul 14 23:37 02-files.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 03-permissions.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 04-users.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 05-processes.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 06-search.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 07-compression.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 08-package-manager.md
-rw-rw-r-- 1 havva havva    0 Jul 14 15:03 backup.txt
-rw-rw-r-- 1 havva havva   99 Jul 14 15:49 notes.txt
-rw-rw-r-- 1 havva havva 1889 Jul 15 20:51 permissions.md


```

---

## 2. chmod

### Purpose

Change file permissions.

### Syntax

chmod permissions filename
### My Practice

chmod 755 notes.txt
ls -l notes.txt
### Output

```-rwxr-xr-x 1 havva havva 99 Jul 14 15:49 notes.txt


```

### Notes

755 means:

- Owner = rwx
- Group = r-x
- Others = r-x

---

## 3. chmod using letters

### Syntax

chmod u+x notes.txt
### Purpose

Give execute permission to the owner.

### Output

```rwxr-xr-x 1 havva havva 99 Jul 14 15:49 notes.txt


```

---

## 4. chmod remove permission

chmod g-w notes.txt
### Purpose

Remove write permission from the group.

### Output

```rwxr-xr-x 1 havva havva 99 Jul 14 15:49 notes.txt


```

---

## 5. chown

### Purpose

Change file owner.

### Syntax

sudo chown username filename
### Example

sudo chown havva notes.txt
### Notes

Requires sudo privileges.

---

## 6. chgrp

### Purpose

Change file group.

### Syntax

sudo chgrp groupname filename
### Example

sudo chgrp havva notes.txt
---

# Understanding Permission Numbers

| Number | Permission |
|---------|------------|
| 7 | rwx |
| 6 | rw- |
| 5 | r-x |
| 4 | r-- |
| 3 | -wx |
| 2 | -w- |
| 1 | --x |
| 0 | --- |

---

# Common Errors

Example

chmod: cannot access 'notes.txt': No such file or directory
Reason

Wrong filename.

Solution

Use:

ls
to verify the file exists.

---

# Summary

After completing this lesson I can:

- Read Linux permissions.
- Change permissions using chmod.
- Understand numeric permissions.
- Change file owner.
- Change file group.
