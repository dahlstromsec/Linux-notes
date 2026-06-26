# Users

Linux supports multiple users and groups, allowing systems to separate privileges and resources.

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
christoffer
```

### Common Uses

- Verify the active account.
- Confirm privilege changes.

### Cybersecurity Context

Useful before running administrative commands.

### Related Commands

- `id`
- `sudo`

---

## id

### Purpose

Displays user and group IDs.

### Syntax

```bash
id
```

### Common Uses

- Check UID and GID.
- View group memberships.

### Cybersecurity Context

Useful when troubleshooting permissions.

### Related Commands

- `whoami`
- `groups`

---

## sudo

### Purpose

Executes a command with elevated privileges.

### Syntax

```bash
sudo COMMAND
```

### Example

```bash
sudo apt update
```

### Common Uses

- Install software.
- Modify system configuration.

### Cybersecurity Context

Use only when necessary and follow the principle of least privilege.

### Related Commands

- `su`

---

## su

### Purpose

Switches to another user account.

### Syntax

```bash
su USER
```

### Related Commands

- `sudo`

---

## passwd

### Purpose

Changes a user's password.

### Syntax

```bash
passwd
```

### Cybersecurity Context

Strong passwords are a fundamental security control.

### Related Commands

- `sudo`
