---
title: CTF
tags:
  - security
  - ctf
---

# CTF Notes

Capture The Flag writeups and solutions.

## Categories

- [ ] Web
- [ ] Crypto
- [ ] Pwn (Binary Exploitation)
- [ ] Reverse Engineering
- [ ] Forensics
- [ ] Misc

---

## Platforms

| Platform | Description |
|----------|-------------|
| [HackTheBox](https://hackthebox.com) | Machines and challenges |
| [TryHackMe](https://tryhackme.com) | Guided learning paths |
| [PicoCTF](https://picoctf.org) | Beginner-friendly CTF |
| [CTFtime](https://ctftime.org) | CTF calendar and rankings |

---

## Writeup Template

When adding a new writeup, use this structure:

```markdown
# Challenge Name

**Platform:** HackTheBox / TryHackMe / etc.
**Category:** Web / Crypto / Pwn / etc.
**Difficulty:** Easy / Medium / Hard
**Date:** YYYY-MM-DD

## Description

Brief description of the challenge.

## Reconnaissance

Initial enumeration steps.

## Solution

Step-by-step solution.

## Flag

`flag{example_flag_here}`

## Lessons Learned

Key takeaways from this challenge.
```

---

## Common Tools

```bash
# Crypto
python -c "import base64; print(base64.b64decode('...'))"

# Steganography
steghide extract -sf image.jpg
strings image.jpg
exiftool image.jpg

# Binary analysis
file binary
strings binary
ltrace ./binary
```
