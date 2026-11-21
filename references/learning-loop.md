# Evidence-led methodology learning

## Objective

Find engineering practices that improve delivery speed, reduce redundant work, lower branch/PR sprawl or remove unnecessary friction while preserving critical quality. The skill is a versioned instruction package, **not a self-mutating autonomous memory**.

## Observe -> assess -> propose -> approve -> version

1. **Observe:** Detect a real correction or repeated problem in project execution (e.g., needless security gate, test duplication, unmerged PR accumulation, redundant branches, installer blocked by incidental hash changes).
2. **Assess:** Compare observed before/after evidence if present. Separate data from hypothesis. Favor demonstrated improvement; no invented ROI percentages.
3. **Classify scope:** personal methodology, shared organizational convention, project-only rule, or temporary exception. Keep company-private context from flowing into public/personal distribution.
4. **Propose:** Summarize problem, change, why it speeds delivery, trade-off, evidence, applicable scope and how success will be verified.
5. **Approve:** User approval is required to change canonical instruction files. Gather related proposals at task or milestone completion to avoid interrupting every coding step.
6. **Version:** Update the canonical Skill/repo via authorized mechanism. Track semantic version, date, short decision, source project/evidence pointer, and superseded rule. Distribute/reinstall updates to execution environments as necessary; GitHub alone does not automatically synchronize local skill installations.
7. **Re-evaluate:** If a rule makes work slower or harms quality, propose reversal with the same standard of evidence.

## Proposed lesson format

**Candidate rule:** [one sentence in imperative form]
**Observed problem:** [what actually happened]
**Evidence:** [verified PR, incident, CI result or user-approved correction; mark anecdote as such]
**Expected gain:** [observable shorter cycle, fewer branches, reduced duplicate checks; no invented percentages]
**Boundary / risk:** [what must not be weakened]
**Scope:** [personal / shared / project / temporary]
**Decision:** PROPOSED, APPROVED, REJECTED or SUPERSEDED
**Version:** [assign only after approval and actual update]

## Initial approved baseline to preserve

- Prioritize correctness and delivery over flattery.
- Do not allow process/security theater to block ordinary iterative development.
- Keep `main` current after review, checks and authorization; minimize branches and orphan PRs.
- Require clear benefit, mechanism, expected output and ownership for new tasks.
- Require actual delivery status and actionable next step on every task closure.
- Diagnose and minimally adapt existing projects before imposing a new project-wide methodology.

These are initial user-stated preferences, not proof that the skill is installed or that external repos already comply.
