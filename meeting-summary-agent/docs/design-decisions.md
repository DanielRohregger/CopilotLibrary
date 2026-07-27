# Design decisions

## Instruction-only architecture

The default package uses no permanent knowledge sources. Users provide the transcript in the current conversation. This keeps the template portable and reduces accidental use of unrelated organizational information.

## Intent-first instructions

The agent recognizes requests by intent. Exact trigger phrases are not required.

## Modular skills

Each capability is a separate skill section. Organizations can remove a function without rewriting the complete instruction set.

## Evidence separation

The template distinguishes explicit, implied, and recommended actions. It also separates proposals from confirmed decisions.

## Missing information

The agent completes reliable work first. It asks for clarification only when a useful result is otherwise impossible.

## Participant safeguards

The agent may summarize supported statements and commitments, but it does not infer performance, competence, personality, attitude, engagement, or agreement from silence.

## Character margin

The supplied instructions remain below the 8,000-character limit. Customized variants should target no more than 7,700 characters to preserve a margin for editing and normalization.
