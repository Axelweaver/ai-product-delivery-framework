

# TASK_EXECUTION_PROTOCOL.md

## Purpose

This document defines the standard task execution protocol for AI agents and humans working in a repository that adopts the AI Product Delivery Framework.

The protocol exists to keep implementation work controlled, reviewable and aligned with product documentation.

It should be copied into project repositories and adapted only when necessary.

---

# Core Rule

Do not start implementation until the task, context, scope and validation method are clear.

If they are not clear, stop and ask for clarification or perform a review-only analysis first.

---

# Task Execution Lifecycle

Every task should follow this lifecycle:

```text
Task Selected
      │
      ▼
Repository State Checked
      │
      ▼
Context Loaded
      │
      ▼
Scope Confirmed
      │
      ▼
Implementation Plan Created
      │
      ▼
Changes Applied
      │
      ▼
Validation Performed
      │
      ▼
Documentation Updated
      │
      ▼
Final Review
      │
      ▼
Human Approval
      │
      ▼
Commit / Push If Requested
```

Skipping steps increases the risk of incorrect implementation.

---

# Step 1 — Check Repository State

Before starting any task, inspect the repository state.

Run:

```text
git status
```

Record:

- current branch;
- changed files;
- untracked files;
- whether the working tree is clean;
- whether there are existing user changes.

Do not overwrite user changes.

If the repository has uncommitted changes that are not part of your task, report them before proceeding.

---

# Step 2 — Read Required Context

Read available context before making decisions.

Recommended order:

1. `README.md`
2. `PROJECT_CONTEXT.md`
3. `docs/README.md`
4. `docs/product/`
5. `docs/architecture/`
6. `docs/tasks/`
7. `docs/reviews/`
8. `CLAUDE.md`
9. Current task file

If any expected context is missing, mention it in the task summary.

Missing context is not always a blocker, but it must be visible.

---

# Step 3 — Identify The Current Task

Before implementation, identify:

- task name;
- task location;
- task objective;
- task scope;
- dependencies;
- acceptance criteria;
- expected validation.

If the task is not documented, create a short task summary before implementation or ask the human owner for clarification.

---

# Step 4 — Confirm Scope

The agent must work only inside the assigned scope.

Allowed:

- implement required behavior;
- update directly related files;
- update documentation when required;
- add or update tests when required;
- report unrelated findings.

Not allowed without explicit approval:

- broad refactoring;
- changing unrelated architecture;
- rewriting unrelated documentation;
- modifying unrelated tasks;
- deleting historical context;
- changing product direction.

---

# Step 5 — Create A Short Implementation Plan

Before editing files, create a short plan.

The plan should include:

- files likely to change;
- implementation approach;
- expected validation commands;
- potential risks.

The plan should be concise.

Do not over-plan small tasks.

---

# Step 6 — Apply Changes Incrementally

Apply changes in small steps.

Prefer focused edits over large rewrites.

After each meaningful change, keep the repository understandable.

Avoid mixing unrelated changes in one task.

---

# Step 7 — Update Documentation If Needed

Documentation must remain consistent with implementation.

Update documentation when the task changes:

- product behavior;
- architecture;
- task status;
- setup instructions;
- public API;
- release behavior;
- known limitations.

Do not update documentation only for cosmetic reasons unless requested.

---

# Step 8 — Validate The Result

Run project-appropriate validation.

Examples:

```text
flutter analyze
flutter test
npm test
dotnet test
cargo test
```

Use repository-documented commands when available.

If validation cannot be run, explain why.

Do not claim success without validation.

---

# Step 9 — Review The Changes

Before finishing, review your own changes.

Check:

- task requirements satisfied;
- no unrelated changes introduced;
- documentation remains consistent;
- tests or validation performed;
- no obvious broken links;
- no temporary debug artifacts left behind.

---

# Step 10 — Final Response

The final response should include:

- what was done;
- files changed;
- validation performed;
- known risks or TODOs;
- Git status summary;
- recommended next step.

Do not hide failures.

Do not claim that the repository is clean unless verified.

---

# Review-Only Task Protocol

If the task is review-only:

- do not change existing files;
- inspect repository state;
- read relevant context;
- produce findings;
- classify findings by severity;
- recommend next actions.

If the human explicitly requests a report file, creating that report is allowed.

Review reports should be saved in:

```text
docs/reviews/
```

Use filename format:

```text
YYYY-MM-DD_HH-MM_REVIEW_NAME.md
```

---

# Documentation Task Protocol

For documentation-only tasks:

- keep content aligned with existing framework vocabulary;
- avoid unnecessary duplication;
- preserve links;
- update related indexes if needed;
- maintain consistent status and date metadata;
- avoid mixing documentation languages unless required.

Documentation is part of the product.

Treat it as a first-class artifact.

---

# Implementation Task Protocol

For implementation tasks:

- read product and architecture documents first;
- inspect existing code before writing new code;
- follow established conventions;
- prefer minimal working implementation;
- add tests where appropriate;
- update documentation when behavior changes.

Implementation should satisfy the task, not redesign the product.

---

# Legacy Migration Task Protocol

For legacy migration tasks:

- audit before changing;
- classify legacy artifacts;
- preserve useful history;
- archive before deleting;
- document migration risks;
- avoid big-bang rewrites;
- keep migration steps reversible when possible.

If old and new documentation conflict, report the conflict instead of guessing.

---

# AI-Assisted Migration Task Protocol

For repositories with previous AI involvement:

- assume important knowledge may exist outside current files;
- prioritize repository source of truth;
- inspect old prompts and review reports if available;
- identify conflicting AI-generated artifacts;
- stabilize knowledge inside documentation;
- recommend prompt or agent-rule updates when needed.

Do not treat previous AI output as automatically correct.

---

# Commit Protocol

Do not commit unless the human explicitly asks.

When asked to commit:

1. Run `git status`.
2. Confirm changed files are expected.
3. Stage only relevant files.
4. Use a concise commit message.
5. Run `git status` after commit.
6. Push only if explicitly requested.

Example:

```text
git status
git add <files>
git commit -m "Add task execution protocol"
git status
git push
```

---

# Task Status Updates

When a task is completed, update task status if the project uses status fields.

Common statuses:

- Draft
- Ready
- In Progress
- Blocked
- Done
- Deprecated

Do not mark a task Done if validation failed or known blockers remain unresolved.

---

# Handling Blockers

If blocked, stop and report:

- what is blocked;
- why it is blocked;
- what was attempted;
- what decision is needed;
- recommended next action.

Do not continue by inventing requirements.

---

# Handling Uncertainty

Uncertainty should be visible.

Use phrases such as:

- "This is unclear because..."
- "The repository does not define..."
- "This requires human decision..."
- "I recommend creating a follow-up task..."

Do not hide uncertainty behind confident language.

---

# Definition Of Done

A task is done when:

- requested scope is completed;
- acceptance criteria are satisfied;
- validation was performed or explicitly impossible;
- documentation is updated if needed;
- no unrelated changes remain;
- final summary is provided;
- next step is clear.

Done does not mean perfect.

Done means safe to continue.

---

# Absolute Prohibitions

Do not:

- overwrite user changes;
- invent product requirements;
- silently expand scope;
- delete historical documentation without approval;
- commit without instruction;
- push without instruction;
- claim tests passed without running them;
- ignore broken validation;
- mix unrelated changes;
- treat chat history as more authoritative than repository files.

---

# Guiding Principle

Small safe tasks. Clear context. Visible decisions. Repository memory.