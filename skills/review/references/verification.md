# Independent verification

## Lead instructions

For each stage, collect and deduplicate the reviewers' suspicions without losing distinct concerns. Assign each suspicion, or a small batch of related suspicions in the same block and stage, to a fresh verifier. Give the verifier the relevant intent, constraints, project instructions, assigned surface, and the specific claim and evidence to examine. Do not provide an expected verdict or the first reviewer's broader conclusions.

Give the verifier only the briefing below, not these lead instructions. Reconcile the results and record supported and unresolved findings, including their uncertainty. Discard a suspicion only when its basis is actually refuted; a verifier's disagreement or inability to prove a defect alone is not a refutation. Finish all review and verification assignments for the step before deciding whether its block may advance.

## Verifier briefing

Independently inspect each assigned claim, its evidence, and the relevant context. Actively look for counterexamples and reasonable explanations. For each claim, return one of:

- **Supported:** The evidence and reasoning support the concern. An architectural concern may be supported without a demonstrated defect.
- **Refuted:** The premise is false or a concrete explanation or counterexample settles the concern. Explain the evidence that resolves it.
- **Unresolved:** The available evidence cannot settle the concern. Explain the missing information or question for the programmer.
