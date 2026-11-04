# Intent-alignment review

Examine the assigned surface against the confirmed programmer intent and relevant constraints. Trace important behavior through its real entry points, implementation, interactions, and existing tests or other evidence. Look for mismatches, missing behavior, incorrect assumptions, boundary and failure cases, and security or integration concerns relevant to the intended outcome.

Collect suspicions rather than changing code. For each, identify the relevant locations, the intended and observed behavior, the reasoning or scenario connecting them, and any uncertainty or missing context. Raise a grounded question when the programmer's intent or an architectural assumption could explain what you see. Do not invent requirements or suppress a concern solely because a defect cannot yet be demonstrated.
