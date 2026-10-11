# Vibe Coding Docs

**Don't vibe code your app until you've written these six documents.**

They give your AI coding agent (Claude Code, Cursor, Lovable, Bolt, Replit, ChatGPT…) a clear picture of what you're building, how it should work, and in what order — so it stops guessing.

You don't have to write them by hand. Each file below has a **ready-to-copy prompt**: paste it into Claude or ChatGPT, answer its questions about your idea, and it writes the document for you. Each file also has a **template** if you'd rather fill it in yourself.

| # | Document | What it answers |
|---|---|---|
| 1 | [PRD — Product Requirements](01-PRD.md) | What are we building, for whom, and which features? |
| 2 | [TRD — Technical Requirements](02-TRD.md) | Which stack, tools and APIs, and why? |
| 3 | [App Flow](03-APP-FLOW.md) | How does a user move through the app, screen by screen? |
| 4 | [UI/UX Design Brief](04-UI-UX-BRIEF.md) | What does it look and feel like? |
| 5 | [Backend Schema](05-BACKEND-SCHEMA.md) | How is the data stored, and who can see what? |
| 6 | [Implementation Plan](06-IMPLEMENTATION-PLAN.md) | In what order do we build it? |
| ★ | [Start Building](07-START-BUILDING.md) | The prompt that hands all six to your coding agent |

## How to use them

1. **Write them in order.** Each prompt asks you to paste in the documents before it, so they stay consistent — the TRD builds on the PRD, the schema on both, and so on.
2. **Save each one as a file in your project** — for example a `docs/` folder: `docs/PRD.md`, `docs/TRD.md`… Your agent reads them from there.
3. **Start the build with the [Start Building](07-START-BUILDING.md) prompt.** It makes the agent read everything and come back with a plan *before* writing any code.
4. **Keep them up to date.** When you change your mind about a feature, change the document first, then ask the agent to follow it.

## Tips that save the most time

- **Be specific about what's *not* in version 1.** Agents love to add features; an "out of scope" list stops them.
- **Make the agent ask, not assume.** Every prompt here tells the AI to ask you questions when something is unclear — answer them; that's where the good decisions come from.
- **Build in small phases.** One phase, test it, then the next. It's far easier to fix a small step than a whole app.
- **Ask for a plan before code — every time.** "Read the docs and tell me your plan first" is the single most useful sentence in vibe coding.

---

Free to use, copy and share. If it helped, tell someone else about it.
