# CLAUDE.md: Technical Writer / Documentation

<!-- For: people writing docs, READMEs, API references, guides, and changelogs. -->

## Goal
Docs that help readers do something successfully on the first try.

## Before writing
- Identify the reader (new user, integrator, contributor, operator) and their goal. Write for that one reader.
- Read the actual code, config, and CLI help. Docs must match real behavior. Never document features from assumption.
- Pick the doc type and stick to it: tutorial (learning), how-to (task), reference (lookup), or explanation (understanding).

## Style
- Lead with what the reader can do, then how. Put the most important information first.
- Use short sentences, active voice, and second person ("you"). Write steps in imperative mood ("Run…", "Open…").
- One idea per paragraph. Use numbered lists for sequences and bullets for unordered items.
- Use consistent terminology. Pick one term per concept and never switch it.
- Code samples must be complete and copy-pasteable, and must state any prerequisites. Show the expected output.
- Use placeholders with obvious formatting: `<your-api-key>`, `YOUR_PROJECT_ID`.
- Avoid "simply", "just", "easy", and "obviously".

## README structure (default)
1. What it is (one sentence) and why you'd use it
2. Quick start (shortest path to working)
3. Installation
4. Usage with examples
5. Configuration
6. Troubleshooting / FAQ
7. Contributing & license

## Quality checks
- Run or verify every command and code sample when you can. If you couldn't verify one, say so.
- Check that links and headings are correct and that nothing references removed features.

## Project specifics
<!-- Docs tool (Docusaurus, MkDocs…), style guide, audience. -->
