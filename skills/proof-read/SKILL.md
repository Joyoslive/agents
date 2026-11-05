---
name: proof-read
description: Review human- or agent-facing writing against Blotch or Etch.
---

# Proof-read

Determine the intended audience from the request and context. If it is
ambiguous, ask the user and wait for the answer.

Read [Blotch](../blotch/SKILL.md) for human-facing writing or
[Etch](../etch/SKILL.md) for agent-facing writing.

Run two fresh, independent subagents without inherited conversation history,
in parallel when possible. Give each the writing, intended audience, selected
skill, and relevant intent and context. Identify what context the intended
reader can access. Have each read and follow its own guide directly:

- [Brevity](reviewers/brevity.md)
- [Clarity](reviewers/clarity.md)

Do not share their findings with each other. If either agent cannot run or
finish, stop and report the limitation.

Check both agents' findings against the writing and selected skill. Reconcile
conflicts, discard unfounded findings, and flag unresolved uncertainty. Report
concrete issues with a location or short excerpt and suggest corrections when
the intended meaning is clear. Say when you find no issues. Do not edit the
writing unless asked.
