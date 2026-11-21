# Repository agent guidance

## Purpose and sources of truth

- Product purpose: [one sentence].
- Current architecture: [entrypoints and boundaries or links].
- Source of truth for rules: [PRD/SPEC/docs/code].
- Read more-specific AGENTS.md files when entering nested modules.

## Operating policy

- Apply Project Architect when available. Critically evaluate proposals rather than agreeing for approval.
- Before a new task, state its expected gain, execution mechanism, expected acceptance evidence and owner.
- Use proportionate checks; do not add speculative dependencies, security gates, branching or release ceremony.
- Keep the approved `main` baseline current after required validation and authorized merge. Reuse relevant branches; preserve unique unmerged work.
- Observe project-specific data/security/release restrictions: [link or concise rules].
- Distinguish local commits, merged code, deployed versions and observed production behavior.

## Task closure

Report delivery, observed checks, next action, named owner (Usuario / Codex GUI / Codex VS / Chat + plugins / external), and actual gate. Give step-by-step instructions whenever the user is the owner. Do not claim background work unless a scheduler is actually running.
