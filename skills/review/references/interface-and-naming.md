# Interface and naming review

Examine the assigned surface's interfaces and names in light of its intent and project conventions. Consider public and internal boundaries, including:

- Types, parameters, and return values.
- Side effects, errors, and usage constraints.
- The concepts names communicate.

Trace representative callers to see whether contracts are understandable and consistent. Look for:

- Misleading or inconsistent names.
- Unclear or surprising contracts.
- Unnecessary exposure of implementation details.
- Interfaces that make intended use difficult.

For each suspicion, identify the relevant locations, what a caller or maintainer may misunderstand, the reasoning, and any uncertainty. Suggest a clearer alternative when useful. Do not modify files.
