# Networking

Networking commands help inspect interfaces, test connectivity, troubleshoot name resolution, and securely communicate with remote systems.

---

## ip a

### Purpose

Displays network interfaces and their IP addresses.

### Syntax

```bash
ip a
```

### Common Uses

- View IP addresses.
- Check interface status.
- Troubleshoot connectivity.

### Cybersecurity Context

Useful when identifying interface configuration during investigations or lab work.

### Related Commands

- `ip r`
- `ss`

---

## ip r

### Purpose

Displays the routing table.

### Syntax

```bash
ip r
```

### Common Uses

- Verify the default gateway.
- Troubleshoot routing issues.

### Cybersecurity Context

Helps determine how traffic leaves the host.

### Related Commands

- `ip a`

---

## ping

### Purpose

Tests network connectivity using ICMP.

### Syntax

```bash
ping HOST
```

### Example

```bash
ping 8.8.8.8
```

### Common Uses

- Verify connectivity.
- Measure latency.

### Cybersecurity Context

Useful during troubleshooting, though ICMP may be blocked on some systems.

### Related Commands

- `traceroute`

---

## traceroute

### Purpose

Shows the path packets take to a destination.

### Syntax

```bash
traceroute HOST
```

### Related Commands

- `ping`

---

## ss

### Purpose

Displays active network connections and listening sockets.

### Syntax

```bash
ss -tulpn
```

### Cybersecurity Context

Useful for identifying listening services and unexpected open ports.

### Related Commands

- `netstat`

---

## netstat

### Purpose

Displays network connections and routing information (legacy).

### Syntax

```bash
netstat -tulpn
```

### Related Commands

- `ss`

---

## nslookup

### Purpose

Queries DNS records.

### Syntax

```bash
nslookup openai.com
```

### Related Commands

- `dig`

---

## dig

### Purpose

Performs detailed DNS queries.

### Syntax

```bash
dig openai.com
```

### Related Commands

- `nslookup`

---

## curl

### Purpose

Transfers data to or from a server.

### Syntax

```bash
curl URL
```

### Example

```bash
curl https://example.com
```

### Cybersecurity Context

Frequently used to test web services and APIs.

### Related Commands

- `wget`

---

## wget

### Purpose

Downloads files from the web.

### Syntax

```bash
wget URL
```

### Related Commands

- `curl`

---

## ssh

### Purpose

Connects securely to a remote system.

### Syntax

```bash
ssh user@host
```

### Cybersecurity Context

One of the most common protocols for secure remote administration.

### Related Commands

- `scp`

---

## scp

### Purpose

Securely copies files between systems using SSH.

### Syntax

```bash
scp file.txt user@host:/path
```

### Related Commands

- `ssh`
