# Navigation

> **Estimated Reading Time:** 5–10 minutes
> **Difficulty:** Beginner
> **Prerequisites:** None

Navigation is one of the first Linux skills you'll use. Before creating files, searching logs, editing configurations, or running scripts, you first need to know where you are in the file system and how to move between directories.

Understanding navigation commands builds the foundation for almost every other Linux task.

---

## What You'll Learn

* Understanding the Linux file system
* Absolute vs. relative paths
* Viewing the current working directory
* Listing directory contents
* Navigating between directories
* Viewing hidden files

---

# Linux File System Overview

Linux uses a hierarchical directory structure that starts at the root directory (`/`).

```text
/

├── home
│   └── user
│       ├── Desktop
│       ├── Documents
│       ├── Downloads
│       └── Pictures
│
├── etc
├── var
├── usr
├── opt
└── tmp
```

Some common directories include:

| Directory | Purpose                              |
| --------- | ------------------------------------ |
| `/`       | Root directory                       |
| `/home`   | User home directories                |
| `/etc`    | System configuration files           |
| `/var`    | Logs and variable data               |
| `/usr`    | Installed applications and utilities |
| `/tmp`    | Temporary files                      |

---

# Absolute vs. Relative Paths

Linux allows you to reference files and directories using either **absolute** or **relative** paths.

### Absolute Path

Starts from the root directory (`/`).

Example:

```bash
/home/user/Documents
```

### Relative Path

Starts from your current working directory.

Examples:

```bash
Documents

../Downloads

../../Desktop
```

Useful shortcuts:

| Shortcut | Meaning           |
| -------- | ----------------- |
| `.`      | Current directory |
| `..`     | Parent directory  |
| `~`      | Home directory    |
| `/`      | Root directory    |

---

# Command Reference

---

## pwd

### Purpose

Displays the absolute path of the current working directory.

### Syntax

```bash
pwd
```

### Example

```bash
pwd
```

Output

```text
/home/user/Documents
```

### Common Uses

* Verify your current location.
* Confirm where commands will execute.
* Avoid working in the wrong directory.

### Cybersecurity Context

Before searching log files, editing configuration files, or running scripts, it is good practice to verify your current working directory.

### Related Commands

* `ls`
* `cd`

---

## ls

### Purpose

Lists files and directories within a directory.

### Syntax

```bash
ls [OPTION]... [DIRECTORY]
```

### Common Options

| Option | Description                  |
| ------ | ---------------------------- |
| `-l`   | Long listing format          |
| `-a`   | Show hidden files            |
| `-h`   | Human-readable file sizes    |
| `-R`   | List directories recursively |

### Examples

```bash
ls

ls -la

ls -lh

ls -R
```

### Common Uses

* View directory contents.
* Check if files exist.
* Display hidden files.
* View file permissions.

### Cybersecurity Context

Frequently used during investigations to inspect directories before analyzing logs, scripts, or suspicious files.

### Related Commands

* `pwd`
* `cd`
* `find`

---

## cd

### Purpose

Changes the current working directory.

### Syntax

```bash
cd DIRECTORY
```

### Examples

```bash
cd Documents

cd ..

cd ~

cd /

cd -
```

### Common Uses

* Navigate between directories.
* Return to the home directory.
* Move to the previous directory.
* Access system folders.

### Cybersecurity Context

Security analysts constantly change directories when reviewing logs, investigating files, or navigating Linux servers remotely.

### Related Commands

* `pwd`
* `ls`

---

# Navigation Tips

* Press **Tab** to autocomplete files and directories.
* Press **↑** to cycle through previous commands.
* Use `history` to display previous commands.
* Press **Ctrl + L** to clear the terminal.

---

# Common Mistakes

| Problem                     | Cause                      |
| --------------------------- | -------------------------- |
| `No such file or directory` | Incorrect path or spelling |
| `Permission denied`         | Insufficient permissions   |
| Wrong directory             | Forgot to check with `pwd` |

---

# Summary

You should now understand how to determine your current location, list directory contents, navigate between directories, and recognize the difference between absolute and relative paths.

These commands form the foundation for almost every Linux task you'll perform throughout your cybersecurity journey.

---

# Related Chapters

* Files & Directories
* Searching
* Permissions
