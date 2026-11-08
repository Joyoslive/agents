# Reporting

After each implementation step, summarize the result for review with a table:

| Type | A | M | R | +/- Lines |
|---|---:|---:|---:|---|
| File category | X | Y | Z | +X / -Y |
| … | | | | |
| Functions | X | Y | Z | — |
| Tests | X | Y | Z | — |

A, M, and R mean added, modified, and removed. Omit rows with no changes.

Common file categories include source files, test files, documentation, and configuration. Add other categories when useful.

Omit generated files and lockfiles by default unless they matter to the review.

For line counts:

- Report added and removed lines for each file category.
- Include a total when more than one file category is shown.
- For files with existing changes, compare the state before and after the step so earlier changes are not included.

Count named functions and methods as modified when their name or code changes. Exclude formatting-only changes and anonymous callbacks.

For test definitions:

- Count added, modified, and removed definitions.
- Count a parameterized test as one definition; mention case changes separately when they matter.
- Count renames as modifications; exclude formatting-only changes.
