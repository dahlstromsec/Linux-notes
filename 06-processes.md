# Processes

Processes are running programs managed by the Linux kernel.

---

## ps

### Purpose

Displays information about running processes.

### Syntax

```bash
ps aux
```

### Common Uses

- View running processes.
- Troubleshoot applications.

### Cybersecurity Context

Useful when investigating suspicious activity.

### Related Commands

- `top`
- `kill`

---

## top

### Purpose

Displays a real-time view of running processes.

### Syntax

```bash
top
```

### Common Uses

- Monitor CPU and memory usage.

### Related Commands

- `htop`

---

## htop

### Purpose

Interactive process viewer with an easier interface.

### Syntax

```bash
htop
```

### Common Uses

- Monitor and manage processes.

### Related Commands

- `top`

---

## kill

### Purpose

Terminates a process using its PID.

### Syntax

```bash
kill PID
```

### Example

```bash
kill 1234
```

### Cybersecurity Context

Useful for stopping malicious or unresponsive processes.

### Related Commands

- `killall`

---

## killall

### Purpose

Terminates processes by name.

### Syntax

```bash
killall PROCESS_NAME
```

### Example

```bash
killall firefox
```

### Related Commands

- `kill`
