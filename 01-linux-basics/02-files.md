# Linux File Management

## Objective

Learn how to create, copy, move, rename, delete, and inspect files and directories in Linux.

---

# What is File Management?

File management is the process of creating, organizing, copying, moving, renaming, viewing, and deleting files and directories.

---

# Commands

## 1. touch

### Purpose

Create a new empty file.

### Syntax

touch filename
### My Practice

touch notes.txt
### Output

```no output

```

### Notes

Creates an empty file if it does not already exist.

---

## 2. mkdir

### Purpose

Create a new directory.

### Syntax

mkdir directory_name
### My Practice

mkdir Projects
### Output

```no output

```

---

## 3. rmdir

### Purpose

Remove an empty directory.

### Syntax

rmdir directory_name
### My Practice

rmdir Projects
### Output

```no output

```

### Notes

Works only if the directory is empty.

---

## 4. cp

### Purpose

Copy files.

### Syntax

cp source destination
### My Practice

cp notes.txt copy.txt
### Output

```no output

```

---

## 5. cp -r

### Purpose

Copy directories recursively.

### Syntax

cp -r Folder Backup
### My Practice

cp -r LinuxLab LinuxLabBackup
### Output

```no output

```

---

## 6. mv

### Purpose

Move or rename files.

### Syntax

mv old_name.txt new_name.txt
### My Practice

mv copy.txt backup.txt
### Output

```text

```

---

## 7. rm

### Purpose

Delete files.

### Syntax

rm filename
### My Practice

rm backup.txt
### Output

```no output

```

### Warning

Deleted files cannot be recovered easily.

---

## 8. rm -r

### Purpose

Delete directories and their contents.

### Syntax

rm -r directory_name
### My Practice

rm -r LinuxLabBackup
---

## 9. cat

### Purpose

Display file contents.

### Syntax

cat filename
### My Practice

cat notes.txt
### Output

```learning linux is important for cybersecurity 
this is my first linux projrct 
practice every day 

```

---

## 10. head

### Purpose

Display the first lines of a file.

### Syntax

head filename
### My Practice

head notes.txt
### Output

```no output

```

---

## 11. tail

### Purpose

Display the last lines of a file.

### Syntax

tail filename
### My Practice

tail notes.txt
### Output

```no output


```

---

## 12. less

### Purpose

View large files page by page.

### Syntax

less filename
### My Practice

less notes.txt
### Output

```text

```

---

## 13. file

### Purpose

Determine the file type.

### Syntax

file filename
### My Practice

file notes.txt
### Output

```notes.txt: ASCII text


```

---

## 14. stat

### Purpose

Display detailed file information.

### Syntax

stat filename
### My Practice

stat notes.txt
### Output

```
  File: notes.txt
  size: 99        	Blocks: 8          IO Block: 4096   regular file
Device: 8,2	Inode: 396820      Links: 1
Access: (0664/-rw-rw-r--)  Uid: ( 1000/   havva)   Gid: ( 1000/   havva)
Access: 2026-07-14 15:49:55.570157780 +0100
Modify: 2026-07-14 15:49:45.490096360 +0100
Change: 2026-07-14 15:49:45.490096360 +0100
 Birth: 2026-07-14 15:02:56.314292881 +0100


```

---

## 15. wc

### Purpose

Count lines, words, and characters.

### Syntax

wc filename
### My Practice

wc notes.txt
### Output

```
0 0 0 backup.txt


```

---

# Common Errors

## Error

rm: cannot remove 'notes.txt': No such file or directory
### Reason

The file does not exist.

### Solution

Use

ls
to verify the filename.

---

# Summary

After completing this lesson I can:

- Create files.
- Create directories.
- Copy files and folders.
- Move and rename files.
- Delete files and directories.
- Read file contents.
- View file information.
- Count words and lines.
