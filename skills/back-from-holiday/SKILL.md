---
name: back-from-holiday
description: Creates an interactive, self-contained HTML recap dashboard after a longer absence (vacation, sabbatical, sick leave). Surfaces missed emails, meetings, Teams messages, files, pending decisions, deadlines, and top priorities — with checkboxes, dark mode, filters, and browser-persisted state. Works fully autonomously without follow-up questions.
---

# Back from Holiday — Recap Dashboard Skill

This skill generates a complete "what did I miss" recap as a single offline-capable HTML dashboard.

## When to use

- Returning from vacation, sabbatical, or any longer absence
- Also works as a weekly digest when the time period is shortened

## How to use

1. Pick your language: [prompt-de.md](prompt-de.md) (German) or [prompt-en.md](prompt-en.md) (English).
2. Fill in the **WHO I AM** section (role, organization, responsibilities). Optionally fill **TIME PERIOD** and **MY FOCUS AREAS** — if left empty, the prompt derives them automatically and marks them as "automatically detected".
3. Optionally attach your company logo so brand colors are picked up.
4. Start a new task in your assistant and paste the full prompt.
5. Wait a few minutes — the result is a single HTML file that works offline.

## Compatibility

| Target | Notes |
|---|---|
| **Copilot Cowork (M365 Copilot)** | Full experience. Reads Outlook, Calendar, Teams, SharePoint, and OneDrive directly via work data grounding. |
| **Claude Cowork** | Requires the Microsoft 365 / Outlook / Teams connectors (or uploaded exports of mail and calendar data). Data-access steps degrade gracefully if a source is not connected; gaps are flagged in the dashboard instead of being guessed. |
| **Microsoft Scout** | Works with the same prompt. If a specific data source is unavailable in Scout, the prompt marks that section as a gap rather than inventing facts. |

The prompt is explicitly read-only: it never sends, edits, or deletes anything.

## Customization ideas

- **Shorter absence:** reduce the time period; step 6 ("decisions made in my name") can usually be dropped.
- **Different role:** swap the urgency criteria in step 1 — e.g., quotes and customer inquiries for sales, incidents and changes for IT.
- **Weekly instead of post-vacation:** set the period to seven days and schedule it as a recurring task.
- **No Teams or SharePoint:** simply delete the corresponding step.

## Notes

- Without a transcript or minutes, a meeting cannot be summarized — the dashboard states this openly instead of guessing.
- Always verify results before acting on them.
