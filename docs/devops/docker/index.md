---
title: Docker
tags:
  - devops
  - docker
  - containers
---

# Docker Notes

Container fundamentals and Docker best practices.

## Topics

- [ ] Dockerfile best practices
- [ ] Multi-stage builds
- [ ] Docker Compose
- [ ] Networking
- [ ] Volumes and storage
- [ ] Security

---

## Quick Reference

### Essential Commands

```bash
# Build image
docker build -t myapp:latest .

# Run container
docker run -d -p 8080:80 --name myapp myapp:latest

# List containers
docker ps -a

# View logs
docker logs -f myapp

# Execute command in container
docker exec -it myapp /bin/sh

# Stop and remove
docker stop myapp && docker rm myapp

# Remove unused resources
docker system prune -af
```

### Dockerfile Example

```dockerfile
# Multi-stage build example
FROM node:20-alpine AS builder
WORKDIR /app
COPY package*.json ./
RUN npm ci
COPY . .
RUN npm run build

FROM node:20-alpine AS runner
WORKDIR /app
COPY --from=builder /app/dist ./dist
COPY --from=builder /app/node_modules ./node_modules
EXPOSE 3000
CMD ["node", "dist/index.js"]
```

### Docker Compose

```yaml
version: '3.8'
services:
  app:
    build: .
    ports:
      - "3000:3000"
    environment:
      - NODE_ENV=production
    depends_on:
      - db
  db:
    image: postgres:15
    volumes:
      - postgres_data:/var/lib/postgresql/data
volumes:
  postgres_data:
```
