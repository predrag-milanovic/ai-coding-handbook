# Chat, autocomplete, and agents

Not every AI coding tool does the same job. **Agent** has become a catch-all
buzzword, but the distinction matters: the right tool depends on whether you
need an explanation, a suggestion while typing, or help completing a
multi-step coding task.

I find it useful to think about AI-assisted development in three buckets:

## Chat

Chat explains ideas and answers questions. It can happen in a browser, in your
editor, or on Boot.dev with Boots; it is still a conversation with a
[large language model (LLM)](https://en.wikipedia.org/wiki/Large_language_model).

Chat is useful when you want to:

- understand an unfamiliar concept or error;
- compare approaches before changing code; or
- ask for an example, explanation, or review.

The important boundary is that chat is primarily conversational. Unless the
tool has agent capabilities, it does not carry out the workflow for you.

## Autocomplete

Autocomplete suggests the rest of the line or code block while you write. It
is highly editor-specific and is primarily an ergonomics and UX feature.

For example, you might start typing a function name and your editor suggests
the rest of the function. Press `Tab` to accept the suggestion and keep
writing.

Autocomplete is useful when you already know what you want to write and need
to write it faster. It is not a substitute for deciding what to build,
checking whether the generated code is correct, or running the relevant tests.

## Agents

Agents provide the biggest productivity boost. You interact with them
conversationally, but on each turn they can use tools to advance the task:

- run commands on your machine;
- read and write files;
- search for information;
- run tests and inspect failures; and
- make and verify a sequence of related changes.

In other words, **agents handle an entire coding workflow**, not just a
conversation or a predicted line of code. You can ask an agent to investigate
a bug, implement a fix, run the tests, and iterate on the result. You still
need to provide context and exercise judgment: an agent can make incorrect
changes quickly, so review its work and verify the outcome.

## Choosing the right tool

| Need | Best fit |
| --- | --- |
| Understand a concept or error | Chat |
| Get a suggestion while writing known code | Autocomplete |
| Investigate, change, test, and verify a codebase | Agent |

These categories can overlap. An agent may use an LLM conversationally, and
an editor may offer both chat and autocomplete. The useful question is not
what a product calls itself, but what it can do on your behalf in the current
interaction.

With how powerful agents have become, my use of chat-only and autocomplete
tools has gone down dramatically. Agents now account for more than 90% of my
AI coding workflow. That does not make the other tools obsolete: chat remains
valuable for learning and planning, while autocomplete is excellent for
small, predictable edits. But for substantial coding work, an agent is the
tool that can carry the task from intent to a tested result.