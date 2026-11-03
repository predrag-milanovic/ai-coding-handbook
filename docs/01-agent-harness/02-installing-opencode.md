# Installing OpenCode

[OpenCode](https://opencode.ai/) is an open-source AI coding agent. It can
read your repository, edit files, run commands, and use your local development
tools to validate its work.

If that sounds similar to [Claude Code](https://claude.com/product/claude-code),
[Cursor](https://cursor.com/), or [Codex](https://openai.com/codex/), that is
because they belong to the same category: tools that let an LLM work *inside*
a real software project instead of only chatting about one.

I have used Claude Code, Cursor, and Zed's in-editor agents. They all solve
similar problems, but I think the OpenCode team's taste—especially around
user experience—is excellent.

## Why OpenCode?

OpenCode is:

- **Terminal-first:** everyone on a team can use it regardless of their
  preferred editor.
- **Open-source:** the community can contribute to it, and you can inspect how
  it works.
- **Provider-agnostic:** it is not tied to one AI provider, so you can choose
  the models and services that fit your needs.
- **Focused on UX:** because the product is not selling its own models, the
  team can focus on making the agent itself better.

## Install OpenCode

Use the installation instructions for your operating system in the
[official OpenCode documentation](https://opencode.ai/docs/). After installing
it, confirm that the command is available:

```sh
opencode --version
```

If your shell cannot find `opencode`, restart the terminal or follow the
documentation's PATH instructions for your installation method.

## Configure a provider

OpenCode needs access to an AI provider before it can complete a coding task.
Follow the provider's setup instructions, then start OpenCode from the
repository you want it to work on:

```sh
cd path/to/your-project
opencode
```

Keep credentials in the provider's supported environment variables or
credential store. Do not put API keys in the repository, commit them to source
control, or paste them into project configuration files that may be shared.

## Start safely

The first time you use an agent in a repository:

1. Start in a branch or worktree where you can review its changes.
2. Ask it to inspect the project and explain its plan before making a large
   change.
3. Give it a focused task with clear acceptance criteria.
4. Review the diff and run the project's tests yourself.

OpenCode can move quickly, but it does not replace engineering judgment. Treat
its output as a proposed change that needs the same review as code written by a
teammate.