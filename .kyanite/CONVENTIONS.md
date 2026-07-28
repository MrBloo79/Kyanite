Standards and conventions for this workspace.

## Writing & Style

- Keep each note in one language: French or English, not mixed
- Use accents in French
- Use spaces only; indent with two spaces and never tabs
- Keep list items readable: concise but complete
- Omit final periods from short list items; use them in paragraphs and multi-sentence items
- No H1 headers (`#`); start with H2 (`##`) or content; filename serves as the title
- Blank line before bullet lists
- Use markup (bold, italic, etc) only when needed for emphasis or clarity
- Avoid special characters: emojis, arrows, em-dashes
- No space before punctuation (`:`, `;`, `?`, `!`), including in French
- No comma before `and` or `or`
- Join clauses with semicolons, colons or parentheses instead of dashes
- No placeholder sections for future content

## Filenames

- Use short, natural and readable names in the note language
- Do not use accents in file or directory names
- Name actions with an infinitive verb followed by a concrete object or expected result
- Do not put dates, statuses or tags in filenames; use frontmatter instead

Examples: `Reply to the insurance company.md`, `Book the vehicle inspection.md`

## Frontmatter

Frontmatter keeps notes findable and trackable across the vault. Every note starts with YAML frontmatter:

- `status`: new, active, shelved, next, waiting, done
- `created`: YYYY-MM-DD
- `modified`: YYYY-MM-DD
- `description`: optional short summary
- `tags`: `action` or `reference`
- `topics`: array of free-form tags for searchability
- `recipient`: optional array of people benefiting from the note or action

Keep shared frontmatter fields in this order: `status`, `created`, `modified`, `description`, `tags`, `topics`, `recipient`.

### Status

- `new`: just captured, not reviewed
- `active`: in use, maintained
- `shelved`: abandoned, may revisit
- `next`: prioritized as next action
- `waiting`: blocked on external input
- `done`: completed, archived

## Actions

Action frontmatter inserts `scheduled` and optional `due` after `modified`, continues with `description`, then places other action fields before `tags`. Actions use the TaskNotes plugin, which adds:

- `priority`: integer from 1 to 4; 1 low, 2 normal, 3 high, 4 top
- `scheduled`: YYYY-MM-DD; date when the action should be performed, not the capture date
- `due`: YYYY-MM-DD; hard deadline after which the action is overdue
- `projects`: array of wikilinks to related projects

Set `scheduled` to the next date on which the action should be performed. Set `due` only when a real deadline exists; keep it distinct from `scheduled`. Use today for a short or urgent action, the next working day for a normal action, and a later date when there is a known dependency or follow-up delay.

## References

- Use wikilinks syntax: `[[FILENAME]]`
- Use short paths without folder prefix (e.g., `[[DESIGN]]` not `[[.kyanite/DESIGN]]`)

## Commit Messages

- Inspect the repository status and relevant diff before suggesting a message; describe only the concrete changes concerned
- Use a concise English Conventional Commit
