# Code style

Use blank lines to make the logical structure of code visible.

- Keep statements that contribute to the same immediate purpose together.
- Separate distinct steps or changes in intent with a blank line, such as preparation, execution, and handling the result.
- Use blank lines after multiline statements to make statement boundaries clear.
- Keep short expressions and flat records compact; expand them when their contents are easier to read separately.

## Variables

Keep variables close to where they are used.

Prefer named intermediate variables over multiline conditions when they clarify the condition.

Prefer named intermediate variables over multiline iterable expressions when they clarify what a loop iterates over.

Use `!` with identifiers or direct property access. For compound conditions, prefer a named condition when its name makes the meaning clear.

Iterate directly over identifiers or property access. For transformed collections, prefer a named variable when its name makes the collection's meaning clear.

## Function placement

Place the main function or entry point first, followed by functions from higher-level orchestration to lower-level details.
