---
name: quick-review
description: Review a requested software surface in one pass with a single agent.
---

# Quick review

Review the requested surface yourself; do not delegate. Do not modify the reviewed work.

Run all applicable lint and formatting checks in check-only mode, without installing tools or changing configuration. Record each command, its scope and result, and any unavailable or inapplicable checks. Continue the review even if a check fails or cannot run.

Use the available context to understand the intended behavior and constraints. Review the whole surface in one pass, considering:

- **Logic:** Mismatches with intent, missing behavior, failure cases, and relevant security or integration concerns. See [logic](../review/references/logic.md).
- **Architecture:** Responsibilities, abstractions, information hiding, dependencies, contracts, and relevant tradeoffs. See [architecture](../review/references/architecture.md).
- **Boundaries:** Whether use of external interfaces satisfies their established contracts. See [boundaries](../review/references/boundary.md).
- **Interfaces and naming:** Clarity and consistency of contracts, names, and intended usage. See [interfaces and naming](../review/references/interface-and-naming.md).

Check each concern against the relevant evidence, counterexamples, and plausible explanations. Classify it as supported, refuted, unresolved, or unverified; retain refuted concerns and the evidence that resolves them. Do not present your assessment as independent verification. Continue reviewing despite findings or uncertainty, and report any work you could not complete.

Report all findings in chat.
