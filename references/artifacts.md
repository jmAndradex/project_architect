# Minimal project artifacts

Do not create a documentation farm. Use existing material before adding files. The artifact must have a reader, decision or acceptance purpose.

## PRD - why and what

Use for new product/feature scope, complex redesign or unresolved product rules. Keep concise:

- Problem, user and business impact
- Goals, non-goals, assumptions and decisions
- Critical user flows, rules and constraints
- Interfaces/dependencies/data sources where needed
- Acceptance criteria with observable results
- Delivery slices and unresolved decisions

Avoid prescribing an implementation when a design decision remains open; do not duplicate the repo's exhaustive architecture docs.

## AGENTS.md - how this repository operates

Project-specific, short and authoritative for the repo. Include only:

- Current architecture and where to find truth
- Applicable instructions and skill triggers
- Repo workflow (branch, test, PR, merge and release gates)
- Project-specific access/data/operational restrictions
- Handoff and task reporting requirements (refer to Project Architect when installed)

Never replace existing AGENTS.md without inspecting its entire scope and more-specific nested instructions. Do not embed secrets or pretend availability of skills not installed.

## README - how to run and orient

Use for entrypoint/setup/commands only when absent or broken. Do not turn README into a second PRD.

## Technical SPEC and short plan

Create SPEC only when architecture/interfaces or nontrivial constraints require durable clarity. Use a short execution plan for multi-step work, but avoid permanent plans that will go stale. When a separate roadmap system is configured and requested, update it according to its own skill/policy, not by inventing parallel roadmap files.

## Handoff and status

At the end of tasks, provide a compact owner/action/gate/evidence report directly in the conversation or designated issue/PR. Avoid permanent docs for each routine task unless auditability requires them.
