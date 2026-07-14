
# Linux Navigation

## Objective

Learn how to navigate efficiently through the Linux file system using terminal commands.

---

# What is Linux Navigation?

Linux Navigation is the process of moving between directories and locating files using terminal commands.

---

# Commands

## 1. pwd

### Purpose

Display the absolute path of the current working directory.

### Syntax

pwd
### My Practice

pwd
### Output

```/home/havva/Linux-Pratice/01-linux-basics


```

### Notes

- Shows your current location.
- Safe command (does not modify anything).

---

## 2. ls

### Purpose

List files and directories.

### Syntax

ls
### My Practice

ls
### Output

```01-navigation.md  02-files.md  03-permissions.md  04-users.md  05-processes.md  06-search.md  07-compression.md  08-package-manager.md

```

### Notes

Displays visible files only.

---

## 3. ls -l

### Purpose

Display files in long format.

### Syntax

ls -l
### My Practice

ls -l
### Output

```total 4
-rw-rw-r-- 1 havva havva 3057 Jul 14 14:34 01-navigation.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 02-files.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 03-permissions.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 04-users.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 05-processes.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 06-search.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 07-compression.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 08-package-manager.md


```

### Notes

Shows:

- File permissions
- Owner
- Group
- Size
- Modification date

---

## 4. ls -a

### Purpose

Show hidden files.

### Syntax

ls -a
### My Practice

ls -a
### Output

```.  ..  01-navigation.md  02-files.md  03-permissions.md  04-users.md  05-processes.md  06-search.md  07-compression.md  08-package-manager.md


```

### Notes

Hidden files begin with a dot (.).

---

## 5. ls -la

### Purpose

Show all files in long format.

### Syntax

ls -la
### My Practice

ls -la
### Output

```
total 12
drwxrwxr-x 2 havva havva 4096 Jul 14 14:36 .
drwxrwxr-x 4 havva havva 4096 Jul 12 01:40 ..
-rw-rw-r-- 1 havva havva 3667 Jul 14 14:36 01-navigation.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 02-files.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 03-permissions.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 04-users.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 05-processes.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 06-search.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 07-compression.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 08-package-manager.md

```

---

## 6. ls -lh

### Purpose

Display file sizes in a human-readable format.

### Syntax

ls -lh
### My Practice

ls -lh
### Output

```total 8.0K
-rw-rw-r-- 1 havva havva 4.2K Jul 14 14:37 01-navigation.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 02-files.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 03-permissions.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:42 04-users.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 05-processes.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:43 06-search.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 07-compression.md
-rw-rw-r-- 1 havva havva    0 Jul 12 01:44 08-package-manager.md


```

---

## 7. cd

### Purpose

Change the current directory.

### Syntax

cd directory_name
### Example

cd Documents
### My Practice

cd Documents
pwd
### Output

```~$ 


```

---

## 8. cd ..

### Purpose

Move one directory up.

### Syntax

cd ..
### My Practice

cd ..
pwd
### Output

```havva@havva-VirtualBox:~/Linux-Pratice$ 


```

---

## 9. cd ~

### Purpose

Return to the home directory.

### Syntax

cd ~
### My Practice

cd ~
pwd
### Output

```
~$ 



```

---

## 10. cd -

### Purpose

Return to the previous directory.

### Syntax

cd -
### My Practice

cd -
### Output

```/home/havva/Linux-Pratice/01-linux-basics


```

---

## 11. clear

### Purpose

Clear the terminal screen.

### Syntax

clear
### Notes

Removes previous terminal output from the screen.

---

## 12. history

### Purpose

Display previously executed commands.

### Syntax

history
### My Practice

history
### Output

```    1  sudo apt update\
    2  sudo apt install git 
    3  git --version
    4  git config --global user.name "havva"
    5  git config --global user.email "GitHub_mekhavva@gmail.com"
    6  Done
    7  git config --global user.email "mekhavva@gmail.com"
    8  ssh-keygen -t ed25519 -C "mekhavva@gmail.com"
    9  cat ~/.ssh /id_ed25519.pub
   10  cat ~/.ssh/id_ed25519.pub
   11  sudo apt instsall
   12  virtualbox-guest-utilis 
   13  sudo apt install 
   14  sudo apt install
   15  virtualbox-guest-utils
   16  apt search virtualbox-guest
   17  sudo apt install vurtualbox-guest-utils 
   18  sudo apt install 
   19  virtualbox-guest-utils
   20  sudo apt install virtualbox-guest-utils  virtualbox-guest-x11 
   21  sudo reboot
   22  sudo systemctl reboot -i
   23  cd ~ls
   24  cd~ 
   25  cd ~ ls
   26  cd ~
   27  ls
   28  cd linux-pratice
   29  pwd
   30  ls
   31  find ~ -type d -name "Linux*"
   32  cd Linux-Pratice
   33  ls
   34  pwd
   35  ls -la
   36  cd 01-linux-basics
   37  ls
   38  01-navigation.md 
   39  nano 01-navigation.md 
   40  pwd
   41  nano 01-navigation.md 
   42  ls
   43  nano 01-navigation.md 
   44  ls -l
   45  nano 01-navigation.md 
   46  ls -a
   47  nano 01-navigation.md 
   48  ls -la
   49  nano 01-navigation.md 
   50  ls -lh
   51  nano 01-navigation.md 
   52  cd ..
   53  nano 01-navigation.md 
   54  cd 01-linux-basics
   55  nano 01-navigation.md 
   56  cd
   57  cd 01-linux-basics
   58  pwd
   59  ls
   60  cd ..
   61  find ~ -type d -name "Linux*"
   62  cd linux-pratice
   63  cd ~~/Linux-Pratice/01-linux-basics
   64  cd ~/Linux-Pratice/01-linux-basics
   65  nano 01-navigation.md 
   66  cd ~
   67  pwd
   68  cd -
   69  pwd
   70  history


```

---

# Keyboard Shortcuts

| Shortcut | Description |
|----------|-------------|
| Tab | Auto-complete commands and file names |
| Ctrl + C | Stop the current command |
| Ctrl + L | Clear the terminal |
| ↑ | Previous command |
| ↓ | Next command |

---

# Common Errors

## Error

bash: cd: Desktop: No such file or directory
Reason:

The directory does not exist.

Solution:

Use

ls
to verify the directory name.

---

# Summary

After completing this lesson I can:

- Identify my current directory.
- Navigate between directories.
- Display files.
- Display hidden files.
- Display detailed file information.
- Return to the previous directory.
- Return to the home directory.
- View command history.
