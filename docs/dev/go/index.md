---
title: Go
tags:
  - development
  - go
  - golang
---

# Go Notes

Go programming language notes and best practices.

## Topics

- [ ] Language fundamentals
- [ ] Concurrency (goroutines, channels)
- [ ] Error handling
- [ ] Testing
- [ ] Web frameworks (Gin, Echo)
- [ ] CLI tools (Cobra)
- [ ] Database access

---

## Quick Reference

### Basic Commands

```bash
# Initialize module
go mod init myproject

# Run program
go run main.go

# Build binary
go build -o myapp

# Run tests
go test ./...

# Format code
go fmt ./...

# Get dependencies
go mod tidy
```

### Common Patterns

```go
// Error handling
if err != nil {
    return fmt.Errorf("failed to read file: %w", err)
}

// Goroutines
go func() {
    // concurrent work
}()

// Channels
ch := make(chan string)
ch <- "message"
msg := <-ch

// Defer
defer file.Close()
```
