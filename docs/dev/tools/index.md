---
title: Development Tools
tags:
  - development
  - tools
---

# Development Tools

IDEs, editors, utilities, and productivity tools.

## Tools

- [ ] VS Code
- [ ] Neovim
- [ ] Git
- [ ] GitHub CLI
- [ ] Terminal tools (tmux, zsh)
- [ ] HTTP clients (curl, httpie, Postman)

---

## Git Essentials

```bash
# Clone repository
git clone <url>

# Create branch
git checkout -b feature/my-feature

# Stage and commit
git add .
git commit -m "feat: add new feature"

# Push
git push -u origin feature/my-feature

# Rebase
git rebase main

# Interactive rebase
git rebase -i HEAD~3
```

## Useful Aliases

```bash
# Git aliases (~/.gitconfig)
[alias]
    co = checkout
    br = branch
    ci = commit
    st = status
    lg = log --oneline --graph
```
