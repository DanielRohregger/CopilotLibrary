---
name: meeting-dictation
description: Captures a user's dictated personal action items during an unrecorded meeting, reviews them for approval, then creates or updates personal Outlook calendar reminders one at a time. Use when someone wants low-interruption task capture followed by controlled Outlook reminders.
---

# Meeting Dictation — Personal Task Reminders

Capture personal action items dictated into chat during a meeting, then review and create Outlook calendar reminders with explicit approval at every write step.

## When to use

- You are in an unrecorded meeting and want to dictate your own action items without interruption.
- You want each approved task represented by a separate personal Outlook calendar item with a reminder.

## How to use

1. Choose [prompt-de.md](prompt-de.md) for German or [prompt-en.md](prompt-en.md) for English.
2. Copy the complete prompt into a new chat with an assistant that can access your Outlook calendar.
3. Dictate tasks while the meeting is in progress, then use the prompt's localized completion and approval commands.

## Compatibility and limitations

- A deeper reasoning or analysis mode is recommended when the host offers one; it must not reveal chain-of-thought.
- This skill does not record or transcribe the meeting. It processes only tasks that you dictate into chat.
- Phase 3 requires permission and capability to create and update personal Outlook calendar items with reminders. Without it, phases 1 and 2 still work; the assistant must report phase 3 as unavailable and must not claim a write succeeded.
- Do not dictate sensitive content unless doing so is appropriate for your environment and its data-handling policies.
