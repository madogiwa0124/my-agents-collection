# My Agents Collection

This repository is a collection of prompts for AI agents that I have created.

## Usage

### For Copilot CLI

Add the following line to your terminal to install the collection as a Copilot plugin.

```sh
$ copilot plugin marketplace add madogiwa0124/my-agents-collection
```

Then, install the desired plugin from the collection.

```sh
$ copilot plugin install {{plugin_name}}@my-agents-collection
```

### For Claude Code

Add the following marketplace to Claude Code:

```sh
$ /plugin marketplace add madogiwa0124/my-agents-collection
```

Then, install the desired plugin from the collection.

```sh
$ /plugin install {{plugin_name}}@my-agents-collection
```

## Collection Overview

### Plugins

| Plugin                                     | Description                   |
| ------------------------------------------ | ----------------------------- |
| [Auto Implementation](./plugins/auto-impl) | A set of agents for automatic implementation using SubAgent. |
| [Prompting Best Practices](./plugins/prompting) | A plugin that provides best practices and guidelines for creating effective prompts for agents. |
| [My Tech Blog](./plugins/my-techblog) | A plugin that provides a custom agent for writing my technical blog posts. |

### Skills

| Skill                                      | Description                   |
| ------------------------------------------ | ----------------------------- |
| [Commit Message](./skills/commit-message)  | Generates clear Git commit messages using Conventional Commits. Use when crafting a subject line and body for a change. |
| [Current Time](./skills/current-time)          | Get the current date and time. Use when a log timestamp or time check is needed. |
| [Skill Creation Best Practices](./skills/skill-creation-best-practice) | Provides guidelines and best practices for creating and improving new skills for agents. |
| [Prompting Best Practices](./skills/prompting-best-practice) | Supports the creation and improvement of prompts for various use cases. |

## Resources

- [Awesome GitHub Copilot](https://github.com/github/awesome-copilot)
- [Anthropics Skills](https://github.com/anthropics/skills)
- [Awesome Claude Code Plugins](https://github.com/ccplugins/awesome-claude-code-plugins)
