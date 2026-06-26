# Security

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner–Intermediate
> **Prerequisites:** Files & Directories, Searching

Many Linux commands can be used to improve security, verify file integrity, and investigate systems. This chapter covers commands commonly used by system administrators and cybersecurity professionals during troubleshooting, incident response, and forensic analysis.

---

## What You'll Learn

* Reviewing command history
* Managing passwords
* Verifying file integrity
* Identifying unknown files
* Viewing file metadata

---

# Security Commands

---

## history

### Purpose

Displays previously executed commands from the current user's shell history.

### Syntax

```bash
history
```

### Examples

Display command history:

```bash
history
```

Display the last 10 commands:

```bash
history | tail
```

Search command history:

```bash
history | grep ssh
```

### Common Uses

* Review previously executed commands.
* Repeat earlier commands.
* Troubleshoot previous actions.

### Cybersecurity Context

Command history can help investigators understand what actions were performed on a system before an incident occurred.

### Related Commands

* `grep`
* `tail`

---

## passwd

### Purpose

Changes the password for the current user or another user (with sufficient privileges).

### Syntax

```bash
passwd
```

Administrator:

```bash
sudo passwd username
```

### Common Uses

* Change your password.
* Reset another user's password.
* Enforce password changes.

### Cybersecurity Context

Strong passwords are one of the most fundamental security controls. Passwords should be unique, difficult to guess, and changed when compromise is suspected.

### Related Commands

* `sudo`

---

## sha256sum

### Purpose

Calculates a SHA-256 cryptographic hash for a file.

### Syntax

```bash
sha256sum FILE
```

### Examples

```bash
sha256sum ubuntu.iso
```

Compare two files:

```bash
sha256sum file1.txt

sha256sum file2.txt
```

### Common Uses

* Verify downloaded files.
* Check file integrity.
* Detect file modifications.

### Cybersecurity Context

SHA-256 is commonly used to verify downloaded software and confirm that evidence or forensic files have not been modified.

### Related Commands

* `md5sum`

---

## md5sum

### Purpose

Calculates an MD5 hash for a file.

### Syntax

```bash
md5sum FILE
```

### Example

```bash
md5sum backup.zip
```

### Common Uses

* Compare files.
* Verify older checksums.

### Cybersecurity Context

MD5 is still encountered in legacy systems, but SHA-256 is preferred because it provides stronger collision resistance.

### Related Commands

* `sha256sum`

---

## file

### Purpose

Identifies the type of a file based on its contents rather than its filename.

### Syntax

```bash
file FILE
```

### Examples

```bash
file script.sh

file image.png

file suspicious.exe
```

### Common Uses

* Identify unknown files.
* Verify downloaded files.
* Confirm executable types.

### Cybersecurity Context

Useful when investigating suspicious files that may use misleading file extensions.

### Related Commands

* `stat`

---

## stat

### Purpose

Displays detailed metadata about a file or directory.

### Syntax

```bash
stat FILE
```

### Example

```bash
stat report.pdf
```

### Common Uses

* View timestamps.
* Check ownership.
* Inspect file size.
* Verify permissions.

### Cybersecurity Context

File metadata is frequently reviewed during forensic investigations to determine when files were created, modified, or accessed.

### Related Commands

* `ls -l`
* `file`

---

# Common Mistakes

| Problem              | Cause                                           |
| -------------------- | ----------------------------------------------- |
| Hashes don't match   | Files are different or have been modified       |
| `Permission denied`  | Insufficient privileges                         |
| File type unexpected | File extension does not match the file contents |

---

# Summary

You should now understand how to review command history, manage passwords, verify file integrity, identify unknown file types, and inspect file metadata. These commands are commonly used by Linux administrators and cybersecurity professionals when securing or investigating systems.

---

# Related Chapters

* Searching
* Permissions
* Storage & Filesystems
* Git
