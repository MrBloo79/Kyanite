Standards and conventions for this workspace.

## Writing & Style

- Keep each note in one language: French or English, not mixed
- Use accents in French
- Keep list items readable: concise but complete
- No H1 headers (`#`); start with H2 (`##`) or content; filename serves as the title
- Blank line before bullet lists
- Use markup (bold, italic, etc) only when needed for emphasis or clarity
- Avoid special characters: emojis, arrows, em-dashes
- No space before double punctuation (`;`, `?`, `!`), including in French, to prevent unintended line breaks
- No comma before `and` or `or`
- Join clauses with semicolons, colons or parentheses instead of dashes
- No placeholder sections for future content

## Filenames

- Use natural, readable names in the note language
- Name actions with an infinitive verb followed by a concrete object or expected result
- Do not put dates, statuses or tags in filenames; use frontmatter instead

Examples: `Reply to the insurance company.md`, `Book the vehicle inspection.md`

## Frontmatter

Every note starts with YAML frontmatter:

- `status`: new, active, shelved, next, waiting, done
- `created`: YYYY-MM-DD
- `modified`: YYYY-MM-DD
- `tags`: `action` or `reference`
- `topics`: array of free-form tags for searchability

Frontmatter keeps notes findable and trackable across the vault.

### Status

- `new`: just captured, not reviewed
- `active`: in use, maintained
- `shelved`: abandoned, may revisit
- `next`: prioritized as next action
- `waiting`: blocked on external input
- `done`: completed, archived

## Actions

Actions use the TaskNotes plugin, which adds:

- `priority`: low, normal, high, top
- `scheduled`: YYYY-MM-DD; date when the action should be performed, not the capture date
- `projects`: array of wikilinks to related projects

Pick a realistic date when the action is created based on urgency, effort, deadlines and dependencies. Use today for a short or urgent action, the next working day for a normal action, and a later date when there is a known deadline, dependency or follow-up delay.

## References

- Use wikilinks syntax: `[[FILENAME]]`
- Use short paths without folder prefix (e.g., `[[DESIGN]]` not `[[.kyanite/DESIGN]]`)

## Commit Messages

- Use a concise English Conventional Commit based on the actual diff; name the concrete change
- Example: `feat: add capture workflow and scheduling conventions`
