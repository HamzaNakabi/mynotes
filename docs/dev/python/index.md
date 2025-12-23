---
title: Python
tags:
  - development
  - python
---

# Python Notes

Python programming language notes, libraries, and best practices.

## Topics

- [ ] Language fundamentals
- [ ] Virtual environments
- [ ] Package management (pip, poetry)
- [ ] Type hints
- [ ] Testing (pytest)
- [ ] Web frameworks (FastAPI, Django, Flask)
- [ ] Data science (pandas, numpy)
- [ ] Automation scripts

---

## Quick Reference

### Virtual Environments

```bash
# Create virtual environment
python -m venv .venv

# Activate (macOS/Linux)
source .venv/bin/activate

# Activate (Windows)
.venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Freeze dependencies
pip freeze > requirements.txt
```

### Common Patterns

```python
# Context manager
with open("file.txt", "r") as f:
    content = f.read()

# List comprehension
squares = [x**2 for x in range(10)]

# Dictionary comprehension
word_lengths = {word: len(word) for word in words}

# Type hints
def greet(name: str) -> str:
    return f"Hello, {name}!"
```

---

!!! tip "Use Poetry for modern Python projects"
    Poetry handles dependencies, virtual environments, and packaging in one tool.
    ```bash
    poetry init
    poetry add requests
    poetry shell
    ```
