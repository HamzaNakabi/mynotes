---
title: CI/CD
tags:
  - devops
  - cicd
  - automation
---

# CI/CD Notes

Continuous Integration and Continuous Deployment pipelines.

## Platforms

- [ ] GitHub Actions
- [ ] GitLab CI
- [ ] Jenkins
- [ ] CircleCI
- [ ] ArgoCD

---

## GitHub Actions

### Basic Workflow

```yaml
name: CI

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: '20'
          cache: 'npm'

      - name: Install dependencies
        run: npm ci

      - name: Run tests
        run: npm test

      - name: Build
        run: npm run build
```

### Deployment Workflow

```yaml
name: Deploy

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4

      - name: Deploy to production
        run: |
          # Deployment commands here
        env:
          DEPLOY_TOKEN: {% raw %}${{ secrets.DEPLOY_TOKEN }}{% endraw %}
```

---

## Best Practices

!!! tip "CI/CD Best Practices"
    - Keep pipelines fast (< 10 minutes)
    - Run tests in parallel
    - Cache dependencies
    - Use matrix builds for multiple environments
    - Implement proper secret management
    - Use environment-specific deployments
