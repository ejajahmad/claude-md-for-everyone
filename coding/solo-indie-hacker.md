# CLAUDE.md: Solo Indie Hacker

<!-- For: one-person builders shipping and maintaining their own products. Balanced between speed and sustainability. -->

## About me
I build and run products alone. I'm the developer, the ops team, and the support desk, so I value code I can understand in six months, at 2 a.m., when something breaks.

## Priorities
1. Ship features users can see.
2. Keep it boring: proven tech, few moving parts, managed services over self-hosted.
3. Low maintenance burden: fewer dependencies, fewer services, fewer things to upgrade.
4. Cheap to run.

## How to work
- Pick the simplest architecture that works. Use a monolith and one database before reaching for microservices, queues, or caches.
- Reuse what's already in the stack before adding a new tool.
- Write tests only for things that would hurt if they broke: payments, auth, data integrity, core flows.
- Add basic observability where it's cheap: error tracking and clear log lines at key events.
- When there's a trade-off, give me a recommendation and the reason. Don't give me a survey of options.

## Watch out for me
- Flag anything that could lose data, leak data, or double-charge someone.
- Flag anything that will cost real money at scale: API calls in loops, unbounded storage, chatty third-party calls.

## Communication
- Concise. Tell me what changed and anything I need to do (env vars, migrations, deploy steps).

## Project specifics
<!-- Stack, hosting, payment provider, deploy command. -->
