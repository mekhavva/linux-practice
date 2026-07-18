# Linux Users and Groups

## Objective

Learn how Linux manages users and groups, identify the current user, understand sudo, and view user information.

---

# What are Users?

Linux is a multi-user operating system.

Each user has:

- Username
- Password
- Home directory
- Permissions
- Groups

---

# Commands

## 1. whoami

### Purpose

Display the current logged-in user.

### Syntax

whoami

### My Practice

whoami

### Output

``` havva```

### Notes

Shows the current username.

---

## 2. id

### Purpose

Display user ID (UID), group ID (GID), and groups.

### Syntax

id

### My Practice

id

### Output
``` uid=1000(havva) gid=1000(havva) groups=1000(havva),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),100(users),111(lpadmin),114(lxd)

```

### Notes

Useful for checking your identity and permissions.

---

## 3. who

### Purpose

Display users currently logged into the system.

### Syntax

who

### My Practice

who

### Output

``` no output```

---

## 4. groups

### Purpose

Display groups of the current user.

### Syntax

groups

### My Practice

groups

### Output
```havva adm cdrom sudo dip plugdev users lpadmin lxd
```


---

## 5. sudo -l

### Purpose

Display commands the current user is allowed to run with sudo.

### Syntax

sudo -l

### My Practice

sudo -l

### Output
``` User havva may run the following commands on havva-VirtualBox:
    (ALL : ALL) ALL
```


---

## 6. passwd

### Purpose

Change the current user's password.

### Syntax

passwd

### Notes

Do not run unless you want to change your password.

---

## 7. su

### Purpose

Switch to another user.

### Syntax

su username

### Example

su root

### Notes

Requires the target user's password.

---

## 8. adduser

### Purpose

Create a new user.

### Syntax

sudo adduser username

### Example

sudo adduser student

### Notes

Not executed in this project.

---

## 9. userdel

### Purpose

Delete a user.

### Syntax

sudo userdel username

### Example

sudo userdel student

### Notes

Not executed in this project.

---

## 10. usermod

### Purpose

Modify a user account.

### Example

sudo usermod -aG sudo student

### Notes

Adds the user to the sudo group.

---

# Important Concepts

## UID

User ID.

Every user has a unique identifier.

---

## GID

Group ID.

Every group has its own identifier.

---

## Home Directory

Example:

/home/havva

Each user normally has a personal home directory.

---

## Root User

The administrator account.

Username:

root

Root has full control over the system.

---

## Sudo

Allows authorized users to execute administrative commands without logging in directly as root.

---

# Common Errors

Example

sudo: command not found

Reason

sudo is not installed.

---

Example

Permission denied

Reason

The current user does not have permission.

---

# Summary

After completing this lesson I can:

- Identify the current user.
- Understand UID and GID.
- Display groups.
- Understand sudo.
- Understand root.
- Know how users are created and deleted.
