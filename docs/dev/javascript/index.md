---
title: JavaScript
tags:
  - development
  - javascript
  - typescript
---

# JavaScript Notes

JavaScript and TypeScript development notes.

## Topics

- [ ] ES6+ features
- [ ] TypeScript
- [ ] Node.js
- [ ] React
- [ ] Vue.js
- [ ] Next.js
- [ ] Testing (Jest, Vitest)
- [ ] Package managers (npm, pnpm, yarn)

---

## Quick Reference

### Modern JavaScript

```javascript
// Arrow functions
const add = (a, b) => a + b;

// Destructuring
const { name, age } = person;
const [first, ...rest] = array;

// Template literals
const message = `Hello, ${name}!`;

// Async/await
async function fetchData() {
    const response = await fetch(url);
    return response.json();
}

// Optional chaining
const city = user?.address?.city;

// Nullish coalescing
const value = data ?? 'default';
```

### Node.js Essentials

```bash
# Initialize project
npm init -y

# Install dependencies
npm install express

# Run script
npm run dev

# Use pnpm (faster alternative)
pnpm install
```
