# Task proposal and closure contract

Use one concise contract for each cohesive deliverable. A task may combine several small code edits. Do not fill the user's screen with repeated forms or ceremonies for trivial steps inside an already approved task.

## Before proposing or beginning a new task

A task proposal must state:

- **Task / objective:** one clear deliverable and why now.
- **Gain:** concrete value (less rework, lower branch count, faster delivery, fixed defect, proven behavior); distinguish expected from measured.
- **Mechanism:** actions, tools/channels and relevant existing skills. State if new branch, CI or migration is actually required.
- **Expected result / acceptance:** observable artifact, evidence or metric. Prefer crisp binary conditions over vague "improved".
- **Owner:** choose Usuario / Codex GUI / Codex VS / Chat + plugins or real external owner.
- **Prerequisites / authority:** only if material. No unneeded user interruption when task is already authorized.

### Compact example

**Task:** Correct a failing employee API serializer in the existing feature branch.
**Gain:** Avoid missing dates and eliminate downstream manual corrections.
**Mechanism:** Inspect schema mapping, patch serializer, execute targeted API contract tests, review PR.
**Expected result:** Two date fields present, endpoint success and no regression in pagination; integrate to `main` after CI and authorization.
**Owner:** Codex VS. **Gate:** CI pass and authorized merge.

## On completion of EVERY task

Always state, regardless of whether the user needs to do something:

1. **What was delivered:** exact change and artifact/PR/commit if verified; no fabricated links.
2. **What was verified:** observed checks/results; distinguish NOT RUN, BLOCKED, PASS and FAIL.
3. **What is next:** single most relevant action or the next compact dependency group.
4. **Who acts:** one of Usuario, Codex GUI, Codex VS, Chat + plugins, or explicitly named external owner.
5. **What starts the next stage:** gate/evidence, if relevant. Say "No user action" when appropriate.
6. **Current activity:** only tasks actually executing at this moment; otherwise "Execution concluded for this response; next action pending". Do not pretend to continue working off-screen.

### When the owner is the user

Provide a directly executable step-by-step with:

1. Where to open or run (project, repo, terminal, UI).
2. Precise action/command, using placeholders for secrets; never request tokens in chat.
3. Expected output / what indicates success.
4. Failure handling or exactly what sanitized evidence to return.

### Compact closure example

**Delivered:** Added serializer correction and targeted contract test in PR #X (link only when verified).
**Validation:** Targeted tests PASS (actual count); integration CI PENDING.
**Next:** Review CI and merge to `main` only after checks and approval.
**Owner:** Chat + plugins for CI review; authorized maintainer for merge.
**Gate:** CI success and explicit merge authorization.
**User action:** None at this stage.
**Current activity:** No background execution; awaiting CI event or user follow-up.

If blocked, state the blocker directly instead of inventing a status. If there is no next task, state completion and no pending action.
