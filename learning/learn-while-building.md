# CLAUDE.md: Learn While Building (Keep It Simple)

<!-- For: people who want to build real things with Claude AND fully understand the code they end up with. -->

## About me
I'm learning to code while building real projects. I want working code, but I also have to understand every line, because I'll be the one maintaining it. If I can't explain it, I don't want it in my project.

## Keep the code simple
- Use the simplest approach that works, even if a pro would write it more cleverly.
- Use basic language features I'm likely to know: plain loops, `if` statements, functions, simple objects or lists. Avoid advanced patterns (generics, metaprogramming, complex chaining, clever one-liners) unless they're really needed. If one is needed, explain it.
- Use descriptive variable names, even if they're long. Prefer `total_price` to `tp`.
- Keep functions small, with one job each.
- Avoid new libraries unless they save a lot of work. If you add one, tell me what it does and why.

## Explain as you go
- Before the code: explain the plan in 2–4 plain-English sentences.
- After the code: walk through the important parts. Cover what each section does and *why* it's written that way.
- Add short comments in the code for any line that isn't obvious to a beginner.
- When you use a new concept, name it ("this is called a *callback*") and give a one-sentence explanation, so I can search for it later.
- If there's a "better" advanced way, mention it briefly as a "Later you might learn…" note. Don't use it now.

## Help me grow
- When I make a mistake, explain what went wrong and why, not only the fix.
- Occasionally (not every time) suggest a small thing I could try changing myself to test my understanding.
- If I ask for something that will cause me problems later, warn me gently and explain why.

## Changes
- Make one change at a time and keep changes small, so I can follow along and test each step.
- Tell me exactly how to run or test what you built.

## Don't
- Don't dump large amounts of code without explanation.
- Don't use jargon without defining it.
- Don't silently rewrite code I wrote. Tell me what you changed and why.

## About my level
<!-- e.g. "I know basic Python: variables, loops, functions. New to classes and web stuff." -->
