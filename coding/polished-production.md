# CLAUDE.md: Polished, Production-Grade Code

<!-- For: developers shipping to real users who want code that passes a strict senior review the first time. -->

## About me
I ship production software. I'd rather wait a little longer for code that is correct, robust, readable, and maintainable than get something fast that I'll have to rework.

## Before writing code
- Read the surrounding modules, types, and tests until you understand the conventions. New code should look like the best existing code in the repo.
- For anything beyond a small change, outline your approach in 3–6 bullets first: which files change, the key design decisions, and the edge cases. Then implement.
- Find existing utilities, hooks, and helpers before writing new ones. Duplication counts as a defect.

## Quality bar
- **Correctness first.** Think through edge cases: empty input, null or undefined values, very large input, concurrency, partial failure, retries, timezones, and Unicode.
- **Types.** Use precise types. No `any` or loose casts unless you justify them in a comment. Make invalid states impossible to represent where that's practical.
- **Errors.** Fail loudly and clearly at the boundaries. Never swallow an exception silently. Error messages should say what went wrong and what to do about it.
- **Naming.** Names should explain intent. Avoid abbreviations unless they're idiomatic in the codebase.
- **Structure.** Each function does one thing. Keep pure logic separate from I/O. Put dependencies where they can be swapped in tests.
- **Security.** Validate untrusted input, parameterize queries, and never log secrets or personal data.
- **Performance.** Avoid N+1 queries, needless re-renders, and accidental O(n²) work on unbounded data. Don't micro-optimize without a measurement.
- **Accessibility (UI).** Use semantic elements and labels, make everything keyboard-reachable, and keep enough contrast.

## Tests
- Add or update tests for every behavior change: the happy path, edge cases, and at least one failure path.
- Tests check behavior, not implementation details. Each test name should state the expected behavior.
- Run the full relevant test suite, type checker, and linter before you say you're done. Report the actual output.

## Finish
- Self-review the diff as a strict reviewer would. Remove debug output, unused imports, and leftover scaffolding.
- End with a short summary: what changed, why, any trade-offs, and anything I should check manually.

## Don't
- Don't leave TODOs, placeholder implementations, or "simplified for brevity" code.
- Don't silence a linter or type error to make it go away. Fix the cause.
- Don't change public APIs or database schemas without calling it out explicitly.

## Project specifics
<!-- Stack, commands, style guide links, architectural rules. -->
