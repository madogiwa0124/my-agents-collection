---
name: copilot-review
description: "Sends current git changes to GitHub Copilot CLI for code review and displays the results. Use when requesting a second-opinion review from Copilot on staged changes, uncommitted work, or a branch diff."
argument-hint: "Optionally specify scope: 'staged', 'unstaged', 'all' (default), or a git ref/branch (e.g. 'main')."
---

# Copilot Review

Sends the current git diff to `copilot` for review and displays the result.

## Procedure

1. Get the diff based on the scope argument:

   | Argument     | Command                      |
   |--------------|------------------------------|
   | none / `all` | `git diff HEAD`              |
   | `staged`     | `git diff --staged`          |
   | `unstaged`   | `git diff`                   |
   | ref/branch   | `git diff <ref>...HEAD`      |

2. If the diff is empty, tell the user there are no changes to review.

3. Write the diff to a temp file and call `copilot`.  
   The table above maps each scope to the right `git diff` command; substitute accordingly:

   ```bash
   TMPFILE=$(mktemp)
   trap 'rm -f "$TMPFILE"' EXIT
   git diff HEAD > "$TMPFILE"   # replace with scoped command from table above
   copilot -p "Please review the diff at $TMPFILE and give feedback on bugs, security issues, and code quality." \
     --allow-tool='read' --add-dir "$(dirname $TMPFILE)" -s
   ```

4. Display Copilot's output to the user.
