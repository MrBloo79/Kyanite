Standards and conventions for this workspace.

## Writing & Style

- Keep each note in one language: French or English, not mixed
- Use accents in French
- No H1 headers (`#`): filename serves as the title
- Start with H2 (`##`) or content
- Blank line before bullet lists
- Use markup (bold, italic, etc) only when needed for emphasis or clarity
- Avoid special characters: emojis, arrows, em-dashes
- No space before double punctuation (`;`, `?`, `!`), including in French, to prevent unintended line breaks
- Join clauses with semicolons, colons, or parentheses instead of dashes
- No placeholder sections for future content

## Frontmatter

Every note starts with YAML frontmatter:

- `status`: new, active, shelved, next, waiting, done
- `created`: YYYY-MM-DD
- `modified`: YYYY-MM-DD
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
- `scheduled`: YYYY-MM-DD, optional
- `projects`: array of wikilinks to related projects

## References

- Use wikilinks syntax: `[[FILENAME]]`
- Use short paths without folder prefix (e.g., `[[DESIGN]]` not `[[.kyanite/DESIGN]]`)

## Commit Messages

- Follow Conventional Commits format
- Keep messages concise and descriptive
