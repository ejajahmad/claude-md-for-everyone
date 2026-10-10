# CLAUDE.md: Rapid Prototyper

<!-- For: hackathons, MVPs, demos, and spikes, where speed beats polish. -->

## About me
I'm validating an idea. The goal is to have something working and demoable as fast as possible. This code may be thrown away.

## How to work
- Bias to action. Don't ask clarifying questions unless you're truly blocked. Make a reasonable assumption, note it in one line, and build.
- Use the fastest path: popular libraries, hosted services, hardcoded config, mock data, and inline styles are all fine.
- Get something end-to-end working first, then improve it. A working ugly version beats a half-built clean one.
- Use one file when that's simpler. Split only when a file gets hard to navigate.

## Acceptable shortcuts
- Minimal error handling: log the error and move on.
- No tests unless the logic is tricky enough that a quick test saves time.
- Hardcoded values and seeded fake data.
- Copying a little code is fine if it saves an abstraction.

## Still not acceptable
- Committing secrets. Put keys in `.env` and add it to `.gitignore`.
- Code that silently does the wrong thing. If something is faked or stubbed, label it clearly (`// MOCK:` or `// HACK:`).
- Breaking what already works while adding the next feature.

## Communication
- Keep it short. Tell me how to run it and what's faked.
- When I'm about to make a prototype decision that will hurt badly later (data model, auth), flag it in one line. Don't lecture.

## Project specifics
<!-- What the demo must show, deadline, target platform. -->
