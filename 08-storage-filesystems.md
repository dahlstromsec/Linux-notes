# Storage & Filesystems

Storage commands help inspect disks, partitions and filesystem usage.

---

## df -h

### Purpose

Displays filesystem disk usage in a human-readable format.

### Syntax

```bash
df -h
```

### Related Commands

- `du -sh`

---

## du -sh

### Purpose

Displays the size of a directory.

### Syntax

```bash
du -sh DIRECTORY
```

### Related Commands

- `df -h`

---

## mount

### Purpose

Mounts a filesystem.

### Syntax

```bash
mount DEVICE DIRECTORY
```

### Cybersecurity Context

Useful when mounting forensic images or removable media.

### Related Commands

- `umount`

---

## umount

### Purpose

Unmounts a filesystem safely.

### Syntax

```bash
umount DIRECTORY
```

### Related Commands

- `mount`

---

## lsblk

### Purpose

Lists available block devices.

### Syntax

```bash
lsblk
```

### Cybersecurity Context

Useful for identifying disks and USB devices.

### Related Commands

- `df -h`
