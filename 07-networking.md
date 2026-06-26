# Networking

> **Estimated Reading Time:** 15–20 minutes
> **Difficulty:** Beginner–Intermediate
> **Prerequisites:** Navigation

Networking commands help you inspect interfaces, test connectivity, troubleshoot DNS, identify listening services, and securely connect to remote systems.

---

## What You'll Learn

* Viewing network interfaces
* Testing connectivity
* Querying DNS
* Viewing listening ports
* Secure remote access

---

# Networking Commands

---

## ip a

### Purpose

Displays network interfaces and IP addresses.

### Syntax

```bash
ip a
```

### Common Uses

* View IP addresses.
* Verify interface status.
* Troubleshoot networking.

### Cybersecurity Context

Useful when identifying interface configuration during investigations or penetration testing.

### Related Commands

* `ip r`

---

## ip r

### Purpose

Displays the system routing table.

### Syntax

```bash
ip r
```

### Common Uses

* View the default gateway.
* Troubleshoot routing.

### Cybersecurity Context

Helps determine how traffic reaches external networks.

### Related Commands

* `ip a`

---

## ping

### Purpose

Tests connectivity using ICMP.

### Syntax

```bash
ping HOST
```

### Examples

```bash
ping google.com

ping 8.8.8.8
```

### Common Uses

* Verify connectivity.
* Measure latency.
* Troubleshoot networking.

### Cybersecurity Context

Useful during troubleshooting, although ICMP may be disabled on production systems.

### Related Commands

* `traceroute`

---

## traceroute

### Purpose

Displays the path packets take to a destination.

### Syntax

```bash
traceroute HOST
```

### Example

```bash
traceroute google.com
```

### Common Uses

* Identify routing issues.
* Locate network bottlenecks.

### Cybersecurity Context

Useful when diagnosing connectivity problems across multiple networks.

### Related Commands

* `ping`

---

## ss

### Purpose

Displays network sockets and listening ports.

### Syntax

```bash
ss -tulpn
```

### Common Uses

* View open ports.
* Identify listening services.
* Troubleshoot applications.

### Cybersecurity Context

Often used to identify unnecessary or suspicious services listening on a system.

### Related Commands

* `netstat`

---

## netstat

### Purpose

Displays network connections and routing information.

### Syntax

```bash
netstat -tulpn
```

### Common Uses

* View active connections.
* Troubleshoot networking.

### Cybersecurity Context

Legacy command still encountered on many systems.

### Related Commands

* `ss`

---

## nslookup

### Purpose

Queries DNS servers.

### Syntax

```bash
nslookup DOMAIN
```

### Example

```bash
nslookup openai.com
```

### Related Commands

* `dig`

---

## dig

### Purpose

Performs advanced DNS lookups.

### Syntax

```bash
dig DOMAIN
```

### Example

```bash
dig openai.com
```

### Cybersecurity Context

Useful when investigating DNS records and troubleshooting name resolution.

### Related Commands

* `nslookup`

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

Frequently used to test APIs, download responses, and verify web services.

### Related Commands

* `wget`

---

## wget

### Purpose

Downloads files from web servers.

### Syntax

```bash
wget URL
```

### Example

```bash
wget https://example.com/file.txt
```

### Related Commands

* `curl`

---

## ssh

### Purpose

Creates a secure remote connection using SSH.

### Syntax

```bash
ssh user@host
```

### Example

```bash
ssh christoffer@192.168.1.10
```

### Cybersecurity Context

SSH is the standard protocol for secure remote administration.

### Related Commands

* `scp`

---

## scp

### Purpose

Securely copies files between systems using SSH.

### Syntax

```bash
scp FILE user@host:/destination
```

### Example

```bash
scp report.txt christoffer@192.168.1.10:/home/christoffer
```

### Common Uses

* Transfer files securely.
* Copy logs between systems.

### Cybersecurity Context

Useful when securely transferring investigation artifacts between Linux systems.

### Related Commands

* `ssh`

---

# Common Mistakes

| Problem                 | Cause                        |
| ----------------------- | ---------------------------- |
| Host unreachable        | Network connectivity issue   |
| Connection refused      | Service not listening        |
| Permission denied (SSH) | Incorrect credentials or key |

---

# Summary

You should now understand how to inspect network interfaces, test connectivity, query DNS, identify open ports, and securely communicate with remote systems.

---

# Related Chapters

* Processes
* Security
* Bash
