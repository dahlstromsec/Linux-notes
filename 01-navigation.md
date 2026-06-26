# Navigation

Navigation commands are used to move around the Linux file system and determine your current working location.

Understanding these commands is essential before working with files, directories, or system administration tasks.

---

## pwd

### Purpose

Displays the absolute path of the current working directory.

---

### Syntax

```bash
pwd
```

---

### Example

```bash
pwd
```

Example output:

```text
/home/christoffer/Documents
```

---

### Common Uses

- Verify your current location in the file system.
- Avoid running commands in the wrong directory.
- Confirm where files will be created or modified.

---

### Cybersecurity Context

Before searching log files, editing configuration files, or running scripts, it is good practice to verify your current working directory. This helps prevent accidental changes to the wrong location.

---

### Related Commands

- `ls`
- `cd`

---

## ls

### Purpose

Lists the files and directories in the current working directory.

---

### Syntax

```bash
ls
```

---

### Example

```bash
ls
```

Example output:

```text
Documents  Downloads  Pictures  Music
```

---

### Common Uses

- View the contents of the current directory.
- Confirm that a file or directory exists.
- Quickly inspect the structure of a directory.

---

### Cybersecurity Context

The `ls` command is frequently used when navigating Linux systems during security assessments, log analysis, incident response, and system administration. It helps verify the contents of directories before viewing, modifying, or executing files.

---

### Related Commands

- `pwd`
- `cd`
- `find`

---

## ls -l

### Purpose

Displays files and directories in a detailed list format.

---

### Syntax

```bash
ls -l
```

---

### Example

```bash
ls -l
```

Example output:

```text
drwxr-xr-x 2 christoffer users 4096 Jul 30 12:15 Documents
-rw-r--r-- 1 christoffer users 842 Jul 29 20:48 notes.txt
```

---

### Common Uses

- View file permissions.
- Check file ownership.
- See file sizes and modification dates.
- Display detailed information about files and directories.

---

### Cybersecurity Context

The `ls -l` command is commonly used to inspect file permissions and ownership. This helps identify files that may have incorrect permissions or unexpected owners during security investigations and system administration.

---

### Related Commands

- `ls`
- `chmod`
- `chown`
- `stat`
