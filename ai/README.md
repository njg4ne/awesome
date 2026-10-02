# AI-Assisted Programming

[← Back to all awesomes](../README.md)

## Contents

1. [Tools](#tools)
2. [Agent Context and Standards](#agent-context-and-standards)
3. [Principles](#principles)

## Tools

- [GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/overview) is best when the programmer is heavily involved, especially for:
  - inline completions
  - inline chat
  - diffs to review before accepting what the AI changed
- [Claude Code](https://code.claude.com/docs/en/overview) is a CLI that's great for agentic coding tasks that involve looking at less of the code.
  - Its [VS Code extension](https://code.claude.com/docs/en/vs-code) also shows reviewable diffs, so changes can be checked when wanted.
- Graphical apps for agentic programming are mostly untried here. So far they hold no appeal, and none is preferred.

## Agent Context and Standards

- [AGENTS.md](https://agents.md) is the preferred format for agent context. Avoid harness-specific files when possible (this repo has its own [AGENTS.md](../AGENTS.md)).
- Skills, instructions, and tools are best in open, standard formats, such as:
  - [Agent Skills](https://agentskills.io)
  - [Model Context Protocol (MCP)](https://modelcontextprotocol.io)

## Principles

1. **Prefer deterministic software when you can, even when using AI.** It's better, or at least easier, to rely on.
2. **Let LLMs be the interface.** Ideally an LLM drives ordinary code and CLI tools, and doesn't replace them.
3. **Keep the human able to review.** Diffs and inline tools let the programmer see what the AI changed whenever they want to.
