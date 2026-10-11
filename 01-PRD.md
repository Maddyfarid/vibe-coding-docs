# 1. PRD — Product Requirements Document

**What it is:** the "what and why" of your app. Every feature you're building, who it's for, and a short overview of the whole idea. It's the document every other one builds on.

**Why your agent needs it:** without it, the AI invents features you didn't ask for and misses the ones you did.

---

## Copy this prompt into Claude or ChatGPT

```
You are a senior product manager. Help me write a PRD (Product Requirements Document) for my app.

My app idea: [describe your app in 2–5 sentences]

Before writing anything, ask me questions — one group at a time — until you clearly understand:
- who the users are and what problem it solves for them
- the core features for version 1, and what is NOT in version 1
- the user roles (e.g. guest, user, admin) and what each can do
- what success looks like

Then write the PRD in Markdown using exactly these sections:
1. Overview (the app in one paragraph)
2. Problem and goals
3. Target users and roles
4. Features for version 1 — for each: name, description, user story ("As a … I want … so that …") and acceptance criteria (a checklist that says when it's done)
5. Out of scope for version 1
6. Rules and constraints (privacy, legal, money, permissions)
7. Success metrics
8. Open questions

Keep it plain and specific. Don't invent features I haven't confirmed — list them under Open questions instead.
```

---

## Template

```markdown
# PRD: [App name]

## 1. Overview
[One paragraph: what the app is, who it's for, and the main thing it does.]

## 2. Problem and goals
- Problem: [what's painful today]
- Goals: [what the app must achieve]

## 3. Target users and roles
| Role | Who they are | What they can do |
|---|---|---|
| [Visitor] | | |
| [User] | | |
| [Admin] | | |

## 4. Features (version 1)
### Feature: [name]
- Description: [what it does]
- User story: As a [role], I want [action] so that [benefit].
- Acceptance criteria:
  - [ ] [specific, testable condition]
  - [ ] [another one]

(repeat for each feature)

## 5. Out of scope (version 1)
- [things we are deliberately NOT building yet]

## 6. Rules and constraints
- [e.g. users only see their own data; payments in USD only; must work on mobile]

## 7. Success metrics
- [e.g. a new user can sign up and create their first project in under 2 minutes]

## 8. Open questions
- [anything not decided yet]
```

**Tip:** the acceptance criteria are gold. Your agent can test its own work against them.
