# The Unix philosophy

Coding agents work best in projects that follow the [Unix
philosophy](https://en.wikipedia.org/wiki/Unix_philosophy): build small tools
that do one thing well, accept text input, and produce text output.

That interface is more than a historical curiosity. Fifty years later,
text-in, text-out remains one of the most effective interfaces for software
engineering. It is easy for an agent to discover, compose, inspect, and
verify.

## Why text works so well for agents

Science fiction led us to imagine AI as binary-in, binary-out. After all,
`1`s and `0`s are often described as the "native language of computers." That
is not how modern [large language models
(LLMs)](https://en.wikipedia.org/wiki/Large_language_model) interact with
software, though. LLMs are trained on human-produced text: documentation,
source code, issue discussions, and, yes, plenty of bad GitHub code.

Agents therefore work most naturally with the same things developers do:
readable files, predictable commands, explicit errors, and observable test
results. A command such as `pytest tests/` gives an agent a clear action and a
clear result. A test failure gives it text to inspect and a concrete problem
to solve.

This does not mean every tool must literally use a shell pipeline. It means
that important project behavior should be exposed through simple, composable,
and inspectable interfaces.

## What makes a project agent-friendly?

Agent-friendly projects tend to have:

- **Robust tests** that make expected behavior executable and regressions
  visible.
- **Enforced formatting, style, and static typing** so correctness is not
  hidden in subjective conventions.
- **A well-organized file structure** that makes responsibilities and entry
  points easy to find.
- **Consistent naming** for files, functions, types, commands, and concepts.
- **Clear architecture and readable code** with focused modules and explicit
  boundaries.
- **Useful documentation and errors** that explain how to operate the system
  and what went wrong.

These properties reduce the amount of context an agent must infer. They also
make its changes easier for a human to review.

## Design for composition

Prefer commands and modules with one obvious responsibility. Keep inputs and
outputs explicit, use stable text formats where practical, and make failures
visible instead of silently recovering. A good workflow often looks like:

1. inspect the relevant files;
2. run a focused command or test;
3. make one coherent change;
4. run the formatter, type checker, and tests; and
5. inspect the resulting diff.

This structure gives an agent frequent checkpoints. It can use each command's
output as evidence, rather than guessing whether a hidden side effect
occurred.

## Preventing the spread of slop

Architecture is a force multiplier. The better the project is organized, the
easier it is for an agent to make a correct change. The reverse is also true:
once unclear names, duplicated logic, inconsistent formatting, and untested
behavior enter a repository, agents will happily reproduce those patterns.

Treat every agent change as a contribution to the project's future examples.
Keep the change small, run the project's checks, and improve the surrounding
structure when it is directly relevant. Good constraints do not limit agents;
they give agents reliable boundaries within which to work.