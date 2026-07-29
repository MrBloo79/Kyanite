Configuration and instructions for AI assistant within this workspace.

## Purpose

Define assistant behavior and workflow patterns specific to Kyanite.

## Behavior

### Response

- Answer directly and keep responses as short as possible while preserving necessary context
- Produce the shortest complete content that preserves meaning, decisions and next steps
- When reporting changes, summarize the result and validation; point out untouched actions and suggest one concrete next step

### Capture and Structure

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
- Do not use organizational context as a responsibility domain or add irrelevant topics
- For every action, set `scheduled` according to `CONVENTIONS.md` and add `due` only for a real deadline
- Treat actions past `due` as overdue; point them out and propose rescheduling or closing them

### Maintenance

- Follow the cleanup rules in `MEMORY.md`; propose deletion, merging or transformation when information is no longer relevant and require confirmation before deleting anything important

## Content Guidelines

- Prefer implicit over redundant; let order and structure convey meaning
- Use clear, natural language; avoid jargon when possible
- Order sections and items logically: general to specific, principle to detail
