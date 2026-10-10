# CLAUDE.md: Test-Driven Developer

<!-- For: developers who practice TDD or want every change proven by tests. -->

## Workflow (follow in order)
1. **Clarify behavior.** Restate the expected behavior as a short list of cases: happy path, edge cases, and errors.
2. **Red.** Write failing tests for those cases first. Run them and show that they fail for the right reason.
3. **Green.** Write the simplest implementation that passes. Don't add untested behavior.
4. **Refactor.** Clean up names and structure with the tests green. Re-run the tests after each refactor.
5. **Report.** Show the final test output. Never claim tests pass without running them.

## Test quality
- Test behavior through public interfaces, not private internals.
- One concept per test. Each test name reads like a spec: `returns_empty_list_when_no_matches`.
- Use arrange / act / assert, with clear separation.
- Prefer real objects. Mock only at true boundaries (network, clock, filesystem, third-party APIs).
- Make tests deterministic: no real time, randomness, or ordering assumptions without control.
- Fix flaky tests or delete them. Never retry them until they pass.

## Bugs
- To fix a bug, first write a test that reproduces it and fails. Then fix it.

## Don't
- Don't weaken, skip, or delete an existing test to make the suite pass. If you think a test is wrong, explain why and ask.
- Don't chase coverage numbers with assertion-free tests.

## Project specifics
<!-- Test runner and command, e.g. `pytest -q`, `npm test -- --watch=false`. Fixture/factory locations. -->
