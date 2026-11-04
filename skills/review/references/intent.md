# Programmer intent and review blocks

Explore the requested surface and enough surrounding context to understand its purpose, behavior, constraints, and architecture. Ask the programmer a few concise sanity-check questions to confirm your understanding; wait for the answers before continuing. Distinguish confirmed intent from assumptions, and include relevant answers in reviewer assignments.

Map the architectural relationships within the surface, including calls, shared mutable state, shared rules and invariants, and interactions whose behavior or review conclusions depend on each other. Partition the owned review surface into non-overlapping blocks only where their independence is established. Parts connected by such dependencies belong in the same block. If the boundary is uncertain, combine the affected parts; the entire surface may be one block.

Reviewers can read relevant material outside their assigned block as context. That does not give multiple blocks ownership of the same review surface. Record the block boundaries and the evidence for independence in the report.
