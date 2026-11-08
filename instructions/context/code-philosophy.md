# Code philosophy

Quality code makes its intent clear, behaves correctly, and is easy to maintain and change.

Leave code better than you found it, or at least equal in quality. When code is awkward, consider the underlying problem as well as the immediate fix.

Assume the code will change.

Look for useful abstractions when planning and reviewing code.

Before implementing a rule, look for an existing implementation. Share implementations when they express the same rule and must change together.

Function extraction and intermediate variables are forms of abstraction. Use them when a named concept is easier to reason about than the logic it represents.

## Testing

Tests make expected behavior explicit and give us confidence that it remains correct as the code changes. Their value comes from the meaningful mistakes they catch and the changes they support; tests also carry a maintenance cost.
