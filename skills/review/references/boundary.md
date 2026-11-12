# Boundaries

## Explorer briefing

Explore the requested surface and identify the established interfaces it consumes across its boundaries. For each relevant interface, locate its definition and implementation, applicable documentation, and representative uses elsewhere. Trace the obligations on callers, including ordering, transactions, inputs and results, side effects, errors, and other constraints where relevant.

Return the interface, locations in the surface that use it, evidence for its contract and representative usage, and any conflicting evidence or uncertainty. Distinguish established requirements from patterns inferred from existing callers; existing callers can also be wrong or operate in different contexts. Report any part of the exploration you could not complete. Do not modify files.

## Reviewer guidance

Examine the assigned block's use of established interfaces across its boundaries. Use the explorer's evidence as a starting point, inspect the relevant sources independently, and check actual usage against the interface's obligations in context. Consider ordering, transactions, inputs and results, side effects, errors, and other applicable constraints. Investigate conflicting or unclear evidence rather than treating an observed convention as an automatic requirement.

For each suspicion, identify the usage and contract evidence, explain the mismatch and its consequence or the question that needs resolving, and state any uncertainty. Do not modify files.
