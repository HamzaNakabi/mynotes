---
title: A vicious cercle
date: 2025-12-23
authors:
  - Hamza Nakabi
categories:
  - Ideas
  - LLMs
tags:
  - llms
readtime: 1
---

# Unintentional supply chain "risk"


## Introduction

Recently, I've been reading posts from open source project maintainers, and as a security engineer, something clicked: we're witnessing an unintentional supply chain risk unfold in real-time.

## Why this is happening 

Contributors are increasingly using AI to generate entire features without understanding the underlying code. The code compiles and runs, but it's often bloated with unnecessary patterns that introduce technical debt and potential vulnerabilities.

## The Problem

Here's what makes this concerning: AI doesn't understand code—it matches patterns. For example, when it encounters defensive checks in its training data, it replicates them everywhere, even when they serve no purpose. This code gets committed to repositories, becomes part of the training data for future AI models, and the cycle continues. We've created a feedback loop where suboptimal code breeds more suboptimal code.

What makes this particularly challenging is the motivation behind many of these contributions. Some contributors prioritize building an impressive GitHub profile over genuinely improving projects. While maintainers work to review thousands of lines of code daily, code quality across the ecosystem gradually degrades.

## Conclusion

AI is a powerful learning tool, but it shouldn't replace understanding. Before submitting code to open source projects, we should be able to explain every line and its purpose. This isn't about being anti-AI—it's about maintaining the quality and security that open source communities depend on.

Quality over quantity. The health of open source relies on contributors who understand what they're building.

---

*Have questions or feedback? Feel free to reach out!*
