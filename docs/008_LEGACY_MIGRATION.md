

# Legacy Migration

## Status

**Status:** Draft  
**Last Updated:** 2026-06-30

---

# Introduction

Most real software projects are not greenfield projects.

They already have:

- existing code;
- old documentation;
- outdated decisions;
- partial implementations;
- missing context;
- historical compromises;
- technical debt;
- business constraints.

The AI Product Delivery Framework treats legacy migration as a normal and important delivery scenario.

Legacy is not failure.

Legacy is accumulated product history.

The goal is not to erase it blindly.

The goal is to understand it, preserve useful knowledge, archive obsolete knowledge and move the project toward a clearer product and engineering direction.

---

# What Is Legacy?

Legacy is any part of a project that no longer fully matches the current product, architecture or delivery direction.

Legacy may include:

- code;
- documentation;
- tasks;
- architecture decisions;
- design files;
- tests;
- deployment scripts;
- AI-generated artifacts;
- old prompts;
- assumptions;
- workflows.

Legacy does not always mean bad.

Something becomes legacy when it needs classification before it can be safely used.

---

# Legacy Is Not Automatically Wrong

Old work may contain valuable knowledge.

It may explain:

- why a feature exists;
- why a decision was made;
- why a workaround exists;
- what constraints existed at the time;
- what previous product direction looked like.

Deleting legacy without review destroys context.

The framework prefers:

> Archive before delete.

---

# Legacy Migration Goals

Legacy migration should achieve several goals:

- identify current source of truth;
- preserve useful knowledge;
- archive obsolete artifacts;
- remove ambiguity;
- align documentation with current product direction;
- align architecture with current delivery needs;
- create safe implementation tasks;
- reduce future AI confusion.

Migration is not only technical.

It is product, documentation and architecture work.

---

# Migration Philosophy

The framework follows several rules.

## Understand Before Changing

Do not rewrite before understanding the current state.

## Preserve Useful History

Old decisions may still matter.

## Archive Instead Of Delete

Historical context should remain accessible.

## Create A New Source Of Truth

Migration is complete only when future work has clear current documentation.

## Migrate In Small Steps

Large migrations are risky.

Small migrations are reviewable.

---

# Legacy Migration Lifecycle

A typical migration follows this sequence:

```text
Existing Repository
        │
        ▼
Freeze Current State
        │
        ▼
Repository Audit
        │
        ▼
Documentation Audit
        │
        ▼
Architecture Audit
        │
        ▼
Product Direction Review
        │
        ▼
Legacy Classification
        │
        ▼
Migration Strategy
        │
        ▼
Archive Legacy Artifacts
        │
        ▼
Create New Source Of Truth
        │
        ▼
Rewrite Tasks
        │
        ▼
Resume Delivery
```

Skipping audit usually creates confusion later.

---

# Step 1 — Freeze Current State

Before migration begins, the repository should be safe.

Required actions:

- commit all current work;
- push the current state;
- confirm working tree status;
- record current branch;
- optionally create a backup branch.

Recommended command sequence:

```text
git status
git add .
git commit -m "Checkpoint before legacy migration"
git push
```

If the working tree is not clean, migration risk increases.

---

# Step 2 — Repository Audit

Repository audit identifies what exists.

Audit should inspect:

- root README;
- documentation structure;
- source code structure;
- tests;
- scripts;
- configuration;
- assets;
- build system;
- CI/CD;
- issue trackers if available.

The output should be a repository audit report.

Recommended location:

```text
docs/reviews/
```

---

# Step 3 — Documentation Audit

Documentation audit identifies which documents are current, outdated, conflicting or missing.

Classify every important document as one of:

- Active;
- Partially Active;
- Legacy;
- Deprecated;
- Duplicate;
- Missing Replacement;
- Unknown.

The audit should answer:

- Which documents are source of truth?
- Which documents contradict current direction?
- Which documents contain unique useful knowledge?
- Which documents should be archived?
- Which documents should be rewritten?

---

# Step 4 — Architecture Audit

Architecture audit identifies how the system is currently built.

Review:

- module structure;
- data flow;
- navigation;
- state management;
- persistence;
- external integrations;
- test structure;
- build and release process.

The output should explain:

- current architecture;
- target architecture if known;
- gaps;
- migration risks;
- recommended migration order.

---

# Step 5 — Product Direction Review

Legacy projects often contain old product assumptions.

Before rewriting code, clarify current product direction.

Questions:

- What is the product now?
- What should it become?
- Which old product assumptions are no longer valid?
- Which old features still matter?
- Which users are still target users?
- What is the current MVP or next release goal?

Product direction should be documented before implementation migration begins.

---

# Step 6 — Legacy Classification

After audits, classify artifacts.

## Active

Current source of truth.

Used for future work.

## Partially Active

Still useful, but needs updates.

## Legacy

Historical material preserved for reference.

Not used as implementation guidance.

## Deprecated

Explicitly replaced by newer documentation or implementation.

## Duplicate

Content repeated elsewhere.

Should be merged or removed after review.

## Missing Replacement

Old content contains useful information that has no new equivalent yet.

Do not archive until replacement exists.

---

# Step 7 — Migration Strategy

Migration strategy should define:

- what changes first;
- what must not change yet;
- what is archived;
- what is rewritten;
- what is preserved;
- what tasks are created;
- what risks exist;
- what temporary broken states are acceptable.

A good migration strategy prevents random cleanup.

---

# Step 8 — Archive Legacy Artifacts

Archived artifacts should be moved to a clear archive location.

Recommended structure:

```text
docs/archive/
└── legacy/
```

Archived documents should include a short notice explaining:

- why they were archived;
- when they were archived;
- what replaced them;
- whether they contain useful historical context.

Archived files should not be used as implementation instructions unless explicitly referenced by an active task.

---

# Step 9 — Create New Source Of Truth

Migration is not complete when old files are archived.

Migration is complete only when current documentation exists.

New source of truth usually includes:

```text
docs/product/
docs/architecture/
docs/design/
docs/tasks/
```

The new documentation should answer:

- What is the current product?
- What is the current architecture?
- What is the current delivery plan?
- What should implementation agents follow?

---

# Step 10 — Rewrite Tasks

Old tasks often describe old architecture.

After product and architecture migration, task files should be reviewed.

Each task should be classified as:

- still valid;
- partially valid;
- obsolete;
- should be rewritten;
- should be replaced by a new epic.

Implementation should resume only when active tasks match the current source of truth.

---

# Legacy Documentation Rules

When archiving documentation:

- do not silently delete;
- do not leave old docs in active paths without warning;
- preserve unique useful information;
- create replacement documents before removing active references;
- update README files;
- update task references.

Old documentation without clear status creates confusion for AI agents.

---

# Legacy Code Rules

Legacy code should be treated carefully.

Do not rewrite working code only because it is old.

Rewrite when:

- it blocks product direction;
- it creates unacceptable risk;
- it prevents delivery;
- it contradicts target architecture;
- it is cheaper to replace than maintain.

Preserve when:

- it works;
- it is isolated;
- it supports current product needs;
- rewriting creates unnecessary risk.

---

# Migration And Tests

Tests are part of migration.

Classify tests as:

- still valid;
- tied to old behavior;
- obsolete;
- missing for new behavior.

If tests are expected to fail temporarily, document this before implementation.

Silent test failure is not acceptable.

A planned test migration is acceptable.

---

# Migration And AI Agents

AI agents are especially vulnerable to legacy confusion.

If old and new documents coexist without clear status, AI may combine incompatible instructions.

To reduce this risk:

- mark legacy documents clearly;
- update README files;
- define source of truth;
- remove broken references;
- provide task-specific context;
- save review reports into the repository.

Clear context improves AI reliability.

---

# Legacy Migration Anti-Patterns

## Cleanup Without Audit

Changing files before understanding the project creates risk.

---

## Deleting Historical Context

Old documentation may explain why the system exists.

Archive first.

---

## Rewriting Everything

Full rewrites often destroy useful working value.

Prefer targeted migration.

---

## Keeping Contradictory Docs Active

Conflicting active documentation causes bad implementation decisions.

---

## Letting AI Guess Source Of Truth

AI should not decide which conflicting document is correct unless asked to review and report.

---

## Ignoring Tests

Old tests may fail because behavior changed.

This must be planned, not discovered accidentally.

---

# Real Example — Belgrade Metro

Belgrade Metro revealed a common legacy migration problem.

A new product direction was created:

- Map First UX;
- no bottom navigation;
- bottom-sheet-driven interaction;
- geographic map of Belgrade;
- burger menu for secondary navigation.

However, older documents and existing code still described:

- bottom navigation;
- standalone search screen;
- schematic map;
- old route planning flow.

This created conflicting sources of truth.

The correct migration approach was:

1. audit all documentation;
2. identify conflicts;
3. define product documentation as current source of truth;
4. archive or mark old documents;
5. rewrite architecture documentation;
6. update task structure;
7. only then continue implementation.

This example demonstrates why legacy migration must include product and documentation work, not only code changes.

---

# Practical Migration Checklist

Before starting legacy migration:

- [ ] Working tree is clean.
- [ ] Current state is committed and pushed.
- [ ] Repository audit is complete.
- [ ] Documentation audit is complete.
- [ ] Architecture audit is complete.
- [ ] Current product direction is clear.
- [ ] Source of truth is defined.
- [ ] Legacy archive plan exists.
- [ ] Replacement documentation is planned.
- [ ] Task migration strategy exists.
- [ ] Test migration strategy exists.

If several items are missing, implementation should wait.

---

# Final Notes

Legacy migration is not about blaming the past.

Every legacy system reflects decisions made under previous constraints.

The goal is to make the next decision easier, safer and better documented.

The best migration preserves useful history while creating a clearer future.

---

# Related Documents

- `docs/002_CORE_PRINCIPLES.md`
- `docs/005_PRODUCT_DISCOVERY.md`
- `docs/006_DELIVERY_WORKFLOW.md`
- `docs/009_AI_ASSISTED_MIGRATION.md`
- `templates/prompts/002_LEGACY_REPOSITORY_AUDIT_PROMPT.md`
- `templates/prompts/005_ARCHITECTURE_REVIEW_PROMPT.md`