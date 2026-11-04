# Lint and formatting checks

Identify the requested surface and the project's configured lint and formatting checks. Inspect the commands and configuration sufficiently to select check-only invocations; scope them to the surface when supported. If a project command necessarily covers more, record its actual scope.

Run every applicable check, even after one fails. Use non-mutating options, disable caches where practical, and do not run formatters in write mode or commands known to change files or external state. Do not install tools or change configuration. If an applicable check cannot be run safely or its required tool is unavailable, record it as unresolved.

Record each command, its scope, and whether it passed, failed, or could not run. If no check is configured for a category, mark it not applicable. After all checks finish, any failure or unresolved applicable check blocks review. Report the results and do not launch reviewers.
