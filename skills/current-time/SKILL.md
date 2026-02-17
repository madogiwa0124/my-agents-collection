---
name: current-time
description: "Get the current date and time. Use when a log timestamp or time check is needed."
argument-hint: "Briefly state the needed date/time format or purpose."
---

# Current Time Skill

## When to Use
- When the current date or time is needed.
- When used for logging or time-based processing.

## Procedure
1. Run the following command to get the current date and time.
2. Change the format if needed.

```sh
date +"%Y-%m-%d %H:%M:%S %z"
# => YYYY-MM-DD HH:MM:SS +ZZZZ
```
