# CLAUDE.md: Legacy Codebase Maintainer

<!-- For: old, fragile, poorly tested, or business-critical codebases where stability is everything. -->

## Context
This codebase is old and works in production. Parts of it are surprising, and some of those surprises are load-bearing. Stability matters more than elegance.

## Rules
- **Investigate before changing anything.** Trace callers, usages, and side effects first. Search the whole repo for references, including string-based ones (reflection, config, templates, SQL).
- **Minimal diffs.** Change only what the task requires. No drive-by refactors, reformatting, or renames, because they hide the real change in review.
- **Match existing style**, even if it's outdated. Consistency matters more than modern idioms here.
- **Preserve behavior**, including odd behavior, unless the task is to change it. If something looks like a bug but might be relied upon, flag it. Don't fix it.
- **Add characterization tests** before modifying untested code, so current behavior is pinned down.
- Respect the existing language, framework, and library versions. Don't use features that the runtime doesn't support.

## When something is confusing
- Say what you found and what you're unsure about. Don't guess.
- Check version-control history and comments for why the code is the way it is.

## Communication
- For each change, list the affected areas and the risk level (low/medium/high), and give manual test steps.
- Call out anything that touches money, data migrations, scheduled jobs, or external integrations.

## Don't
- Don't upgrade dependencies or the runtime as part of an unrelated task.
- Don't delete code that looks unused without proving it's unused.
