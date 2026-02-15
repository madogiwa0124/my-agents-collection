# Copilot Instructions

## Project Overview

- This repo is a collection of prompts for AI agents and supporting assets (skills, instructions, rules) that can be reused across tools like Copilot.
- Agent prompts are stored as Markdown with YAML frontmatter; treat each file as a standalone contract defining role, tools, and output formats.
- Use English for all content unless the target file already uses another language and the meaning would be lost otherwise.

## Prompt and Agent Design

- Preserve YAML frontmatter structure and keys when editing or adding agents: `name`, `user-invocable`, `description`, `tools`, `agents`.
- Keep role boundaries explicit in the prompt body (e.g., author vs reviewer vs implementer). Avoid instructions that blur responsibilities.
- Define outputs with concrete markdown templates and required headings. Downstream tooling may rely on exact headings and code fences.
- When adding tools, list only what the role needs and keep the tool names consistent with the surrounding plugin conventions.

## Repository Conventions

- Prefer ASCII-only content unless the target file already uses non-ASCII and the meaning would be lost otherwise.
- Keep prompts concise and action oriented; avoid generic best-practice advice that is not grounded in this repo.

## Developer Workflows

- No build/test tooling is documented in this repo. If you add automation or generation steps, document them in [README.md](../README.md) and update this file.

## Integration Points

- Tool invocation examples in prompts should match actual tool names and argument structures used in this repo.

## Reference

Refer to existing documents and guidelines such as the following:

- [Claude Prompting Best Practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)
- [Claude Agent Skills Best Practices](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/best-practices)
- [GitHub Copilot Prompt Engineering](https://docs.github.com/en/enterprise-cloud@latest/copilot/concepts/prompting/prompt-engineering)
