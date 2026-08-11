# MS Learn Docs Agent v2

An agent example for the GitHub Copilot harness that acts as a Microsoft Learn Documentation Assistant. It uses the Microsoft Learn MCP server as its primary source and provides accurate, current, and traceable answers based on official Microsoft documentation.

## Configuration

| Setting | Value |
| --- | --- |
| Name | MS Learn Docs Agent v2 |
| Runtime | Copilot Studio in the GitHub Copilot Harness |
| Model | GPT 5.6 Reasoning |
| System Prompt | Microsoft Learn Documentation Assistant |

## Description

Helps technical experts find, understand, and apply official Microsoft documentation. Searches the Microsoft Learn MCP server for authoritative sources and answers with inline links to the documentation used.

## Quick start

1. Open `agent/system-prompt.md` and copy only the content inside the `text` code block.
2. Create a new agent in Copilot Studio (GitHub Copilot Harness).
3. Select the GPT 5.6 Reasoning model.
4. Paste the content into the System Prompt / Instructions field.
5. Connect the Microsoft Learn MCP server as a tool.
6. Use the name and description from this README.

## Repository structure

```text
ms-learn-docs-agent-v2/
├── README.md
└── agent/
    ├── system-prompt.md
    └── system-prompt.txt
```

## Default agent boundaries

- Primary source: Microsoft Learn MCP server
- No answers from assumptions when no reliable source can be retrieved
- No invented features, commands, requirements, URLs, or limitations
- Responds in English unless the user requests another language

## Disclaimer

This repository is an independent example. It is not an official Microsoft product. Organizations remain responsible for validating licensing, privacy, and compliance requirements before deployment.
