# Meeting Summary Agent

A reusable, instruction-only template for Agent Builder in M365 Copilot. Users upload a meeting transcript or paste meeting notes into the current conversation. The agent creates summaries, decisions, action items, risks, recommendations, and follow-up communication without configured organizational knowledge sources.

## Design goals

- Ready to copy into Agent Builder in M365 Copilot
- No dependency on Work IQ
- No permanent knowledge sources
- No SharePoint, OneDrive, Teams, Outlook, People, or connector grounding
- No actions or optional AI capabilities required
- Modular skills that companies can remove or adapt
- Grounded only in the uploaded transcript and current conversation
- Instructions kept below the 8,000-character limit

## Repository structure

```text
meeting-summary-agent/
├── README.md
├── LICENSE
├── CHANGELOG.md
├── CONTRIBUTING.md
├── SECURITY.md
├── .gitignore
├── agent/
│   ├── system-instructions.md
│   ├── system-instructions.txt
│   ├── description.md
│   └── starter-prompts.md
├── configurator/
│   └── configuration-quiz.md
├── templates/
│   └── company-configuration.md
├── examples/
│   ├── example-transcript.md
│   └── example-output.md
└── docs/
    ├── setup-guide.md
    └── design-decisions.md
```

## Quick start

1. Open `agent/system-instructions.md`.
2. Copy only the content inside the `text` code block.
3. Create an agent in Agent Builder in M365 Copilot.
4. Paste the content into the Instructions field.
5. Use the name and description from `agent/description.md`.
6. Do not add knowledge sources or optional capabilities for the default instruction-only design.
7. Add selected prompts from `agent/starter-prompts.md`.
8. Test with the synthetic transcript in `examples/example-transcript.md`.

## Customize the agent

Use `configurator/configuration-quiz.md` in Copilot. Answer the quiz and receive adapted instructions with a target size below 7,700 characters.

For manual configuration, complete `templates/company-configuration.md` and adjust only the relevant skill sections.

## Character validation

Current instruction file:

- Unicode characters: 7477
- UTF-8 bytes: 7519
- Agent Builder limit: 8,000 characters
- Validation date: 2026-07-27

Always validate the final pasted version after customization. Different editors can normalize quotation marks and line endings.

## Default agent boundaries

The default template does not use or assume access to:

- Work IQ
- SharePoint or OneDrive
- Teams meetings or messages
- Outlook email
- People data
- Copilot connectors
- Websites
- Actions
- Code Interpreter
- Image Generator

The uploaded transcript and user-provided context are the factual sources.

## License

Released under the MIT License. See `LICENSE`.

## Disclaimer

This repository is an independent template. It is not an official Microsoft product. Organizations remain responsible for validating licensing, privacy, compliance, retention, works council, and data-processing requirements before deployment.
