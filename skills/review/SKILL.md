---
name: review
description: Review a requested software surface through independent, progressively deeper review stages.
---

# Review

Review the surface the user requests. A review is read-only: do not modify the reviewed work.

## Start with checks

Read [checks.md](references/checks.md) and run all applicable lint and formatting checks over the requested surface before review. Complete the entire checks step, even if a check fails. If any check fails or an applicable check cannot be completed safely, do not start review agents; report the results and stop. If no check is configured for a category, record that fact rather than inventing one.

## Review stages

1. Read [intent.md](references/intent.md). Explore the surface, ask the programmer concise sanity-check questions, and wait for the answers. Use the confirmed intent and architecture to partition the surface into non-overlapping, independent blocks. If independence cannot be established, keep the affected parts together, including as one block for the entire surface if necessary.
2. Launch one explorer for the entire requested surface using the explorer briefing in [boundary.md](references/boundary.md). It may work while the blocks progress through their earlier stages. Give each boundary reviewer the evidence relevant to its block. If the exploration is incomplete, stop each affected block before boundary review and report the limitation.
3. For each block, run these stages in order:
   - Architecture: [architecture.md](references/architecture.md).
   - Logic: [logic.md](references/logic.md).
   - Boundaries: reviewer guidance in [boundary.md](references/boundary.md).
   - Interface and naming: [interface-and-naming.md](references/interface-and-naming.md).
4. Give each stage's reviewers its guidance, the confirmed intent, relevant constraints, and their assigned surface. Assign at least one reviewer to each block at each stage.
5. Verify the stage's suspicions as described in [verification.md](references/verification.md). Complete all review and verification assignments for the stage before deciding the block's next step. A supported or unresolved finding stops that block between stages until resolved; record its remaining stages as deferred. A refuted finding does not block the next stage, but remains in the results.

Blocks run as independent tracks: a block can advance as soon as its own stage completes and passes, without waiting for another block. A blocked or incomplete block does not stop an independent block. Wait for every track to finish or stop before presenting the combined results. If a stage cannot be completed, record the limitation and stop that block between stages; do not treat incomplete work as a pass.

## Delegation

The boundary exploration and every review and verification assignment each get a fresh agent with no inherited conversation history or previous assignments. Use a no-history spawn mechanism, such as `fork_turns: none` when available. Inheriting model and reasoning settings is separate from inheriting context. Never reuse an explorer, reviewer, or verifier for another assignment.

Provide only what the assignment needs: its assigned surface, relevant project instructions and constraints, confirmed or otherwise known intent, and the explorer briefing, review stage guidance, or verifier briefing, as appropriate. For boundary review, include the relevant explorer evidence. For verification, include the specific claim and evidence to examine. Give verifiers only the briefing in [verification.md](references/verification.md), not its lead instructions. Do not supply the overall workflow, other reviewers' conclusions, or an expected verdict. Agents may read surrounding code as context; review ownership remains non-overlapping. Let them work read-only.

Run independent assignments in parallel up to the available capacity; queue the rest. A verifier may examine a small batch of related suspicions within one block and stage. If fresh delegation is unavailable or cannot be guaranteed, report the limitation and stop the affected review work rather than reusing context or presenting it as completed.

Review and verification agents inherit the lead's model and reasoning settings by default.

## Results

Report all findings in chat.
