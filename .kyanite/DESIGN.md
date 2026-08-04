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

1. MEMORY.md: user context, needs and preferences
2. DESIGN.md: architecture, principles and compliance rules
3. AGENT.md: behavior, decisions and error handling
4. CONVENTIONS.md: writing, file, commit and formatting standards

## Folders

- Core folders:
	- `Inbox`: unprocessed notes and files
	- `Actions`: actions captured directly or identified from `Inbox`
- Context-specific folders are defined in `MEMORY.md`; they belong to this vault and are not part of Kyanite's generic structure

## Actions

Actions are stored in `Actions` and follow TaskNotes semantics:

- `scheduled` is the next execution date
- `due` is a hard deadline

Actions past `due` are overdue and should be rescheduled or closed.

## Capture Flow

Raw emails, conversations and drafts enter through `Inbox` or chat; the assistant turns them into actions or references.

Each note stays monolingual (French or English).

## Assistant Integrations

Kyanite is assistant-agnostic. Assistant-specific integrations are optional and cannot override vault rules.

### GitHub Copilot

- Copilot auto-loads `.instructions.md`, which proxies `.kyanite/` rules
- Copilot memory lives outside the workspace under `/memories/` and maps to VS Code user data storage (User/globalStorage/github.copilot-chat)
- `/memories/repo/` is workspace-scoped; `/memories/session/` is session-scoped
- Copilot memory complements vault notes; it does not replace `.kyanite/` files

When a rule should stay visible and versioned for the vault, keep it in `.kyanite/` files and optionally mirror a concise reminder in assistant-specific memory.

## Design Choices

This section records implementation choices for `.kyanite/`; it documents the design and does not redefine it.

Update this file whenever user-requested evolutions change principles, boundaries, or operating rules.

### Configuration Boundaries

- Decision: keep `AGENT.md` generic and assistant-agnostic; it must not contain context-specific assumptions
- Decision: define Kyanite behavior only through the contents of `.kyanite/`
- Decision: put vault-specific behavior and context in `MEMORY.md`; keep domain content itself in the relevant vault notes
- Rationale: separate reusable workflow rules from context that belongs to this workspace

### Action Tracking Model

- Decision: use Obsidian TaskNotes for action tracking
- Rationale: properties-based metadata is more robust than inline task markup; standard Obsidian Bases views improve discoverability and maintenance
- Rejected: Obsidian Tasks plugin (less aligned with a properties-first model)

## Improvements

- Consider automated workflows through skills folder
- Consider a stricter caveman response mode for contexts requiring extreme brevity

