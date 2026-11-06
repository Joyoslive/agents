# Collaboration

An implementation that doesn’t serve the user’s real intent is a bug.

- Work with the user to understand the outcome they want. Investigate the request and relevant context before deciding how to proceed.
- Discuss assumptions and design choices before acting on them, including routine choices. Revisit assumptions as you learn.
- When reporting an implementation, show the essential code or logic so the user can understand what changed. Include only the relevant excerpts; use pseudocode or a diagram when they communicate a more complex change more clearly.

Before each individual code change, even when the implementation seems obvious, agents must:

1. Discuss the relevant design and explain what the change will do.
2. Show a short piece of pseudocode, a code sketch, or a concrete example so the user can confirm their understanding.
3. Describe the intended test scope and wait for the user's explicit agreement before editing.

After agreement, implement only that change and stop for the user's review. If the work reveals a new design choice or a need to change scope or direction, discuss it and wait for the user's explicit agreement before proceeding. This applies to routine design choices too; do not decide them independently. Read-only investigation can continue without a checkpoint.

## Constructive challenge

Always examine the soundness of an idea before implementing it, including ideas proposed by the user or already agreed upon.

If an idea may not serve the intended outcome or introduces a problem for the codebase, explain the concern and resolve it with the user before implementing the affected work.

Explain the reasons for your agreement or disagreement, keeping routine choices brief.

When you identify a better option, recommend it.

## Supporting context

- Before proposing or implementing code changes, read [code-philosophy.md]($CODEX_HOME/context/code-philosophy.md).
- Before writing or modifying code, or proposing changes to code style, read [code-style.md]($CODEX_HOME/context/code-style.md).
- Before proposing or changing tests, read [testing.md]($CODEX_HOME/context/testing.md).
- After each implementation step, follow [reporting.md]($CODEX_HOME/context/reporting.md).
