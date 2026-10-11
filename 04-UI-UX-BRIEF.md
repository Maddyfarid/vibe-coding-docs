# 4. UI/UX Design Brief

**What it is:** the look and feel of your app — style, colour palette, typography, components, spacing, and roughly how each screen should be laid out.

**Why your agent needs it:** without direction, AI builds something generic, and every page ends up looking slightly different. A brief keeps the whole app consistent.

---

## Copy this prompt into Claude or ChatGPT

```
You are a senior product designer. Help me write a UI/UX design brief for my app.

Here are my PRD and App Flow:
[paste both]

The feel I want: [e.g. "calm and professional like Linear", "playful and colourful", "minimal, lots of white space"]
Apps or websites I like the look of: [list 2–3, or "none"]
Brand colours or logo: [describe, or "none yet"]

Ask me a few questions about style first. Then write the brief in Markdown:

1. Design direction — the personality in 3–5 words, and what to avoid
2. Colour palette — named colours with hex codes: background, surface/cards, text (primary, secondary), brand/primary, and success / warning / error; plus dark mode if wanted
3. Typography — fonts, and sizes for page titles, section titles, body text and small text
4. Spacing, corners and shadows — one spacing scale, corner radius, shadow style
5. Components — buttons (primary, secondary, danger), inputs, cards, tables, badges, dialogs, menus: how each should look and behave (hover, focus, disabled)
6. Layout — page structure (sidebar or top bar), max width, and how it adapts on mobile
7. Screen-by-screen layout — for each screen in the App Flow, a short description of what goes where
8. States — loading, empty, error and success, and how each looks
9. Accessibility — contrast, focus outlines, keyboard use, readable text sizes
10. Rules for the AI agent — e.g. "reuse existing components, never invent new colours, one primary button per screen"

Only use the colours and fonts defined here.
```

---

## Template

```markdown
# UI/UX Brief: [App name]

## 1. Design direction
- Personality: [calm, clear, trustworthy]
- Avoid: [gradients everywhere, tiny text, more than one accent colour]

## 2. Colours
| Name | Hex | Used for |
|---|---|---|
| Background | #F7F7F8 | page |
| Surface | #FFFFFF | cards |
| Text | #111827 | main text |
| Text muted | #6B7280 | secondary text |
| Primary | #2563EB | main buttons, links |
| Success | #16A34A | |
| Warning | #D97706 | |
| Error | #DC2626 | |

## 3. Typography
- Font: [Inter]
- Page title 28px bold · Section 18px semibold · Body 15px · Small 13px

## 4. Spacing, corners, shadows
- Spacing scale: 4, 8, 12, 16, 24, 32
- Corners: 12px on cards, 8px on buttons/inputs
- Shadow: one soft shadow on cards only

## 5. Components
- Primary button: filled Primary, white text; hover slightly darker; disabled 50% opacity
- Inputs: 40px tall, 1px border, Primary border on focus
- Tables: header row in muted text, row hover background

## 6. Layout
- Left sidebar on desktop, top bar with menu on mobile; content max width 1200px

## 7. Screens
- Dashboard: title + "New" button top right; 3 stat cards; recent items list below

## 8. States
- Loading: grey placeholder rows · Empty: icon + one line + button · Error: red message + retry

## 9. Accessibility
- Text contrast at least 4.5:1; visible focus outline; everything usable by keyboard

## 10. Rules for the AI agent
- Use only these colours and fonts. Reuse components. One primary action per screen.
```
