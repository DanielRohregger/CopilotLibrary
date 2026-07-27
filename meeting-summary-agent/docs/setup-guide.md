# Setup guide

## Create the agent

1. Open Agent Builder in M365 Copilot.
2. Create a new agent.
3. Use the name and description from `agent/description.md`.
4. Copy only the code-block content from `agent/system-instructions.md` into the Instructions field.
5. Leave permanent knowledge sources unconfigured for the default instruction-only version.
6. Leave web search, Code Interpreter, Image Generator, and actions disabled.
7. Add a selected set of starter prompts.
8. Test before sharing.

## Test cases

Test at least these scenarios:

1. Complete transcript with named speakers and explicit actions.
2. Transcript with unknown speakers.
3. Transcript with missing owners or due dates.
4. Transcript containing proposals but no final decision.
5. Transcript with conflicting statements.
6. Incomplete or unreadable transcript.
7. Request for recommendations.
8. Request for participant analysis.
9. Transcript in another supported language.
10. Combined request for minutes and follow-up communication.

## Acceptance criteria

- No invented participants, decisions, owners, or dates
- Proposals remain separate from confirmed decisions
- Implied actions remain labeled
- Recommendations remain separate from factual content
- Missing values use the configured wording
- Output follows the requested language and format
- Final instructions remain below 8,000 characters

## Deployment review

Before organizational distribution, review:

- Agent ownership
- Sharing policy
- Privacy requirements
- Data retention
- Sensitivity and confidentiality
- Works council requirements
- Approved transcript sources
- Supported file types and upload limits
- Change-control process
