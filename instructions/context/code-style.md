# Code style

Use blank lines to make the logical structure of code visible. Apply these rules in priority order:

1. Add a blank line after multiline statements.
2. Keep initialization and immediate validation together.
3. Separate distinct steps with a blank line.

Keep short expressions and flat records compact; expand them when their contents are easier to read separately.

## Variables

Keep variables close to where they are used.

Prefer named intermediate variables over multiline conditions when they clarify the condition.

Use `!` with identifiers, direct property access, or short compound conditions. For more complex conditions, prefer a named condition that makes the negation clear.

Iterate directly over identifiers or property access. Name transformed collections and multiline iterable expressions before iterating.

## Function placement

Place the main function or entry point first, followed by functions from higher-level orchestration to lower-level details.
