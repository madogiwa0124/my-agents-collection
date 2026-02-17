---
name: commit-message
description: "Generates clear Git commit messages using Conventional Commits. Use when crafting a subject line and body for a change."
argument-hint: "Describe what changed, why it was needed, and key details."
---

# Commit Message Guidelines

## When to Use
- You need a high-quality Git commit message.
- You want consistent Conventional Commits formatting.

## Procedure
1. Identify the primary change and select the Conventional Commit type.
2. Write the subject line in 50 characters or fewer.
3. Add a blank second line.
4. In the body, explain why the change was needed and the key details.
5. Prefer "Because there was an issue with ..., fix ..." over "Fix ...".

## Conventions
- Use the Conventional Commits format.
  - Prefixes: `feat:`, `fix:`, `docs:`, `style:`, `refactor:`, `test:`, `chore:`
  - Example: `feat: introduce Devise to provide authentication`
