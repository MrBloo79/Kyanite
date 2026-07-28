Architecture and design decisions for Kyanite.

## Principles

Kyanite follows these principles:

- Assistant-agnostic: Works with any AI assistant; no vendor lock-in
- Transparent: Configuration is tracked and visible
- Simple: Uses the simplest structure that supports the workflow
- Self-cleaning: Resists accumulation and stays organized
- Self-updating: Integrates changes, flags conflicts and refactors when needed

## Files & Purpose

Files load in this order:

1. MEMORY.md: User context, needs and preferences
2. DESIGN.md: Architecture, principles and compliance rules
3. AGENT.md: Behavior, decisions and error handling
4. CONVENTIONS.md: Writing, file, commit and formatting standards

## Folders

- `Inbox`: Unprocessed notes and files
- `Actions`: Actions captured directly or identified from `Inbox`

## Actions

Actions are stored in `Actions` and managed with TaskNotes; their fields are defined in CONVENTIONS.md.

Actions use `scheduled` for their next execution date and may use `due` for a hard deadline; both are defined in CONVENTIONS.md.

## Capture Flow

Raw emails, conversations and drafts enter through `Inbox` or chat; the assistant turns them into actions or references.

## Ameliorations

- Enable cross-assistant compatibility with assistant-specific overrides
- Consider automated workflows through skills folder
- Consider a stricter caveman response mode for contexts requiring extreme brevity

