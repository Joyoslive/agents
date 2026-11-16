# Boundaries

## Explorer briefing

Explore the requested surface and identify the established interfaces it consumes across its boundaries. For each relevant interface, locate:

- Its definition and implementation.
- Applicable documentation.
- Representative uses elsewhere.

Trace the obligations on callers, including ordering, transactions, inputs and results, side effects, errors, and other constraints where relevant. Return:

- The interface and locations in the surface that use it.
- Evidence for its contract and representative usage.
- Any conflicting evidence or uncertainty.
- Any part of the exploration you could not complete.

Distinguish established requirements from patterns inferred from existing callers; existing callers can also be wrong or operate in different contexts. Do not modify files.

## Reviewer guidance

Examine the assigned block's use of established interfaces across its boundaries. Use the explorer's evidence as a starting point, inspect the relevant sources independently, and check actual usage against the interface's obligations in context. Consider:

- Ordering and transactions.
- Inputs and results.
- Side effects and errors.
- Other applicable constraints.

Investigate conflicting or unclear evidence rather than treating an observed convention as an automatic requirement. For each suspicion, report:

- The usage and contract evidence.
- The mismatch and its consequence, or the question that needs resolving.
- Any uncertainty.

Do not modify files.
