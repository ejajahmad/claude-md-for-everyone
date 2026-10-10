# CLAUDE.md for Everyone

Ready-to-use `CLAUDE.md` files that set how Claude works for you, one per persona. Pick the one that sounds like you, copy it, fill in the last section, and you're done.

## How to use

1. Pick a persona file below.
2. Copy it to where Claude Code will read it:
   - **One project:** `<your-project>/CLAUDE.md`
   - **All projects (personal default):** `~/.claude/CLAUDE.md`
   ```bash
   cp coding/polished-production.md ~/my-app/CLAUDE.md
   ```
3. Fill in the final section (*Project specifics*, *About my level*, and so on). That's where you add your stack, commands, and context.
4. Edit freely. Delete rules you don't want, and add your own.

**Combining:** you can stack them. For example, put `learning/learn-while-building.md` in `~/.claude/CLAUDE.md` as your personal default, and add `coding/security-first.md` in a specific project. If two files conflict, the more specific (project) file should win, so say that explicitly when you merge them.

## Personas

### 💻 coding/
| File | For you if… |
|---|---|
| [pragmatic-coder](coding/pragmatic-coder.md) | You want correct code with no fuss. A good everyday default. |
| [polished-production](coding/polished-production.md) | You want senior-review-quality, production-ready code the first time. |
| [rapid-prototyper](coding/rapid-prototyper.md) | You're hacking an MVP or demo, and speed beats polish. |
| [minimalist](coding/minimalist.md) | You hate over-engineering and want the least code that works. |
| [test-driven](coding/test-driven.md) | You want tests first and every change proven. |
| [security-first](coding/security-first.md) | You handle auth, payments, personal data, or public endpoints. |
| [performance-tuner](coding/performance-tuner.md) | Latency, memory, or bundle size really matters. |
| [legacy-maintainer](coding/legacy-maintainer.md) | You work on an old, fragile codebase where stability is everything. |
| [code-reviewer](coding/code-reviewer.md) | You mainly want Claude to review PRs and diffs. |
| [solo-indie-hacker](coding/solo-indie-hacker.md) | You build and run products alone. |

### 🌱 learning/
| File | For you if… |
|---|---|
| [learn-while-building](learning/learn-while-building.md) | You want to build real things, keep the code simple, and understand every line. |
| [absolute-beginner](learning/absolute-beginner.md) | You've never coded before. |
| [socratic-tutor](learning/socratic-tutor.md) | You want hints and questions, not answers. |
| [career-switcher](learning/career-switcher.md) | You're moving into tech and need job-ready skills. |
| [student-academic-integrity](learning/student-academic-integrity.md) | You want coursework help that stays within integrity rules. |
| [interview-prep](learning/interview-prep.md) | You're preparing for coding, system design, or behavioral interviews. |

### 🍎 teaching/
| File | For you if… |
|---|---|
| [coding-instructor](teaching/coding-instructor.md) | You teach programming (bootcamp, university, workshops). |
| [school-teacher](teaching/school-teacher.md) | You teach K–12, any subject. |
| [course-creator](teaching/course-creator.md) | You design full courses or training programs. |

### ✍️ writing/
| File | For you if… |
|---|---|
| [technical-writer](writing/technical-writer.md) | You write docs, READMEs, and guides. |
| [content-writer](writing/content-writer.md) | You blog or write newsletters, and want it to sound human. |
| [academic-researcher](writing/academic-researcher.md) | You write papers and need rigor with no fabricated citations. |
| [editor-proofreader](writing/editor-proofreader.md) | You want your own writing improved, in your own voice. |

### 📊 data/
| File | For you if… |
|---|---|
| [data-analyst](data/data-analyst.md) | You use SQL, pandas, and dashboards, and need trustworthy numbers. |
| [ml-engineer](data/ml-engineer.md) | You train or evaluate models, or build LLM features. |

### 🧭 product/
| File | For you if… |
|---|---|
| [product-manager](product/product-manager.md) | You write PRDs, user stories, and specs. |
| [ui-designer-frontend](product/ui-designer-frontend.md) | You care about polished, accessible UI. |
| [startup-founder](product/startup-founder.md) | You're juggling product, code, and fundraising. |

### ⚙️ ops/
| File | For you if… |
|---|---|
| [devops-sre](ops/devops-sre.md) | You manage infrastructure, CI/CD, and production reliability. |
| [open-source-maintainer](ops/open-source-maintainer.md) | You maintain a public library or tool. |

### 🙂 everyday/
| File | For you if… |
|---|---|
| [non-technical-user](everyday/non-technical-user.md) | You're not a programmer but use Claude to get things done. |
| [busy-professional](everyday/busy-professional.md) | You want fast, high-signal answers and ready-to-send drafts. |

## Why these files work well with Claude

- **Specific over vague.** "Run the tests and report real output" works better than "be careful".
- **Reasons included.** Claude follows rules better when it knows *why* (for example, "this code may be thrown away").
- **Short and scannable.** Each file is loaded into every conversation, so every line has to earn its place.
- **Calm, direct tone.** No ALL-CAPS shouting. Claude follows plain instructions reliably, and over-emphasis makes it overcorrect.
- **A slot for your context.** The final section is where most of the value comes from, so fill it in.

## Contributing

Add a persona by copying an existing file in the closest category. Keep it under about 80 lines, put the audience in the top comment, and add a row to the table above.
