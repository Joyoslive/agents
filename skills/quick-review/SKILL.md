---
name: quick-review
description: Review a requested software surface in one pass with a single agent and write reports.
---

# Quick review

Review the requested surface yourself; do not delegate. Default to a full review. If the user requests polish only, review only polish. Do not modify the reviewed work; the two reports are the only file changes.

Run all applicable lint and formatting checks in check-only mode, without installing tools or changing configuration. Record each command, its scope and result, and any unavailable or inapplicable checks. Continue the review even if a check fails or cannot run.

For a full review, use the available context to understand the intended behavior and constraints. Review the whole surface in one pass, considering:

- **Intent:** Mismatches, missing behavior, failure cases, and relevant security or integration concerns. See [intent alignment](../review/references/intent-alignment.md).
- **Architecture:** Responsibilities, abstractions, information hiding, dependencies, contracts, and relevant tradeoffs. See [architecture](../review/references/architecture.md).
- **Boundaries:** Whether use of external interfaces satisfies their established contracts. See [boundaries](../review/references/boundary.md).
- **Interfaces and naming:** Clarity and consistency of contracts, names, and intended usage. See [interfaces and naming](../review/references/interface-and-naming.md).
- **Polish:** Concrete style and readability improvements under project conventions. See [polish](../review/references/polish.md).

Check each concern against the relevant evidence, counterexamples, and plausible explanations. Classify it as supported, refuted, unresolved, or unverified; retain refuted concerns and the evidence that resolves them. Do not present your assessment as independent verification. Continue reviewing despite findings or uncertainty, and report any work you could not complete.

Write two linked reports based on the same results, including every distinct concern. Write an agent-facing detailed report following [Etch](../etch/SKILL.md) to the user's requested path or `review-report.md`, and a human-facing summary following [Blotch](../blotch/SKILL.md) beside it with `-summary` before the extension, or appended if there is no extension. Do not overwrite an existing summary. If either default path exists, choose a non-conflicting pair.

The detailed report includes scope, mode, known intent and uncertainty, checks and outcomes, findings with locations, evidence, reasoning and assessment, and incomplete work. The summary gives each concern and its significance at a glance, useful locations, failed checks, uncertainty, and incomplete work. Link the reports to each other and return both paths with a short summary.
