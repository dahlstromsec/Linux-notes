# Permissions

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner
> **Prerequisites:** Navigation, Files & Directories

Linux permissions determine who can read, write, or execute files and directories. Understanding permissions is one of the most important Linux skills, as they form the foundation of system security and access control.

---

## What You'll Learn

* Understanding Linux permissions
* File ownership
* Changing permissions
* Managing file ownership
* Secure default permissions

---

# Understanding Permissions

Every file and directory has three permission groups:

| Group      | Description                   |
| ---------- | ----------------------------- |
| User (u)   | Owner of the file             |
| Group (g)  | Members of the assigned group |
| Others (o) | Everyone else                 |

Example:

```text
-rwxr-xr--
```

| Symbol | Meaning                |
| ------ | ---------------------- |
| r      | Read                   |
| w      | Write                  |
| x      | Execute                |
| -      | Permission not granted |

---

## chmod

### Purpose

Changes file or directory permissions.

### Syntax

```bash
chmod MODE FILE
```

### Examples

```bash
chmod 755 script.sh

chmod 644 notes.txt

chmod +x script.sh
```

### Common Uses

* Make scripts executable.
* Restrict access to files.
* Set secure permissions.

### Cybersecurity Context

Proper permissions help prevent unauthorized access and accidental modification of sensitive files.

### Related Commands

* `chown`
* `stat`
* `ls -l`

---

## chown

### Purpose

Changes the owner of a file or directory.

### Syntax

```bash
chown USER FILE
```

### Examples

```bash
sudo chown christoffer report.txt

sudo chown root script.sh
```

### Common Uses

* Transfer ownership.
* Correct file ownership.
* Manage shared systems.

### Cybersecurity Context

Incorrect ownership can expose sensitive information or prevent applications from functioning correctly.

### Related Commands

* `chmod`
* `chgrp`

---

## chgrp

### Purpose

Changes the group ownership of a file or directory.

### Syntax

```bash
chgrp GROUP FILE
```

### Example

```bash
sudo chgrp developers app.py
```

### Common Uses

* Share files between users.
* Configure project directories.

### Cybersecurity Context

Using groups correctly supports the principle of least privilege.

### Related Commands

* `chmod`
* `chown`

---

## umask

### Purpose

Sets the default permissions for newly created files and directories.

### Syntax

```bash
umask

umask 022
```

### Common Uses

* Configure default permissions.
* Improve system security.

### Cybersecurity Context

A secure umask helps prevent newly created files from being accessible to unauthorized users.

### Related Commands

* `chmod`

---

# Common Mistakes

| Problem                  | Cause                                      |
| ------------------------ | ------------------------------------------ |
| Permission denied        | Missing read, write, or execute permission |
| Script won't run         | Execute permission not set                 |
| Users can't access files | Incorrect ownership or group               |

---

# Summary

You should now understand how Linux controls access to files and directories, how to modify permissions, and how ownership affects system security.

---

# Related Chapters

* Navigation
* Files & Directories
* Users
* Security
