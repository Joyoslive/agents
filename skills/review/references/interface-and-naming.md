# Interface and naming review

Examine the assigned surface's interfaces and names in light of its intent and project conventions. Consider public and internal boundaries, including types, parameters, return values, side effects, errors, usage constraints, and the concepts names communicate. Trace representative callers to see whether contracts are understandable and consistent.

Look for misleading or inconsistent names, unclear or surprising contracts, unnecessary exposure of implementation details, and interfaces that make intended use difficult. Do not flag a wide interface solely for its size or demand that names follow a pattern that obscures the domain.

For each suspicion, identify the relevant locations, what a caller or maintainer may misunderstand, the reasoning, and any uncertainty. Suggest a clearer alternative when useful. Do not modify files.
