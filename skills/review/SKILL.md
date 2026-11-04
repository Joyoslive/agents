---
name: review
description: Review a requested software surface through independent, progressively deeper review stages, or review only its polish, and write a report.
---

# Review

Review the surface the user requests. Default to `full`; use `polish` when the user explicitly requests a polish-only review. A review is read-only: do not modify the reviewed work or other files. The lead writes the requested report as the sole file change.

## Start with checks

Read [checks.md](references/checks.md) and run all applicable lint and formatting checks over the requested surface before either mode. Complete the entire checks step, even if a check fails. If any check fails or an applicable check cannot be completed safely, report the results and stop. Do not start review agents. If no check is configured for a category, record that fact rather than inventing one.

## Full review

1. Read [intent.md](references/intent.md). Explore the surface, ask the programmer concise sanity-check questions, and wait for the answers. Use the confirmed intent and architecture to partition the surface into non-overlapping, independent blocks. If independence cannot be established, keep the affected parts together, including as one block for the entire surface if necessary.
2. For each block, run these stages in order:
   - Intent alignment: [intent-alignment.md](references/intent-alignment.md).
   - Architecture: [architecture.md](references/architecture.md).
   - Interface and naming: [interface-and-naming.md](references/interface-and-naming.md).
   - Polish: [polish.md](references/polish.md).
3. Give each stage's reviewers its guidance, the confirmed intent, relevant constraints, and their assigned surface. Assign at least one reviewer to each block at each stage. For polish, divide the block into non-overlapping file groups.
4. Verify the stage's suspicions as described in [verification.md](references/verification.md). Complete all review and verification assignments for the stage before deciding the block's next step. A supported or unresolved finding stops that block between stages until resolved; record its remaining stages as deferred. Discard a suspicion only when its basis is actually refuted.

Blocks run as independent tracks: a block can advance as soon as its own stage completes and passes, without waiting for another block. A blocked or incomplete block does not stop an independent block. Wait for every track to finish or stop before writing the combined report. If a stage cannot be completed, record the limitation and stop that block between stages; do not treat incomplete work as a pass.

## Polish-only review

After the checks pass, split the requested files into non-overlapping groups. Do not run the intent questions or architectural partitioning. Give each group to a fresh polish reviewer with [polish.md](references/polish.md), the applicable conventions, and any relevant intent already known. Verify its suspicions with [verification.md](references/verification.md), then report the results.

## Delegation

Every review and verification assignment gets a fresh agent with no inherited conversation history or previous assignments. Use a no-history spawn mechanism, such as `fork_turns: none` when available. Inheriting model and reasoning settings is separate from inheriting context. Never reuse a reviewer or verifier for another assignment.

Provide only what the assignment needs: its assigned surface, relevant project instructions and constraints, confirmed or otherwise known intent, and the review stage guidance or the verifier briefing, as appropriate. For verification, include the specific claim and evidence to examine. Give verifiers only the briefing in [verification.md](references/verification.md), not its lead instructions. Do not supply the overall workflow, other reviewers' conclusions, or an expected verdict. Reviewers may read surrounding code as context; assigned ownership remains non-overlapping. Let them work read-only.

Run independent assignments in parallel up to the available capacity; queue the rest. A verifier may examine a small batch of related suspicions within one block and stage. If fresh delegation is unavailable or cannot be guaranteed, report the limitation and stop the affected review work rather than reusing context or presenting it as completed.

Review and verification agents inherit the lead's model and reasoning settings by default. For polish, use a cheap available model with low reasoning effort when the environment supports that choice; otherwise inherit. Never sacrifice the fresh-context requirement for a model choice.

## Report

Write one report to the user's requested path, or to `review-report.md` in the working directory. If the default path exists, choose a non-conflicting name; do not overwrite it. Include:

- The requested scope and mode, check commands and outcomes, and any checks that were unavailable or not applicable.
- For `full`, the confirmed intent, block boundaries, and the basis for their independence when established.
- Findings grouped by block or file group and stage, with relevant locations, evidence, reasoning, uncertainty, and useful alternatives or tradeoffs when available. Distinguish demonstrated defects from supported concerns and unresolved questions.
- Each track's completed, blocked, deferred, or incomplete stages, including why further work stopped. For a check failure, explicitly state that review stages did not run.

Return the report path and a short summary in chat. Do not imply that skipped or incomplete stages passed.
