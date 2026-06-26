# Permissions

Linux permissions control who can read, write, or execute files and directories.

---

## chmod

### Purpose

Changes file or directory permissions.

### Syntax

```bash
chmod MODE FILE
```

### Example

```bash
chmod 755 script.sh
chmod +x script.sh
```

### Common Uses

- Make scripts executable.
- Restrict file access.
- Set correct permissions.

### Cybersecurity Context

Proper permissions reduce the risk of unauthorized access or accidental modification.

### Related Commands

- `chown`
- `stat`
- `ls -l`

---

## chown

### Purpose

Changes the owner of a file or directory.

### Syntax

```bash
chown USER FILE
```

### Example

```bash
sudo chown alice report.txt
```

### Common Uses

- Transfer ownership.
- Correct file ownership after copying.

### Cybersecurity Context

Incorrect ownership can expose sensitive files or break security controls.

### Related Commands

- `chmod`
- `chgrp`

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

- Share files within a group.
- Manage collaborative access.

### Cybersecurity Context

Useful for implementing least-privilege access.

### Related Commands

- `chmod`
- `chown`

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

- Define secure default permissions.

### Cybersecurity Context

A secure umask helps prevent new files from being overly permissive.

### Related Commands

- `chmod`
