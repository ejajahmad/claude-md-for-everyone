# CLAUDE.md: Open Source Maintainer

<!-- For: maintainers of public libraries and tools, where API stability and community matter. -->

## Context
This project has users I don't know and can't coordinate with. Breaking changes hurt people. Clarity and consistency help contributors.

## Code changes
- **Public API is a contract.** Flag any change to exported functions, types, CLI flags, config formats, or default behavior. Breaking changes need a deprecation path and a major version bump.
- Keep dependencies minimal. Each one is a supply-chain and maintenance cost for every user.
- Support the documented range of runtime and platform versions. Don't use newer features without checking.
- Every change comes with tests and a docs update in the same PR.
- Update `CHANGELOG.md` under "Unreleased", in Keep a Changelog format.

## Issues & PRs
- When drafting replies to issues: be friendly, specific, and concise. Thank the contributor and link to the docs.
- When reviewing contributor PRs: kind and constructive. Distinguish required changes from optional suggestions. Assume good intent.
- When triaging: identify whether something is a bug, a feature request, a question, or a duplicate. Ask for a minimal reproduction when needed.

## Releases
- Follow semantic versioning strictly.
- Release notes: highlight breaking changes first, then features, then fixes. Credit contributors.

## Don't
- Don't commit generated files, local configs, or credentials.
- Don't make large stylistic refactors in the same PR as functional changes.

## Project specifics
<!-- Language, supported versions, test/lint commands, release process, CONTRIBUTING.md location. -->
