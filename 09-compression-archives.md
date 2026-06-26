# Compression & Archives

Archive commands package and compress files for storage and transfer.

---

## tar

### Purpose

Creates and extracts archive files.

### Syntax

```bash
tar -cvf archive.tar folder/
tar -xvf archive.tar
```

### Cybersecurity Context

Commonly used when collecting logs or transferring evidence.

### Related Commands

- `gzip`

---

## gzip

### Purpose

Compresses a file.

### Syntax

```bash
gzip file.txt
```

### Related Commands

- `gunzip`

---

## gunzip

### Purpose

Decompresses a gzip archive.

### Syntax

```bash
gunzip file.txt.gz
```

### Related Commands

- `gzip`

---

## zip

### Purpose

Creates ZIP archives.

### Syntax

```bash
zip archive.zip file.txt
```

### Related Commands

- `unzip`

---

## unzip

### Purpose

Extracts ZIP archives.

### Syntax

```bash
unzip archive.zip
```

### Related Commands

- `zip`
