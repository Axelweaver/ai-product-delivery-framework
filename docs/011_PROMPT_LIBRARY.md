# Prompt Library

## Status

**Status:** Draft  
**Last Updated:** 2026-06-30

---

# Introduction

Artificial Intelligence is one of the core components of the AI Product Delivery Framework.

However, AI systems do not produce reliable results simply because they are available.

High-quality results depend on clear context, well-defined objectives and structured communication.

This document defines how prompts should be designed, organized, versioned and maintained throughout the lifecycle of a project.

The objective is not to collect prompts.

The objective is to build a reusable Prompt Library that evolves together with the framework.

---

# Prompt Philosophy

A prompt is not a magic command.

A prompt is a structured interface between a human and an AI system.

Good prompts reduce ambiguity.

Good prompts improve consistency.

Good prompts reduce repeated explanations.

The best prompt is often the one that provides enough context for the AI to make good decisions without unnecessary complexity.

---

# Goals Of The Prompt Library

The Prompt Library exists to:

- standardize recurring AI workflows;
- reduce repetitive prompt writing;
- improve consistency across projects;
- simplify onboarding;
- capture lessons learned;
- preserve successful prompting patterns;
- improve collaboration between different AI systems.

Prompts are considered reusable engineering assets.

---

# Prompt Lifecycle

Every reusable prompt follows a lifecycle.

```text
Idea
   │
   ▼
Experimental Prompt
   │
   ▼
Used In Real Project
   │
   ▼
Reviewed
   │
   ▼
Improved
   │
   ▼
Added To Prompt Library
   │
   ▼
Versioned
   │
   ▼
Maintained
```

Only prompts validated through real projects should become part of the official library.

---

# Prompt Categories

The framework groups prompts by purpose rather than by AI provider.

Examples include:

- project initialization;
- repository audit;
- product discovery;
- architecture review;
- documentation review;
- implementation;
- testing;
- code review;
- release preparation;
- legacy migration;
- AI session handover;
- knowledge capture.

This classification remains stable even if AI systems change.

---

# Prompt Structure

Every reusable prompt should clearly define:

- objective;
- expected inputs;
- expected outputs;
- assumptions;
- limitations;
- required repository context;
- required documents;
- expected deliverables.

Reusable prompts should minimize hidden assumptions.

---

# Prompt Templates

Prompt templates should be generic.

Project-specific information should be injected separately.

Avoid embedding:

- project names;
- repository paths;
- personal information;
- temporary implementation details.

Reusable templates remain applicable across many projects.

---

# Context Before Instructions

Context is usually more important than instructions.

Before asking an AI system to perform a task, provide:

- product vision;
- repository structure;
- current task;
- relevant documentation;
- constraints;
- expected outcome.

Better context often produces better results than longer prompts.

---

# Repository As Context

Whenever possible, context should come from the repository rather than from the conversation.

Recommended sources include:

- README.md;
- product documentation;
- architecture documents;
- task documents;
- AI agent rules;
- review reports;
- changelog;
- checkpoints.

Repository-based context is easier to maintain than conversation-based context.

---

# Multi-Agent Compatibility

Prompt templates should avoid provider-specific assumptions.

A prompt should remain usable with:

- ChatGPT;
- Claude;
- Gemini;
- Codex;
- Cline;
- Cursor;
- local LLMs;
- future AI systems.

Only implementation-specific instructions should depend on the chosen AI platform.

---

# Prompt Versioning

Prompts evolve.

Changes should be versioned.

Version history should explain:

- why the prompt changed;
- what problem it solved;
- what was improved;
- whether compatibility changed.

Versioning allows successful prompt patterns to evolve without losing history.

---

# Prompt Quality

Not every prompt should become part of the Prompt Library.

A reusable prompt should satisfy several quality criteria.

Good prompts are:

- clear;
- reusable;
- deterministic where possible;
- context-aware;
- easy to maintain;
- independent from temporary project details.

The objective is not to make prompts longer.

The objective is to make them more reliable.

---

# Prompt Review

Reusable prompts should be reviewed after practical use.

Questions to ask:

- Did the AI understand the objective?
- Was important context missing?
- Were the expected deliverables produced?
- Were unnecessary assumptions made?
- Could the prompt be simplified?
- Can the prompt be reused in another project?

Prompt review should focus on improving reliability rather than increasing complexity.

---

# Prompt Testing

Reusable prompts should be validated in real projects.

Whenever possible, test a prompt using:

- different repositories;
- different project sizes;
- different AI systems;
- different levels of repository maturity.

A prompt that works only in one specific repository is usually too specialized.

---

# Prompt Naming Convention

Prompt names should describe their purpose.

Recommended naming:

```text
001_PROJECT_INITIALIZATION_PROMPT.md
002_LEGACY_REPOSITORY_AUDIT_PROMPT.md
003_PRODUCT_DISCOVERY_PROMPT.md
004_ARCHITECTURE_REVIEW_PROMPT.md
005_DOCUMENTATION_REVIEW_PROMPT.md
006_TASK_IMPLEMENTATION_PROMPT.md
007_CODE_REVIEW_PROMPT.md
008_RELEASE_REVIEW_PROMPT.md
009_AI_SESSION_HANDOVER_PROMPT.md
```

Avoid names like:

```text
new_prompt.md
prompt2.md
claude_prompt.md
test.md
```

Prompt names should remain meaningful years later.

---

# Prompt Directory Structure

Recommended repository structure:

```text
templates/
└── prompts/
    ├── README.md
    ├── project/
    ├── discovery/
    ├── architecture/
    ├── implementation/
    ├── review/
    ├── release/
    ├── migration/
    ├── knowledge/
    └── archive/
```

Grouping prompts by workflow makes them easier to discover than grouping them by AI provider.

---

# Prompt Metadata

Every reusable prompt should include basic metadata.

Recommended fields:

- Title
- Purpose
- Status
- Version
- Last Updated
- Expected Inputs
- Expected Outputs
- Compatible AI Systems
- Related Documents

Metadata simplifies long-term maintenance.

---

# Prompt Documentation

Every important prompt should explain:

- why it exists;
- when it should be used;
- when it should not be used;
- required repository context;
- expected deliverables;
- known limitations.

Users should understand a prompt without reading its implementation history.

---

# Prompt Collections

Individual prompts are useful.

Prompt collections are more powerful.

Examples:

Repository Initialization Collection

- Repository audit
- Product discovery
- Architecture review
- Documentation review
- Migration strategy

Implementation Collection

- Task briefing
- Implementation
- Code review
- Test review
- Completion review

Release Collection

- Release audit
- Documentation review
- Final QA
- Release checklist

Collections help automate repeatable workflows.

---

# Prompt Evolution

Prompt engineering is an iterative process.

Every real project improves the Prompt Library.

When a better prompting strategy is discovered:

- review it;
- validate it;
- generalize it;
- document it;
- replace the older version if appropriate.

The library should evolve together with the framework.

---

# Prompt Anti-Patterns

Poor prompts often create more work instead of reducing it.

Common anti-patterns include:

## Starting Without Context

Asking an AI system to implement a task without explaining the product, architecture or repository.

---

## Overly Generic Prompts

Requests such as:

> "Improve this."

or

> "Refactor everything."

provide too little guidance.

---

## Over-Specifying Every Step

Micromanaging every implementation detail prevents the AI from contributing useful reasoning.

Provide objectives and constraints rather than dictating every action.

---

## Embedding Temporary Knowledge

Project-specific implementation details should remain in project documentation.

Reusable prompts should remain generic.

---

## Provider Lock-In

Avoid writing prompts that only work with a single AI platform unless absolutely necessary.

The framework aims for provider independence.

---

# Multi-Agent Prompt Strategy

Different AI systems may participate in the same project.

Rather than creating different project workflows, the framework recommends assigning different roles.

Example:

- ChatGPT — Product Strategy
- Claude Code — Repository Review
- Codex CLI — Implementation
- Gemini — Research
- Local LLM — Automation

The workflow remains identical.

Only the assigned agent changes.

This keeps the framework stable as AI capabilities evolve.

---

# Prompt Library Maintenance

The Prompt Library should be treated like source code.

Regular maintenance includes:

- removing obsolete prompts;
- improving successful prompts;
- archiving deprecated prompts;
- updating metadata;
- reviewing compatibility with current AI systems;
- incorporating lessons learned from real projects.

Prompt quality should improve continuously.

---

# Belgrade Metro Case Study

The Belgrade Metro project became the first practical validation of this Prompt Library approach.

During development, multiple AI systems participated in:

- product discovery;
- documentation;
- repository reviews;
- implementation planning;
- code generation;
- architecture reviews;
- task management.

Several lessons emerged:

- repository context produces better results than long conversations;
- review reports should be stored in the repository;
- prompt templates become reusable only after multiple real uses;
- AI agent rules significantly improve consistency;
- different AI systems perform better in different roles.

These observations directly influenced the design of the Prompt Library.

---

# Prompt Library Evolution

The Prompt Library is expected to evolve continuously.

New prompts should not be added simply because they are useful once.

They should first demonstrate long-term value across multiple projects.

As the framework matures, the Prompt Library becomes a curated collection of validated engineering workflows rather than a growing archive of random prompts.

Quality is more important than quantity.

---

# Final Notes

Prompt engineering is not about discovering secret phrases.

It is about creating reliable communication between humans, repositories and AI systems.

The Prompt Library captures proven interaction patterns that reduce ambiguity, improve consistency and accelerate delivery.

Like every other part of the framework, it should evolve through practical experience rather than theory.

Every validated project improves the Prompt Library.

Every improved prompt strengthens future projects.

---

# Related Documents

- `docs/002_CORE_PRINCIPLES.md`
- `docs/003_AI_AGENT_ROLES.md`
- `docs/006_DELIVERY_WORKFLOW.md`
- `docs/009_AI_ASSISTED_MIGRATION.md`
- `templates/prompts/README.md`