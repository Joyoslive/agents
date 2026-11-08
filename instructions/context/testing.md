# Testing

Apply the same principles of clarity, maintainability, and abstraction to tests, including their fixtures and helpers.

Test expected behavior, not implementation details. Prefer tests that continue to protect that behavior through changes that preserve it, without requiring the test itself to change.

Investigate test failures before changing tests. If a small change breaks many tests, stop and discuss with the user whether fixtures can better isolate the behavior each test verifies.

When fixing a bug, add a focused regression test where practical. Verify that it fails before the fix and passes afterward.
