# Searching

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner
> **Prerequisites:** Navigation, Files & Directories

Searching is one of the most valuable Linux skills. Whether you're looking for a specific file, investigating log files, or searching for text inside configuration files, these commands help you quickly locate the information you need.

---

## What You'll Learn

* Finding files and directories
* Locating installed programs
* Searching text within files
* Sorting and filtering output
* Counting lines, words, and characters

---

# Searching Commands

---

## find

### Purpose

Searches for files and directories based on name, type, size, permissions, and many other attributes.

### Syntax

```bash
find PATH [OPTIONS]
```

### Examples

```bash
find ~/Downloads -name "*.pdf"

find . -type f

find /var/log -name "*.log"
```

### Common Uses

* Locate files.
* Search directories recursively.
* Find files matching specific patterns.

### Cybersecurity Context

Useful for locating log files, configuration files, certificates, or suspicious files during investigations.

### Related Commands

* `locate`
* `which`

---

## locate

### Purpose

Quickly searches for files using an indexed database.

### Syntax

```bash
locate FILE
```

### Examples

```bash
locate ssh_config

locate passwd
```

### Common Uses

* Quickly locate known files.
* Search large systems efficiently.

### Cybersecurity Context

Useful when quickly locating configuration files or tools on a system.

### Related Commands

* `find`

---

## which

### Purpose

Displays the location of an executable command.

### Syntax

```bash
which COMMAND
```

### Examples

```bash
which python3

which ssh

which git
```

### Common Uses

* Verify software installation.
* Locate executable files.

### Cybersecurity Context

Helpful when verifying which executable will run, especially on systems with multiple versions installed.

### Related Commands

* `whereis`

---

## whereis

### Purpose

Locates binaries, source files, and manual pages for a command.

### Syntax

```bash
whereis COMMAND
```

### Example

```bash
whereis python3
```

### Common Uses

* Locate binaries.
* Find documentation.

### Cybersecurity Context

Useful when investigating installed software and system binaries.

### Related Commands

* `which`

---

## grep

### Purpose

Searches files or command output for matching text.

### Syntax

```bash
grep "PATTERN" FILE
```

### Examples

```bash
grep "Failed password" /var/log/auth.log

grep "error" application.log
```

### Common Uses

* Search logs.
* Find keywords.
* Filter command output.

### Cybersecurity Context

SOC analysts frequently use `grep` to search logs for failed logins, suspicious IP addresses, or indicators of compromise.

### Related Commands

* `grep -r`
* `less`

---

## grep -r

### Purpose

Searches recursively through directories.

### Syntax

```bash
grep -r "PATTERN" DIRECTORY
```

### Examples

```bash
grep -r "password" .

grep -r "TODO" ~/Projects
```

### Common Uses

* Search source code.
* Search configuration files.
* Search entire projects.

### Cybersecurity Context

Useful during threat hunting or code reviews when searching for secrets, API keys, or suspicious strings.

### Related Commands

* `grep`

---

## sort

### Purpose

Sorts lines alphabetically or numerically.

### Syntax

```bash
sort FILE
```

### Example

```bash
sort users.txt
```

### Common Uses

* Organize data.
* Prepare output for further processing.

### Cybersecurity Context

Often combined with other commands to analyze logs.

### Related Commands

* `uniq`

---

## uniq

### Purpose

Removes duplicate consecutive lines.

### Syntax

```bash
uniq FILE
```

### Example

```bash
sort users.txt | uniq
```

### Common Uses

* Remove duplicates.
* Count unique values.

### Cybersecurity Context

Useful when summarizing repeated log entries.

### Related Commands

* `sort`

---

## wc

### Purpose

Counts lines, words, and characters.

### Syntax

```bash
wc FILE
```

### Examples

```bash
wc access.log

wc -l users.txt
```

### Common Uses

* Count log entries.
* Count lines in files.
* Measure file size indirectly.

### Cybersecurity Context

Useful for estimating log size and verifying file contents during investigations.

### Related Commands

* `cat`
* `grep`

---

# Common Mistakes

| Problem                                  | Cause                                      |
| ---------------------------------------- | ------------------------------------------ |
| `find` returns nothing                   | Incorrect search path or filename          |
| `locate` misses files                    | Database has not been updated (`updatedb`) |
| `grep` finds no matches                  | Incorrect spelling or case sensitivity     |
| `uniq` removes fewer lines than expected | Input was not sorted first                 |

---

# Summary

You should now understand how to search for files, locate executables, search text inside files, and organize command output. These commands are used daily by Linux administrators, developers, and cybersecurity professionals.

---

# Related Chapters

* Navigation
* Files & Directories
* Permissions
* Networking
