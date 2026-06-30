# Delivery Workflow

## Status

**Status:** Draft  
**Last Updated:** 2026-06-30

---

# Introduction

Software delivery is more than writing code.

Successful delivery combines product thinking, architecture, implementation, review, testing, documentation and continuous learning.

The AI Product Delivery Framework defines a structured delivery workflow that integrates human leadership with specialized AI roles.

The objective is simple:

Deliver validated product progress safely, consistently and repeatedly.

---

# Delivery Philosophy

The framework is built around one principle:

> Software delivery is a continuous learning process.

Every iteration should increase one or more of the following:

- product value;
- user understanding;
- repository quality;
- engineering quality;
- business confidence.

The goal is not producing more code.

The goal is producing more validated value.

---

# Delivery Lifecycle

Every project follows a repeating lifecycle.

```text
Idea
    │
    ▼
Product Discovery
    │
    ▼
Product Documentation
    │
    ▼
Architecture
    │
    ▼
Epic Planning
    │
    ▼
Task Planning
    │
    ▼
Implementation
    │
    ▼
Review
    │
    ▼
Testing
    │
    ▼
Release
    │
    ▼
Feedback
    │
    ▼
Discovery
```

The cycle never truly ends.

Every release generates new knowledge.

That knowledge becomes the starting point for the next iteration.

---

# Delivery Principles

## Small Safe Iterations

The framework strongly prefers small tasks.

Instead of:

- implementing an entire feature;
- rewriting a subsystem;
- creating massive pull requests;

the work should be decomposed into independent, reviewable steps.

Example:

```text
Epic 005

↓

005A

↓

005B

↓

005C

↓

005D

↓

005E
```

Every completed task should leave the repository in a stable state.

---

## Repository First

The repository is the project's long-term memory.

Important knowledge should never exist only inside AI conversations.

Repository content includes:

- product documentation;
- architecture;
- task descriptions;
- implementation;
- review reports;
- migration notes;
- decision records.

Chat history is temporary.

The repository is permanent.

---

## Context Before Code

Implementation should never begin without sufficient context.

Implementation AI should receive:

- product documentation;
- architecture;
- task description;
- repository rules;
- acceptance criteria;
- project constraints.

Good context dramatically improves implementation quality.

---

## Documentation Drives Delivery

Documentation is not created after implementation.

Documentation guides implementation.

Product documentation influences architecture.

Architecture influences tasks.

Tasks influence implementation.

Implementation updates documentation.

The workflow is bidirectional.

---

# Delivery Stages

The framework divides delivery into distinct stages.

---

## Stage 1 — Product Discovery

Purpose:

Understand what should be built.

Outputs:

- Product Vision
- Product Principles
- UX Principles
- MVP Definition
- Product Roadmap

---

## Stage 2 — Product Documentation

Purpose:

Transform ideas into structured documentation.

Outputs:

- product specifications;
- information architecture;
- user flows;
- screen specifications;
- release criteria.

---

## Stage 3 — Architecture

Purpose:

Define how the product will be implemented.

Outputs:

- architecture overview;
- application structure;
- domain model;
- data model;
- technology choices;
- integration strategy.

Architecture should support delivery rather than overcomplicate it.

---

## Stage 4 — Epic Planning

Purpose:

Break product goals into meaningful implementation milestones.

Each Epic should represent a coherent business capability.

Examples:

- Authentication
- Home Screen
- Offline Support
- Search
- Routing

Epics should remain understandable by both humans and AI agents.

---

## Stage 5 — Task Planning

Each Epic is decomposed into small implementation tasks.

Every task should have:

- objective;
- scope;
- dependencies;
- acceptance criteria;
- implementation notes;
- testing requirements.

Tasks should normally require hours or days, not weeks.

---

## Stage 6 — Implementation

Implementation focuses only on the current task.

Implementation AI should avoid expanding scope.

The implementation phase should not redesign the product.

That work belongs to Product Discovery or Architecture.

---

## Stage 7 — Review

Every implementation should be reviewed.

Review includes:

- correctness;
- consistency;
- documentation alignment;
- architecture compliance;
- coding standards;
- unnecessary complexity;
- hidden risks.

Review is independent from implementation.

---

## Stage 8 — Testing

Testing validates:

- functionality;
- regressions;
- acceptance criteria;
- edge cases;
- user experience where applicable.

Testing protects delivery confidence.

---

## Stage 9 — Release

A release is more than publishing code.

A release should include:

- updated documentation;
- completed tasks;
- changelog;
- version update;
- validated implementation.

---

## Stage 10 — Feedback

Every release creates feedback.

Feedback may come from:

- users;
- analytics;
- crash reports;
- business metrics;
- support;
- AI review.

Feedback becomes input for the next Discovery cycle.

---

# Delivery Roles

The framework separates responsibilities between multiple participants.

Human:

- owns decisions;
- owns priorities;
- approves releases.

Strategic AI:

- assists planning;
- reviews product consistency;
- proposes improvements.

Implementation AI:

- writes implementation;
- updates code;
- performs migrations.

Review AI:

- audits implementation;
- identifies risks;
- verifies consistency.

Research AI:

- gathers external knowledge;
- compares alternatives;
- supports decision making.

Separating responsibilities improves quality.

---

# Task Lifecycle

Every task follows a predictable lifecycle.

```text
Task Created
        │
        ▼
Context Prepared
        │
        ▼
Implementation
        │
        ▼
Review
        │
        ▼
Revision
        │
        ▼
Testing
        │
        ▼
Human Approval
        │
        ▼
Commit
        │
        ▼
Checkpoint
        │
        ▼
Next Task
```

Tasks should move through the workflow one step at a time.

Skipping stages increases delivery risk.

---

# AI Context Lifecycle

AI-assisted delivery depends on context quality.

Context should move through the project in a controlled cycle.

```text
Discovery
    │
    ▼
Repository Documentation
    │
    ▼
Task Context
    │
    ▼
AI Session
    │
    ▼
Review
    │
    ▼
Repository Update
    │
    ▼
Next Task
```

The repository is the long-term memory.

AI sessions are temporary execution environments.

Important knowledge must always return to the repository.

---

# Context Package

Before assigning work to an AI agent, prepare a context package.

A good context package includes:

- project purpose;
- current task;
- relevant product documentation;
- relevant architecture documentation;
- repository rules;
- known constraints;
- expected output;
- validation requirements.

The context package should be as small as possible, but complete enough to avoid guessing.

---

# Definition Of Ready

A task is ready for implementation when:

- the goal is clear;
- the scope is clear;
- required documentation exists;
- dependencies are known;
- acceptance criteria exist;
- implementation boundaries are defined;
- validation method is known;
- expected output is clear.

If these conditions are not met, the task should return to planning.

---

# Definition Of Done

A task is done only when:

- implementation is complete;
- acceptance criteria are satisfied;
- tests or validation were performed;
- documentation was updated if needed;
- no known blocker remains unreported;
- review was completed or explicitly deferred;
- changes were committed;
- important findings were saved into the repository.

Done means stable enough to continue safely.

It does not mean perfect.

---

# Review Reports

Large reviews should be saved as files.

They should not exist only in terminal output or chat history.

Recommended location:

```text
docs/reviews/
```

Review file names should include date and time:

```text
YYYY-MM-DD_HH-MM_REVIEW_NAME.md
```

A review report should include:

- title;
- date and time;
- author or AI role;
- repository revision;
- reviewed scope;
- findings;
- risks;
- recommendations;
- unresolved questions.

This makes reviews reusable and auditable.

---

# Implementation Reports

Implementation reports should summarize completed work.

Recommended location:

```text
docs/reports/
```

Implementation reports are useful when:

- the task is large;
- multiple files changed;
- important trade-offs were made;
- follow-up work exists;
- another AI agent will continue the work.

A report should be concise but complete enough for handover.

---

# Checkpoints

A checkpoint captures the project state after an important milestone.

Checkpoints help future humans and AI agents understand project history.

A checkpoint may include:

- completed work;
- current architecture;
- known issues;
- next priorities;
- important decisions;
- repository revision.

Checkpoints are especially useful after:

- epic completion;
- architecture migration;
- major product pivot;
- release;
- legacy migration.

---

# Git Workflow

Git is part of the delivery workflow.

Every meaningful change should be committed.

Commits should be small and understandable.

A practical workflow:

```text
git status
    ↓
make changes
    ↓
validate
    ↓
git add
    ↓
git commit
    ↓
git push
```

Implementation AI should not hide Git state.

Before completing work, it should report:

- changed files;
- validation performed;
- commit hash if committed;
- push status if pushed.

---

# Branch Strategy

Small documentation changes may happen directly on main.

Larger implementation work should usually happen on a feature branch.

Feature branches are especially useful when:

- the app may be temporarily broken;
- multiple tasks are related;
- tests will be migrated gradually;
- legacy architecture is being replaced;
- release stability matters.

The framework does not enforce one universal branch strategy.

The human owner decides based on project risk.

---

# Handling Broken Intermediate States

Some migrations require temporary incomplete states.

Examples:

- replacing navigation architecture;
- moving from old UI to new UI;
- rewriting data layer;
- changing localization structure;
- migrating tests.

If a broken intermediate state is expected, it must be documented before implementation begins.

The task or epic should explain:

- what will be temporarily broken;
- why it is acceptable;
- how long it should last;
- how recovery will happen;
- which tests are expected to fail temporarily.

Silent breakage is not acceptable.

Documented transitional breakage may be acceptable.

---

# Managing Technical Debt

Technical debt is allowed when intentional.

It should be visible.

For each significant debt item, document:

- what debt was accepted;
- why it was accepted;
- what risk it creates;
- when it should be revisited.

Technical debt should support delivery.

It should not become an excuse for chaos.

---

# Delivery Metrics

The framework values progress that improves the product.

Useful metrics include:

- validated assumptions;
- released MVP increments;
- completed tasks;
- resolved risks;
- documented decisions;
- reduced uncertainty;
- user feedback received;
- revenue or business signals.

Less useful metrics:

- lines of code;
- number of generated files;
- number of prompts;
- amount of AI output.

The goal is validated product progress.

---

# Delivery Anti-Patterns

## Coding Without Discovery

Starting implementation before understanding the product creates waste.

---

## Tasks Without Documentation

Implementation tasks should be derived from product and architecture documentation.

Random tasks create random products.

---

## Giant Tasks

Large tasks are hard to review, test and recover from.

Split work into smaller steps.

---

## AI Scope Expansion

Implementation AI may try to improve unrelated parts of the project.

This should be avoided unless explicitly approved.

---

## Review Only At The End

Late review finds problems after they become expensive.

Review should happen throughout delivery.

---

## Knowledge Trapped In Chat

If important knowledge remains only in chat history, the project will lose it.

Move important conclusions into the repository.

---

## Perfect Architecture Before MVP

Architecture should enable delivery.

It should not become an excuse to avoid release.

---

## No Human Decision

AI can produce options endlessly.

Delivery requires human decisions.

---

# Delivery For Greenfield Projects

For a new project, delivery starts with discovery.

Recommended order:

1. Create repository structure.
2. Define product vision.
3. Define core principles.
4. Define MVP scope.
5. Define architecture direction.
6. Create epic backlog.
7. Create first implementation tasks.
8. Start implementation.
9. Review and iterate.

Greenfield projects should avoid starting with code.

---

# Delivery For Legacy Projects

For an existing repository, delivery starts with audit.

Recommended order:

1. Freeze current state.
2. Commit all existing work.
3. Run repository audit.
4. Run documentation audit.
5. Identify legacy and active areas.
6. Define target product direction.
7. Create migration strategy.
8. Archive obsolete knowledge.
9. Rewrite active documentation.
10. Resume implementation.

Legacy delivery should preserve useful existing value.

---

# Delivery For AI-Assisted Legacy Projects

For existing projects with previous AI involvement, delivery starts with knowledge reconstruction.

Recommended order:

1. Collect existing documentation.
2. Summarize important AI chat history.
3. Identify conflicting AI-generated artifacts.
4. Define the current source of truth.
5. Archive outdated assumptions.
6. Create updated agent rules.
7. Rebuild task structure.
8. Continue with controlled AI workflow.

The goal is to convert chaotic AI history into repository knowledge.

---

# Practical Delivery Rule

Before starting any implementation task, answer:

1. What product value does this task create?
2. What document defines the requirement?
3. What architecture applies?
4. What files may change?
5. How will success be validated?
6. Who reviews the result?
7. Where will new knowledge be stored?

If these answers are unclear, the task is not ready.

---

# Final Notes

The framework does not try to maximize AI activity.

It tries to maximize useful product progress.

The most important delivery rule is:

> Validated Product Progress > Lines Of Code.

AI can generate code quickly.

The human and the framework must ensure that the generated work moves the product in the right direction.

---

# Related Documents

- `docs/001_FRAMEWORK_VISION.md`
- `docs/002_CORE_PRINCIPLES.md`
- `docs/003_AI_AGENT_ROLES.md`
- `docs/004_HUMAN_ROLE.md`
- `docs/005_PRODUCT_DISCOVERY.md`
- `docs/007_MVP_FIRST.md`
- `docs/008_LEGACY_MIGRATION.md`
- `docs/009_AI_ASSISTED_MIGRATION.md`
- `templates/tasks/EPIC_README.md`
- `templates/tasks/TASK_TEMPLATE.md`
- `templates/prompts/007_IMPLEMENTATION_AGENT_PROMPT.md`
- `templates/prompts/008_REVIEW_AGENT_PROMPT.md`
