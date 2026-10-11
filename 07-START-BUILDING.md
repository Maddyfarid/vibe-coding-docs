# ★ Start Building — hand the documents to your coding agent

Once your six documents are saved in your project (for example in a `docs/` folder), start every new build with this prompt. It makes the agent read everything and come back with a plan **before** it writes a single line of code — the habit that saves the most time and the most mistakes.

---

## The first prompt

```
Read these documents in full before doing anything:
- docs/PRD.md
- docs/TRD.md
- docs/APP-FLOW.md
- docs/UI-UX-BRIEF.md
- docs/BACKEND-SCHEMA.md
- docs/IMPLEMENTATION-PLAN.md

Then, before writing any code, report back with:
1. Your understanding of the app in a few sentences
2. Anything unclear, missing or contradictory between the documents — as questions for me
3. Your plan for Phase 1 of the Implementation Plan: the steps, the files you'll create, and any packages you want to install (and why)

Wait for my approval before you start.

Rules for the whole project:
- Follow the documents. If something in them seems wrong, ask me — don't silently change it.
- Ask before installing any package.
- Show me any database change before applying it.
- Never put secrets or API keys in code or in chat.
- Work one phase at a time. At the end of each phase, tell me exactly how to test it.
```

## For each next phase

```
Phase [N] is tested and working. Re-read the documents for Phase [N+1] and tell me your plan before you start: the steps, the files, any new packages, and any decisions you need from me.
```

## When something breaks

```
This isn't working: [what you did, what you expected, what happened — paste any error].
Find the cause before changing anything. Explain it in plain words, then propose the fix and wait for my go-ahead.
```

## When you change your mind

```
I've updated docs/[document].md: [what changed]. Read the change, tell me what it affects in the code we've already built, and propose how to update it.
```
