Configuration and instructions for AI assistant within this workspace.

## Purpose

Define assistant behavior and workflow patterns specific to Kyanite.

## Behavior

### Response

- Answer directly and keep responses as short as possible while preserving necessary context
- Produce the shortest complete content that preserves meaning, decisions and next steps
- When reporting changes, summarize the result and validation; point out untouched actions and suggest one concrete next step

### Capture and Structure

### Memory hierarchy

- Use `.kyanite/MEMORY.md` as the canonical workspace memory shared across assistants
- When the user asks to remember something for later, update `.kyanite/MEMORY.md` unless another location is explicitly requested
- Treat the assistant's technical persistent memory as internal operating context only; do not use it as a substitute for workspace memory
- Before any memory-related action, read `.kyanite/MEMORY.md` and apply its filtering and retention rules
- Do not create a root-level `MEMORY.md`, duplicate workspace memory elsewhere or create `.github/` for this purpose

- Accept raw emails, conversations and drafts from `Inbox` or chat
- Filter each capture against `MEMORY.md`; keep related content here, propose another vault for unrelated content and discard the rest
- Capture raw notes in `Inbox` and actions in `Actions`; do not add wikilinks to `Inbox` notes
- Transform captures into actions or domain notes; rewrite them according to `CONVENTIONS.md` and add links only after transformation
- If an assistant-specific shortcut conflicts with vault conventions, follow `.kyanite/` conventions first
- Choose the most relevant directory and group related notes when useful
- Keep operational resources close to the references they support, preferably in the same folder
- Use the folder-note practice: each functional folder has a same-named index note explaining its scope, contents and related resources
- Make folders self-discoverable without relying on an external or explicit hierarchy

### Actions and Topics

- Set `tags` to `action` or `reference` in frontmatter
- Set `topics` as an array of free-form keywords; include a responsibility domain from the applicable `MEMORY.md` when the note belongs to one
- Do not add responsibility domains beyond those defined in `MEMORY.md`, or irrelevant topics
- For every action, set `scheduled` according to `CONVENTIONS.md` and add `due` only for a real deadline
- Treat actions past `due` as overdue; point them out and propose rescheduling or closing them

### Maintenance

- Follow the cleanup rules in `MEMORY.md`; propose deletion, merging or transformation when information is no longer relevant and require confirmation before deleting anything important
- When reviewing or evolving Kyanite, ask whether the instructions contain inconsistencies, contradictions, unresolved tensions or ambiguities; record or resolve the finding in the appropriate `.kyanite/` file

## Content Guidelines

- Prefer implicit over redundant; let order and structure convey meaning
- Use clear, natural language; avoid jargon when possible
- Order sections and items logically: general to specific, principle to detail
