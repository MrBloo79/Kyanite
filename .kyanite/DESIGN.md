Architectural decisions, design patterns, and system design for Kyanite.

## Principles

Kyanite is designed around four core principles:

- Assistant-agnostic: Should work with any AI assistant; no vendor lock-in
- Transparent: Configuration should be tracked and visible
- Self-cleaning: Should resist accumulation; stay organized and focused
- Self-updating: Should integrate changes where they belong; alert on conflicts; refactor to resolve them

## Files & Purpose

Kyanite uses a layered configuration system. Files should be loaded in this order:

1. MEMORY.md: User context, blockers, needs, language preferences (shapes everything)
2. DESIGN.md: Architectural decisions, principles, compliance rules (compliance baseline)
3. AGENT.md: Behavior rules, tone, decision-making, error handling (execution)
4. CONVENTIONS.md: Standards for writing, files, commits, patterns (output format)

## Ameliorations

- Create root `.instructions.md` to enable cross-assistant compatibility with assistant-specific overrides
- Consider automated workflow skills folder (Triage, Trim, Split)

