# Contributing

## Change process

1. Create a branch from the current default branch.
2. Update the relevant Markdown and plain-text files.
3. Keep `agent/system-instructions.md` and `agent/system-instructions.txt` synchronized.
4. Recalculate the instruction character count.
5. Keep the final instructions below 8,000 characters.
6. Test the changed behavior with synthetic transcripts.
7. Update `CHANGELOG.md`.
8. Submit a pull request describing behavior changes and validation results.

## Prompt-quality requirements

- Use positive, direct instructions.
- State the reason or desired behavior where useful.
- Keep skills modular.
- Do not introduce exact trigger-phrase dependencies.
- Separate facts, implications, and recommendations.
- Do not solve instruction-length limits by placing behavioral instructions in knowledge sources.
- Avoid decorative emojis in agent instructions.
