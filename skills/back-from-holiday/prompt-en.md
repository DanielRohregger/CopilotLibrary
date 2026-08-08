# Vacation Recap Dashboard — Copy-Ready Prompt (English)

A prompt for Copilot Cowork, Claude Cowork, and Microsoft Scout that automatically builds an interactive HTML dashboard after a longer absence: emails, meetings, Teams, files, open decisions, and priorities — with checkboxes, dark mode, and filters.

It runs end to end without asking follow-up questions. The result is a single HTML file that also works offline.

---

## What you need to customize

| Place in the prompt | What goes there | Required? |
|---|---|---|
| **WHO I AM** | Your role, your company or department, and your areas of responsibility. The more precise, the better the prioritization. | Yes |
| **TIME PERIOD** | Duration of your absence. Default is three weeks. | Only if different |
| **MY FOCUS AREAS** | Your 3–5 most important projects and topics. | No — see below |
| **DESIGN** | Attach your company logo to the task and its brand colors will be used. Without a logo, a neutral scheme applies. | No |

**If you leave the focus areas empty**, the prompt runs in standard mode: it derives your topics automatically from your role profile, your personalization, and the actual volume during the period — and marks them in the dashboard as "automatically detected" so you can review them once.

## How to use it

1. Copy the entire prompt
2. Start a new task in Copilot Cowork, Claude Cowork, or Microsoft Scout
3. Optionally attach your company logo
4. Send it — the analysis takes a few minutes; you can close the window

**Note for Claude Cowork and Microsoft Scout:** For the email, calendar, Teams, and file steps to work, the corresponding Microsoft 365 connections (connectors) must be set up. If a source is missing, the prompt flags it in the dashboard as a gap instead of guessing.

---

## The prompt

```text
WORKING MODE (IMPORTANT, READ FIRST)
Complete this task fully and autonomously. Do not ask me any follow-up questions. Do not wait for confirmations. Work through all steps in order and stop only when the finished dashboard has been created. If information is missing, make a reasonable assumption, mark it in the output, and keep going. Do not invent facts: anything you cannot find in my data must be flagged as a gap. You work strictly read-only: you do not modify, send, or delete anything.

WHO I AM
I am [YOUR ROLE, E.G. MEMBER OF THE EXECUTIVE BOARD] at [COMPANY OR DEPARTMENT]. I am responsible for [YOUR AREAS OF RESPONSIBILITY, E.G. HR, PROCUREMENT, PRODUCTION, BUDGET, APPROVALS, ESCALATIONS]. I was on vacation for [TIME PERIOD, E.G. THREE WEEKS] and return today.

YOUR TASK
Give me a complete overview of what I missed during my absence and tell me clearly where I need to act. Use all data sources connected to you (email, calendar, Teams/chats, SharePoint, and OneDrive). If a source is unavailable or not connected, do not silently skip the related step — explicitly flag the missing source as a gap in the dashboard.

TIME PERIOD
My entire absence up to today, at least the last three weeks. State the concrete start and end date you use in the dashboard.

MY FOCUS AREAS
- Projects and topics: [OPTIONAL: LIST YOUR 3-5 MOST IMPORTANT PROJECTS]
- Internal topics I want to track: [OPTIONAL: LIST ADDITIONAL TOPICS]

IF THESE FIELDS ARE EMPTY OR STILL CONTAIN PLACEHOLDERS:
Do not ask. Automatically work in standard mode. Derive my focus areas yourself from:
- my stored personalization, my role and leadership profile, and my saved instructions,
- my areas of responsibility,
- the topics that actually had the highest volume, the most participants, or the greatest urgency during the period.
Visibly mark the focus areas derived this way as "automatically detected" in the dashboard so I can review them.

STEP 1 - EMAILS
Review my inbox for the period. Classify each relevant email into exactly one of these levels:
1. URGENT - immediate action required (approvals, escalations, deadlines, complaints, open decisions, questions addressed directly to me)
2. MEDIUM - handle this week
3. LOW - can wait, but must not be forgotten
4. NO ACTION NEEDED - for information only
Filter out as irrelevant and summarize only as counts: newsletters, advertising, system messages, automatic notifications, and confirmations.
For each email provide: sender, subject, date, a one-line summary, what is expected from me, and a direct link to the email.
Highlight in particular: matters that someone else took over during my absence, and those that were left unattended.

STEP 2 - APPOINTMENTS AND MEETINGS
Check my calendar for the period. List the meetings that took place and are relevant to me - especially my recurring meetings and staff meetings.
For each meeting, check whether a transcript, recording, or minutes exist.
- If yes: summarize the highlights in at most five bullet points - topics discussed, decisions made, agreed tasks with owners and dates, and open points. Link the source.
- If no: explicitly write "no transcript available" and tell me who I should contact for a follow-up.

STEP 3 - MICROSOFT TEAMS
Review my Teams chats and channels for the period.
- Which unread messages and channel posts do I have?
- Prioritize the colleagues I work with most frequently, as well as messages in which I was mentioned by name or addressed directly.
- Briefly summarize per person and channel what it was about, and flag everything that expects a reply from me.

STEP 4 - FILES IN SHAREPOINT AND ONEDRIVE
Check which documents relevant to me were created or modified during the period.
For each file provide: name, who last edited it, when, why it might be relevant, plus a link. Map them to my focus areas where possible.

STEP 5 - WHAT I OWE AND WHO IS WAITING FOR ME
- Who is waiting for a reply, an approval, or a decision from me? Sort by waiting time.
- Which deadlines expired during my absence? What are the consequences?
- Which commitments did I make before the vacation that are now due?
- Are there new tasks that were assigned to me?

STEP 6 - WHAT HAPPENED IN MY NAME
- Which decisions were made during my absence that fall within my area of responsibility?
- Was anything approved or decided on my behalf by a deputy? Which of these do I need to review or confirm?
- Are there topics from the period that I need to know about as a leader?

STEP 7 - WHAT IS COMING UP TODAY AND THIS WEEK
- My meetings today with time, participants, and - where available - the outcome of the last occurrence of the same meeting.
- My meetings for the rest of the week.
- Where do I need to prepare? State concretely what I should read or decide beforehand.

STEP 8 - THE SYNTHESIS
Derive from everything above:
- The five most important things I must tackle today - in the order I should approach them, with reasoning.
- The most important decisions now expected from me.
- Open commitments and deadlines falling due within the next ten days.
- Anything that looks like risk, escalation, or conflict - even if it was only hinted at.
- Explicitly also: what I can safely ignore or delete. Relief is just as valuable as a task list.

STEP 9 - THINK AHEAD YOURSELF
Independently consider what else a truly good vacation recap needs in my role, and add it where sensible. Think about things like: conspicuous clustering of a topic, moods in conflicts, announced follow-ups that never arrived, customers or partners from whom there was unusually much or unusually little, and opportunities that were left lying. Clearly mark everything you add yourself as your own suggestion.

OUTPUT - THE DASHBOARD
Produce the result as a standalone HTML file to open in the browser. Structure in this order:
1. Header: title, time period, creation date, and three to five key metrics at a glance (e.g., total emails, of which relevant, open decisions, expired deadlines).
2. Executive summary: the situation in at most ten lines. What matters most?
3. My top priorities today: the five most important actions as a traffic-light block.
4. Then the detail sections in this order, each clearly separated and with the count in the section title: Emails, Meetings, Teams, Files, Who is waiting for me, Decided in my name, Today and this week, Your additions.

DESIGN
- Modern, light, clean layout. Plenty of whitespace, clear typography, calm structure, easy to read on screen and in print.
- The company logo is attached to this task. Extract the brand colors from it and use them consistently for the header, headings, accents, and table headers. Place the logo subtly in the header. If no logo is attached, use a restrained, professional blue-grey scheme.
- Status colors in addition to the brand color: red means urgent, yellow means medium, green means done or no action needed.
- Use cards and tables instead of long paragraphs. Every entry gets a direct link to its source.
- Language: English, factual, concise. No filler phrases, no repetition.

INTERACTIVE FEATURES (please implement all of them)
1. Checkboxes: every task, every open decision, and every message to be answered gets a checkbox. Checked entries are visibly shown as done, for example greyed out and struck through. Show a progress bar at the top with the number of completed versus total tasks.
2. Dark mode: a clearly visible toggle in the top right between light and dark mode. Both variants must be consistently easy to read with sufficient contrast.
3. Mark as not relevant: every entry you suggested or derived yourself additionally gets a "not relevant" button. With it, I remove the entry from the active list. Hidden entries are not deleted but moved to a collapsible section "Marked as not relevant" and can be restored from there.
4. Remember state: persist the state of checkboxes, dark mode, and hidden entries in the browser, so my choices survive when I reopen the file.
5. Additionally helpful: a simple filter bar that lets me show only the urgent items or only the open items.
The entire file must work without an internet connection: HTML, CSS, and JavaScript in a single file, no external dependencies.

QUALITY RULES
- Visibly flag when information is missing or uncertain. Better to show a gap than to present a guess as fact.
- Clearly separate verified facts from my data from your own assessments.
- No follow-up questions to me. Work through until the dashboard is finished.

Finally, summarize in the chat in five sentences what I should do first.
```

---

## Customization ideas

- **Shorter absence:** reduce the time period; step 6 can usually be dropped.
- **Different role:** swap the urgency criteria in step 1 — e.g., quotes and customer inquiries for sales, incidents and changes for IT.
- **Weekly instead of post-vacation:** set the period to seven days and schedule it as a recurring task.
- **No Teams or SharePoint:** simply delete the corresponding step.

## Notes

- The prompt only reads what is already shared with you. It changes nothing and sends nothing.
- Without a transcript or minutes, a meeting cannot be summarized — the dashboard states this openly instead of guessing.
- Always double-check results before turning them into decisions.
