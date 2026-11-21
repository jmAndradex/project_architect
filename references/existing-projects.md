# Adoption workflow for existing projects

The purpose is to improve development methodology without rewriting a functioning product, blindly copying templates or disrupting authorized operations.

## Step 1 - Read reality first

Collect only sources relevant to the user's goal:

- Repository identity, owner, current default branch and `main` presence, last meaningful change, branch/PR inventory; distinguish local and remote state.
- Applicable `AGENTS.md` hierarchy, project README, PRD/SPEC, architecture notes, existing task conventions and local authorization gates.
- Stack, key modules, system boundaries, CI/test and deployment workflows, current features, known issues and blockers.
- Artifacts/commit equivalence and evidence for claimed merge or deployment status. Do not assume a workflow file means a passing run.
- Existing rules that conflict with this skill. Preserve stronger or more specific legitimate policy; describe the conflict before proposing change.

If only partial source access exists, mark findings as unknown rather than inferring. Never ask the user to repeat information already supplied.

## Step 2 - Produce a short delta analysis

Use a compact matrix or paragraph grouping:

- **Already aligned:** no change.
- **Minimal adjustment:** specific file/rule, benefit, low-risk implementation.
- **Candidate cleanup:** branch/PR/doc clutter, with evidence and safety checks.
- **Project-specific exception:** explicit reason to preserve divergence.
- **Needs decision:** only a real authorization or domain choice.

Check the cost of modifying an existing `AGENTS.md`; prefer a small amendment over wholesale replacement. Avoid duplicate PRD/AGENTS/README or management plans unless real gaps exist.

## Step 3 - Propose and execute controlled adaptation

1. Rank by gain vs. risk vs. effort; deliver the smallest valuable change first.
2. Use the task proposal contract. Do not produce several new branches just for a methodology cleanup.
3. Change project guidance through an authorized PR/commit. Keep actual runtime/application code out of scope unless the user requested it.
4. Verify instructions do not contradict deployed systems, local policy or production controls; run only targeted checks for changes made.
5. Close with actual state and responsible owner. Keep pending changes visible, not hidden behind a generic "migrated" label.

## Template policy

`assets/AGENTS.template.md` and `assets/PRD.template.md` are for new projects or demonstrated missing guidance only. Never insert templates in bulk across existing repositories. A repo-specific `AGENTS.md` must have precedence on business rules, permission, technical stack and release gates.

## Personal and corporate isolation

The shared methodology should express portable engineering behavior. Do not copy internal source code, customer data, secrets, organization-only policies or proprietary architecture into personal projects or a publicly shared skill. Keep project-specific details inside authorized repositories, with separate distribution/permissions.
