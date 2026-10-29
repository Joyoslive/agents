# Code philosophy

Quality code makes its intent clear, behaves correctly, and is easy to maintain and change.

Leave code better than you found it, or at least equal in quality. When code is awkward, consider the underlying problem as well as the immediate fix.

Assume the code will change. Favor designs that are easy to understand and modify.

Look for useful abstractions when planning and reviewing code. Explain to the user what difficulty each abstraction addresses and its tradeoffs. Discuss consequential structural choices before implementing them.

Share implementations when they express the same rule and must change together. Do not combine independent rules solely because their implementations look similar.

Function extraction and intermediate variables are forms of abstraction. Use them when a named concept is easier to reason about than the logic it represents.
