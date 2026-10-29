# Testing

Tests make expected behavior explicit and give us confidence that it remains correct as the code changes. Their value comes from the meaningful mistakes they catch and the changes they support; tests also carry a maintenance cost.

Tests are code and deserve the same care as production code. Apply the same principles of clarity, maintainability, and abstraction to tests, including their fixtures and helpers.

Test expected behavior rather than implementation details so tests remain useful when the implementation changes without changing behavior.

Investigate test failures before changing tests. If a small change breaks many tests, stop and discuss whether fixtures can better isolate the behavior each test verifies.

When fixing a bug, add a focused regression test where practical. Verify that it fails before the fix and passes afterward.
