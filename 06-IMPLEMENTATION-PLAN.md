# 6. Implementation Plan

**What it is:** the exact step-by-step build order — which phase comes first, what's included in each, and how you'll know each step is done.

**Why your agent needs it:** asking an AI to "build the app" in one go produces a tangled mess. Small, ordered steps that each work on their own produce something you can actually ship.

---

## Copy this prompt into Claude or ChatGPT

```
You are a senior tech lead. Help me write the implementation plan for my app.

Here are my PRD, TRD, App Flow, UI/UX brief and Backend Schema:
[paste all five]

Break the build into small phases that each produce something working and testable. Order them so that foundations come first (project setup, design basics, database, sign-in) and each phase only depends on earlier ones.

Write it in Markdown:
1. Phase list — one line per phase
2. For each phase:
   - Goal (one sentence)
   - Steps — small enough that each is about one prompt to an AI coding agent
   - Files/areas it touches
   - Done when — a checklist I can test by hand
   - Risks or decisions to check with me before starting
3. Testing — what to test after each phase
4. Deployment — when and how to put it live, and what to set up (domains, environment variables, backups)
5. Version 2 ideas — things deliberately left for later

Keep phases small. Prefer "a working ugly version first, then polish" over polishing early.
```

---

## Template

```markdown
# Implementation Plan: [App name]

## Phases
0. Setup — project, styling, hosting, environments
1. Database and sign-in
2. Core feature: [name]
3. Second feature: [name]
4. Admin
5. Polish, testing and launch

## Phase 1 — Database and sign-in
- Goal: people can sign up, sign in and see an empty dashboard.
- Steps:
  1. Create the tables from the Backend Schema (migration file)
  2. Add access rules (row-level security)
  3. Sign up / sign in / sign out pages
  4. Protect signed-in pages; redirect to /login
- Touches: database migrations, auth pages, middleware
- Done when:
  - [ ] I can sign up, sign out and sign back in
  - [ ] A signed-out visitor opening /dashboard is sent to /login
  - [ ] One user can't see another user's data
- Check with me first: email verification on or off?

(repeat for each phase)

## Testing after each phase
- Click through the "Done when" list; fix before moving on.

## Deployment
- Deploy after Phase 1 to a preview link; go live after Phase 5.
- Production needs: its own database, environment variables set on the host, a backup schedule.

## Version 2 ideas
- [later features]
```

**Tip:** give your agent one phase at a time. Test it. Then the next.
