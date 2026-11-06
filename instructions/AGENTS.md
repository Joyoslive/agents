# Collaboration

An implementation that doesn’t serve the user’s real intent is a bug.

- Work with the user to understand the outcome they want. Investigate the request and relevant context before deciding how to proceed.
- Discuss assumptions and design choices when they need the user's input. Revisit assumptions as you learn.
- Keep responses concise and suited to the user's immediate needs; include detail when it helps them understand or decide.
- When reporting an implementation, show the essential code or logic so the user can understand what changed. Include only the relevant excerpts; use pseudocode or a diagram when they communicate a more complex change more clearly.

Work in focused, reviewable implementation steps. Do not treat a broad feature, rewrite, or collection of independent decisions as one change merely because it serves one goal.

Scale discussion to the consequences and uncertainty of the step. For consequential changes, investigate and discuss affected behavior and structure, meaningful alternatives, tradeoffs, and relevant risks. Resolve consequential design choices with the user before implementing the affected work.

Discuss consequential work one decision at a time, or group closely related decisions. Wait for the user's response before moving on. Defer details until they're relevant.

Except for the narrow, routine requests described below, before each implementation step agents must:

1. Discuss the relevant design and explain what the change will do.
2. Show a short piece of pseudocode, a code sketch, or a concrete example so the user can confirm their understanding.
3. Describe the intended test scope and wait for the user's explicit agreement before editing.

The user's explicit request is agreement for a routine change when the intended implementation is clear and the required edits are small and confined to a small part of the code. First check the surrounding code and whether the change is reasonable. If it raises a concern or requires a meaningful design choice, discuss it before editing.

This exception does not apply to substantial additions or many repeated edits, even if each edit is simple or the behavioral change is small. Discuss the implementation and obtain agreement before editing.

For other changes, after agreement, implement only the agreed step and stop for the user's review. Agreement on an overall direction or plan does not by itself authorize every implementation step. If work reveals a new design choice or a need to change scope or direction, discuss it and wait for explicit agreement before proceeding. Read-only investigation can continue without a checkpoint.

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
