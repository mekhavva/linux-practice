# 07 - Compression and Archives

## 1. What is Compression?

Compression means reducing the size of data so that it uses less disk space and can be transferred more efficiently.

Compression is commonly used for:

* Backups
* Log files
* File transfers
* Saving disk space
* Server administration
* Cybersecurity investigations

Common compression tools in Linux include:

* `gzip`
* `gunzip`
* `zip`
* `unzip`

---

## 2. Archive vs Compression

An **archive** and a **compressed file** are not exactly the same thing.

### Archive

An archive combines multiple files and directories into one file.

The most common Linux tool for this is:

```bash
tar
```

Example:

```bash
tar -cf backup.tar file1.txt file2.txt
```

This creates one archive containing both files.

### Compression

Compression reduces the size of data.

For example:

```bash
gzip file.txt
```

This creates:

```text
file.txt.gz
```

### Important concept

```text
tar    → creates an archive
gzip   → compresses data
tar.gz → archive + gzip compression
```

---

# 3. tar

`tar` is one of the most commonly used tools for creating and extracting archives in Linux.

The basic syntax is:

```bash
tar [options] archive_name files
```

---

## 4. Creating a TAR archive

To create an archive:

```bash
tar -cf backup.tar file1.txt file2.txt
```

### Options

```text
-c → create an archive
-f → specify the archive filename
```

Example:

```bash
tar -cf backup.tar file1.txt file2.txt
```

This creates:

```text
backup.tar
```

The original files remain unchanged.

---

## 5. Listing the contents of an archive

We can see what is inside an archive without extracting it.

```bash
tar -tf backup.tar
```

### Option

```text
-t → list the contents
```

Example output:

```text
file1.txt
file2.txt
```

This is useful when we want to inspect an archive before extracting it.

---

# 6. Extracting a TAR archive

To extract a TAR archive:

```bash
tar -xf backup.tar
```

### Option

```text
-x → extract
```

The files will be restored to the current directory.

---

# 7. gzip

`gzip` is a compression tool used to reduce the size of files.

Example:

```bash
gzip file.txt
```

The result is:

```text
file.txt.gz
```

The `.gz` extension indicates gzip compression.

---

## 8. Decompressing a GZIP file

To decompress:

```bash
gunzip file.txt.gz
```

The original file will be restored:

```text
file.txt
```

---

# 9. TAR + GZIP

Linux commonly combines `tar` and `gzip`.

The result is usually:

```text
archive.tar.gz
```

To create a compressed TAR archive:

```bash
tar -czf backup.tar.gz file1.txt file2.txt
```

### Options

```text
-c → create
-z → use gzip compression
-f → specify the archive filename
```

Therefore:

```bash
tar -czf backup.tar.gz file1.txt file2.txt
```

means:

> Create an archive containing the files and compress it using gzip.

---

# 10. Listing a TAR.GZ archive

We can inspect the contents without extracting the archive:

```bash
tar -tzf backup.tar.gz
```

### Options

```text
-t → list contents
-z → use gzip
-f → specify the archive
```

Example output:

```text
file1.txt
file2.txt
```

---

# 11. Extracting a TAR.GZ archive

To extract a `.tar.gz` archive:

```bash
tar -xzf backup.tar.gz
```

### Options

```text
-x → extract
-z → gzip
-f → archive filename
```

---

# 12. Extracting to a Specific Directory

We can use the `-C` option to choose the destination directory.

First create a directory:

```bash
mkdir extracted
```

Then:

```bash
tar -xzf backup.tar.gz -C extracted
```

The files will be extracted inside:

```text
extracted/
```

---

# 13. ZIP

ZIP is another common archive and compression format.

To create a ZIP file:

```bash
zip backup.zip file1.txt file2.txt
```

This creates:

```text
backup.zip
```

---

# 14. Unzip

To extract a ZIP archive:

```bash
unzip backup.zip
```

The files will be extracted into the current directory.

ZIP is especially common when exchanging files between Linux and Windows systems.

---

# 15. Practical Example

Create two files:

```bash
touch file1.txt file2.txt
```

Add some content:

```bash
echo "Linux practice" > file1.txt
echo "Cybersecurity practice" > file2.txt
```

Create a TAR archive:

```bash
tar -cf backup.tar file1.txt file2.txt
```

Check its contents:

```bash
tar -tf backup.tar
```

Expected output:

```text
file1.txt
file2.txt
```

Create a compressed TAR archive:

```bash
tar -czf backup.tar.gz file1.txt file2.txt
```

Check its contents:

```bash
tar -tzf backup.tar.gz
```

Expected output:

```text
file1.txt
file2.txt
```

Create a directory for extraction:

```bash
mkdir extracted
```

Extract the compressed archive:

```bash
tar -xzf backup.tar.gz -C extracted
```

Check the extracted files:

```bash
ls extracted
```

Expected output:

```text
file1.txt
file2.txt
```

---

# 16. Real Linux Example

System administrators often create compressed backups of directories.

For example:

```bash
tar -czf logs-backup.tar.gz /var/log
```

This creates a compressed archive containing the system logs.

Compressed backups are easier to store and transfer than many individual files.

---

# 17. Cybersecurity Example

Compressed archives are frequently encountered during security investigations.

For example, an analyst may receive:

```text
incident-logs.tar.gz
```

Before extracting it, the analyst can inspect its contents:

```bash
tar -tzf incident-logs.tar.gz
```

This allows the analyst to see which files are included without extracting them immediately.

The archive can then be extracted:

```bash
mkdir investigation
tar -xzf incident-logs.tar.gz -C investigation
```

The analyst can then investigate the extracted logs.

---

# 18. Why is this useful in Cybersecurity?

Security analysts and system administrators frequently work with:

* Log files
* Backups
* Incident reports
* Evidence files
* Configuration files
* Server data

These files are often transferred as compressed archives.

Being able to inspect and extract these archives is therefore an important Linux skill.

---

# 19. Common Mistakes

### Mistake 1: Confusing TAR and GZIP

`tar` creates an archive.

`gzip` compresses data.

They can be used together:

```bash
tar -czf backup.tar.gz directory/
```

---

### Mistake 2: Forgetting `-f`

Incorrect:

```bash
tar -c backup.tar file1.txt
```

Correct:

```bash
tar -cf backup.tar file1.txt
```

The `-f` option tells `tar` which archive file to use.

---

### Mistake 3: Extracting without checking the contents

Instead of immediately extracting:

```bash
tar -xzf archive.tar.gz
```

we can first inspect the archive:

```bash
tar -tzf archive.tar.gz
```

This is especially useful when dealing with archives received from unknown sources.

---

# 20. Important TAR Options

| Option | Meaning                     |
| ------ | --------------------------- |
| `-c`   | Create archive              |
| `-x`   | Extract archive             |
| `-t`   | List contents               |
| `-z`   | Use gzip                    |
| `-f`   | Specify archive filename    |
| `-C`   | Change extraction directory |

---

# 21. Command Summary

### Create TAR

```bash
tar -cf archive.tar files
```

### List TAR

```bash
tar -tf archive.tar
```

### Extract TAR

```bash
tar -xf archive.tar
```

### Create TAR.GZ

```bash
tar -czf archive.tar.gz files
```

### List TAR.GZ

```bash
tar -tzf archive.tar.gz
```

### Extract TAR.GZ

```bash
tar -xzf archive.tar.gz
```

### Extract to a specific directory

```bash
tar -xzf archive.tar.gz -C directory/
```

### GZIP

```bash
gzip file
```

### GUNZIP

```bash
gunzip file.gz
```

### ZIP

```bash
zip archive.zip files
```

### UNZIP

```bash
unzip archive.zip
```

---

# 22. Interview Questions

### What is the difference between TAR and GZIP?

`tar` is mainly used to create archives, while `gzip` is used to compress data.

They are commonly combined to create `.tar.gz` files.

### What does `.tar.gz` mean?

It is a TAR archive compressed using GZIP.

### How do you list the contents of a TAR.GZ file without extracting it?

```bash
tar -tzf archive.tar.gz
```

### How do you extract a TAR.GZ file?

```bash
tar -xzf archive.tar.gz
```

### Why are compressed archives useful?

They reduce storage requirements and make transferring multiple files easier.

---

# 23. Summary

The main concepts learned in this section are:

```text
tar    → archive files and directories
gzip   → compress data
gunzip → decompress GZIP files
zip    → create ZIP archives
unzip  → extract ZIP archives
```

The most important Linux format to remember is:

```text
.tar.gz
```

because it represents:

```text
TAR archive + GZIP compression
```

Important commands:

```bash
tar -cf archive.tar files
tar -tf archive.tar
tar -xf archive.tar

tar -czf archive.tar.gz files
tar -tzf archive.tar.gz
tar -xzf archive.tar.gz
```

These commands are commonly used in Linux administration, backups, server management, DevOps, and cybersecurity.
