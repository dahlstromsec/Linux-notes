# Users

> **Estimated Reading Time:** 10–15 minutes
> **Difficulty:** Beginner
> **Prerequisites:** Permissions

Linux is a multi-user operating system. Every process runs as a user, and permissions determine what each user is allowed to access. Understanding users and privileges is essential for both Linux administration and cybersecurity.

---

## What You'll Learn

* Identifying the current user
* User and group IDs
* Running commands with elevated privileges
* Switching users
* Managing passwords

---

# User Commands

---

## whoami

### Purpose

Displays the currently logged-in user.

### Syntax

```bash
whoami
```

### Example

```bash
whoami
```

Output

```text
user
```

### Common Uses

* Verify the active user.
* Confirm privilege changes.

### Cybersecurity Context

Useful before executing administrative commands or investigating permissions.

### Related Commands

* `id`
* `sudo`

---

## id

### Purpose

Displays information about the current user, including the User ID (UID), Group ID (GID), and group memberships.

### Syntax

```bash
id
```

### Example

```bash
id
```

### Common Uses

* Verify group memberships.
* Troubleshoot permissions.
* Confirm user identity.

### Cybersecurity Context

Useful when determining whether an account has access to protected resources.

### Related Commands

* `whoami`

---

## sudo

### Purpose

Executes a command with elevated privileges.

### Syntax

```bash
sudo COMMAND
```

### Examples

```bash
sudo apt update

sudo systemctl restart ssh
```

### Common Uses

* Install software.
* Modify system configuration.
* Perform administrative tasks.

### Cybersecurity Context

Only use elevated privileges when necessary. Following the principle of least privilege reduces security risks.

### Related Commands

* `su`

---

## su

### Purpose

Switches to another user account.

### Syntax

```bash
su USER
```

### Examples

```bash
su root

su username
```

### Common Uses

* Switch between accounts.
* Perform administrative work.

### Cybersecurity Context

Switching users is common during administration but should be carefully controlled and audited.

### Related Commands

* `sudo`

---

## passwd

### Purpose

Changes the password for the current user or another user.

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

Strong, unique passwords are one of the most important security controls for protecting Linux systems.

### Related Commands

* `sudo`

---

# Common Mistakes

| Problem                   | Cause                                |
| ------------------------- | ------------------------------------ |
| `Permission denied`       | Command requires elevated privileges |
| `sudo: command not found` | sudo is not installed or configured  |
| Authentication failure    | Incorrect password entered           |

---

# Summary

You should now understand how Linux identifies users, manages privileges, and controls access to administrative commands.

---

# Related Chapters

* Permissions
* Processes
* Security
* Git
