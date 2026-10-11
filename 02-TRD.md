# 2. TRD — Technical Requirements Document

**What it is:** your technical decisions in one place — the stack (frontend, backend, database), hosting, tools, libraries and outside services/APIs, and the reasons for each.

**Why your agent needs it:** it's the blueprint. With it, the agent makes technical choices the way you want instead of picking a different framework every session.

---

## Copy this prompt into Claude or ChatGPT

```
You are a senior software architect. Help me write a TRD (Technical Requirements Document).

Here is my PRD:
[paste your PRD]

My experience level: [beginner / some coding / experienced]
Preferences or constraints: [e.g. "I want Next.js and Supabase", "must be free to host", "mobile app", or "no preference"]

First, ask me anything you need to decide well. Then recommend a stack that is simple, popular and well documented — prefer fewer moving parts over clever ones — and explain each choice in one line.

Write the TRD in Markdown with these sections:
1. Tech stack (frontend, backend, database, auth, file storage, hosting) with the reason for each
2. Libraries and services (payments, email, AI, maps…) with what each is used for
3. Architecture overview (how the parts talk to each other, in plain words)
4. Security and privacy (auth method, who can access what, how secrets/API keys are kept out of the code)
5. Environments and configuration (development vs production, the environment variables needed — names only, never values)
6. Performance and limits (expected users, file sizes, rate limits)
7. Testing approach
8. Coding conventions (folder structure, naming, language)
9. Rules for the AI agent (e.g. "ask before installing a new package", "never put secrets in code", "never change the database without showing me first")

Don't choose a tool just because it's new. If two options are close, pick the one with better documentation.
```

---

## Template

```markdown
# TRD: [App name]

## 1. Tech stack
| Layer | Choice | Why |
|---|---|---|
| Frontend | [e.g. Next.js + Tailwind] | |
| Backend | [e.g. Next.js server actions / Node API] | |
| Database | [e.g. Postgres (Supabase)] | |
| Auth | [e.g. Supabase Auth, email + password] | |
| File storage | [e.g. Supabase Storage] | |
| Hosting | [e.g. Vercel] | |

## 2. Libraries and services
- [Stripe] — payments
- [Resend] — emails
- [OpenAI / Anthropic API] — [what for]

## 3. Architecture overview
[Plain description: the browser talks to …, which reads from …, files go to …]

## 4. Security and privacy
- Who can read/write what: [e.g. users only their own records; admins everything]
- Secrets: kept in environment variables, never in code or chat.

## 5. Environments and configuration
- Development and production use separate databases.
- Environment variables: `DATABASE_URL`, `NEXT_PUBLIC_…` (names only)

## 6. Performance and limits
- [expected users, max upload size, etc.]

## 7. Testing
- [what gets tested and how]

## 8. Coding conventions
- [folder structure, naming, TypeScript, etc.]

## 9. Rules for the AI agent
- Ask before installing any new package.
- Show database changes before applying them.
- Never commit secrets.
```
