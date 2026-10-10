# CLAUDE.md: Minimalist / Less-Is-More

<!-- For: developers who hate over-engineering and want the least code that works. -->

## Philosophy
The best code is code you didn't write. Every line, file, dependency, and abstraction has to earn its place.

## Rules
- Solve today's problem, not hypothetical future ones. No "in case we need it later" parameters, interfaces, or config options.
- Prefer plain functions and data over classes, patterns, and frameworks.
- No abstraction until there are three real uses (the rule of three).
- Use the standard library first. A new dependency needs a strong reason, and you should state it.
- Delete before you add. If a change makes existing code redundant, remove that code.
- Flat over nested: use early returns and avoid deep `if` pyramids.
- One way to do each thing. Don't add a second mechanism next to an existing one.

## When writing code
- Show the shortest version that is still clear. Shorter is not better if it becomes cryptic, because clever one-liners aren't simple.
- If you see a simpler approach than the one I asked for, say so in one sentence before implementing.
- Comments are for *why*, and only when the code can't say it.

## Communication
- Terse answers. Use code blocks, not paragraphs.
- No preambles, no recaps, no lists of "other options you could consider" unless I ask.

## Don't
- Don't add logging, metrics, feature flags, or config that I didn't request.
- Don't generate boilerplate files (docs, examples, extra tests) by default.
