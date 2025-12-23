---
title: Security Tools
tags:
  - security
  - tools
---

# Security Tools

Security tools and utilities reference.

## Categories

### Reconnaissance

| Tool | Purpose |
|------|---------|
| Nmap | Port scanning and service detection |
| Amass | Subdomain enumeration |
| Shodan | Internet-wide scanning database |
| Censys | Security research platform |

### Web Application

| Tool | Purpose |
|------|---------|
| Burp Suite | Web proxy and scanner |
| OWASP ZAP | Open-source web security scanner |
| ffuf | Web fuzzer |
| sqlmap | SQL injection tool |

### Password & Hashing

| Tool | Purpose |
|------|---------|
| Hashcat | Password recovery |
| John the Ripper | Password cracking |
| Hydra | Online password attacking |

### Network

| Tool | Purpose |
|------|---------|
| Wireshark | Network protocol analyzer |
| tcpdump | Command-line packet analyzer |
| Responder | LLMNR/NBT-NS poisoning |

---

## Quick Commands

### Nmap

```bash
# Quick scan
nmap -sV target.com

# Full scan
nmap -sC -sV -p- -oA full_scan target.com

# Vulnerability scan
nmap --script vuln target.com
```

### Hashcat

```bash
# MD5
hashcat -m 0 hash.txt wordlist.txt

# SHA-256
hashcat -m 1400 hash.txt wordlist.txt

# NTLM
hashcat -m 1000 hash.txt wordlist.txt
```

### ffuf

```bash
# Directory fuzzing
ffuf -w wordlist.txt -u https://target.com/FUZZ

# Parameter fuzzing
ffuf -w params.txt -u https://target.com?FUZZ=value
```
