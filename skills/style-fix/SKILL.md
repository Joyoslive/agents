---
name: style-fix
description: Fix style and polish issues across a requested code surface using project conventions and per-file agents.
---

# Style fix

Improve style and low-level readability in the requested surface. Read the applicable project instructions and style conventions first. Preserve behavior and limit changes to style and polish; do not pursue correctness, architecture, or interface changes.

## Screen and delegate

Quickly inspect the requested files for likely fixes under the applicable conventions. Skip files with no likely fixes. Do not run a full review or create review reports for this screening pass.

For each eligible file, assign one fixer agent exclusive ownership of that file. Give it the file, relevant project instructions and conventions, and any useful screening observations. Agents may read surrounding code for context but edit only their assigned file. Run assignments in parallel up to available capacity and queue the rest. If delegation is unavailable, report the affected files as incomplete.

Ask each fixer to inspect its whole file for style and polish issues, including these where covered by project conventions:

**Spacing and layout**

- Missing blank lines after multiline statements.
- Blank lines separating initialization from immediate validation.
- Missing blank lines between distinct steps.
- Short expressions and flat records that are unnecessarily expanded, or whose contents would be easier to read expanded.

Apply the blank-line rules in the order above if the project specifies that priority.

**Expression aliasing**

- Multiline conditions that would be clearer as named variables.
- Complex negations that would be clearer as named conditions.
- Transformed collections and multiline iterable expressions used directly in loops instead of being named first.

**Order and placement**

- Variables declared far from their use.
- Entry points placed after helper functions.
- Functions ordered from lower-level details to higher-level orchestration instead of the reverse.

Fix only changes whose behavior and safety are clear in context. Consider evaluation order, scope, and language-specific initialization or declaration behavior when introducing names or moving code. Report uncertain cases and fixes requiring changes outside the assigned file to the lead instead of making them. Preserve existing unrelated changes.

## Verify and report

After the agents finish, review their changes and run relevant project checks over the changed files or the smallest supported scope. Use check-only commands and report failures or checks that could not run. Summarize the changes, checks, and any uncertain or incomplete work. Do not claim unverified behavior is verified.
