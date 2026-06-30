# AI-Assisted Migration

## Status

**Status:** Draft  
**Last Updated:** 2026-06-30

---

# Introduction

Artificial Intelligence significantly accelerates software development.

However, AI also creates a new class of legacy.

Projects developed with AI often accumulate knowledge outside the repository.

Important decisions may exist only in:

- AI conversations;
- terminal sessions;
- generated patches;
- temporary prompts;
- implementation history;
- human memory.

As projects grow, this hidden knowledge becomes increasingly difficult to recover.

The AI Product Delivery Framework introduces a structured process for migrating AI-assisted projects into a maintainable, repository-driven workflow.

---

# What Is AI Legacy?

AI Legacy is accumulated project knowledge that is not properly represented inside the repository.

Examples include:

- undocumented architectural decisions;
- forgotten prompt history;
- implementation rationale;
- review findings;
- temporary workarounds;
- abandoned experiments;
- conflicting AI-generated documentation.

Unlike traditional legacy, AI legacy often exists outside version control.

---

# Why AI Projects Become Difficult

AI accelerates implementation faster than documentation.

As a result:

- code evolves;
- documentation diverges;
- prompts change;
- assumptions change;
- repository structure changes.

Without a structured process, knowledge fragments across many systems.

This creates uncertainty for both humans and future AI agents.

---

# Migration Objectives

AI-assisted migration aims to:

- reconstruct project knowledge;
- identify the current source of truth;
- recover important architectural decisions;
- archive obsolete AI artifacts;
- preserve useful context;
- eliminate conflicting documentation;
- establish a repeatable workflow.

Migration is primarily a knowledge reconstruction exercise.

---

# AI Migration Lifecycle

```text
Existing AI Project
        │
        ▼
Repository Audit
        │
        ▼
Conversation Review
        │
        ▼
Knowledge Recovery
        │
        ▼
Documentation Reconstruction
        │
        ▼
Architecture Alignment
        │
        ▼
Task Reconstruction
        │
        ▼
Agent Rules
        │
        ▼
Controlled AI Workflow
```

Every stage reduces uncertainty.

---

# Recovering Knowledge

Before writing new code, recover existing knowledge.

Possible sources include:

- Git history;
- README files;
- architecture documents;
- product documentation;
- AI conversations;
- review reports;
- issue trackers;
- commit history;
- changelogs;
- checkpoints.

Recovered knowledge should be written back into the repository.

The repository becomes the permanent memory.

---

# Conversations Are Not Documentation

AI conversations are valuable.

They are not documentation.

Conversations should produce:

- documents;
- decisions;
- reports;
- tasks;
- architecture updates.

Important conclusions should never remain only inside chat history.

---

# Prompt History

Prompt history often contains valuable engineering decisions.

Examples:

- migration strategies;
- architecture alternatives;
- rejected ideas;
- implementation constraints;
- discovered risks.

Useful prompt outcomes should be summarized rather than copied.

The repository should contain conclusions, not chat transcripts.

---

# Knowledge Recovery

Knowledge recovery is the process of reconstructing the true state of a project.

The objective is not to recover every historical detail.

The objective is to recover enough validated knowledge to safely continue delivery.

Recovered knowledge should become part of the repository.

Knowledge that remains only inside conversations will eventually be lost.

---

# Sources Of Knowledge

Project knowledge may exist in many places.

Examples include:

- Git history;
- documentation;
- AI conversations;
- review reports;
- architecture discussions;
- issue trackers;
- project management tools;
- terminal output;
- implementation reports;
- checkpoints;
- release notes;
- human experience.

The migration process should identify all significant knowledge sources.

---

# Knowledge Classification

Recovered knowledge should be classified.

## Current

Matches the current product direction.

Should become part of the active documentation.

---

## Historical

Explains previous decisions.

Useful for understanding the project.

Should usually remain archived.

---

## Conflicting

Contradicts another source.

Requires human review.

AI should never resolve important conflicts autonomously.

---

## Unverified

Cannot be confirmed.

Should not become part of the official documentation until validated.

---

## Lost

Known to have existed but no longer recoverable.

The framework accepts that not every decision can be reconstructed.

---

# Conversation Mining

AI conversations often contain valuable decisions.

However, conversations should not become permanent documentation.

Instead, extract:

- product decisions;
- architecture decisions;
- implementation constraints;
- discovered risks;
- rejected alternatives;
- future ideas.

The result should be concise documentation rather than archived chat transcripts.

---

# Prompt Evolution

Prompts evolve throughout the project.

Early prompts often become outdated.

Instead of preserving every prompt, preserve:

- prompt purpose;
- expected inputs;
- expected outputs;
- lessons learned;
- reusable structure.

Prompt libraries should evolve alongside the framework.

---

# AI Session Handover

Long projects rarely fit into a single AI session.

Every session should end with a structured handover.

A handover should summarize:

- completed work;
- current repository state;
- open questions;
- unresolved risks;
- recommended next steps;
- documents that changed.

Future AI sessions should begin by reading repository documentation rather than previous chat history.

---

# Multi-Agent Collaboration

Different AI systems have different strengths.

One project may use:

- ChatGPT for product strategy;
- Claude Code for implementation;
- Gemini for research;
- Codex CLI for coding;
- local models for automation.

The framework treats AI systems as interchangeable roles.

Knowledge belongs to the repository.

Not to any individual AI.

---

# Repository As Long-Term Memory

The repository is the permanent memory of the project.

Every important conclusion should eventually exist inside:

- documentation;
- architecture;
- tasks;
- reports;
- checkpoints;
- changelog;
- decision records.

If knowledge exists only inside AI conversations, it should be considered temporary.

---

# AI Review Reports

AI reviews should not disappear after the conversation ends.

Significant reviews should be stored.

Recommended location:

```text
docs/reviews/
```

Recommended filename:

```text
YYYY-MM-DD_HH-MM_<TOPIC>_REVIEW.md
```

Review reports should include:

- scope;
- repository revision;
- findings;
- risks;
- recommendations;
- unanswered questions.

Review reports become part of the project's engineering history.

---

# AI Migration Checklist

Before continuing an existing AI-assisted project:

- [ ] Repository state understood.
- [ ] Product documentation reviewed.
- [ ] Architecture reviewed.
- [ ] Current source of truth identified.
- [ ] Legacy documentation classified.
- [ ] Agent rules reviewed.
- [ ] Prompt library reviewed.
- [ ] Existing tasks reviewed.
- [ ] Knowledge gaps identified.
- [ ] Migration strategy documented.

Only then should implementation continue.

---

# AI Migration Anti-Patterns

## Trusting Chat History

Chat history is temporary.

Repository documentation is permanent.

---

## Multiple Sources Of Truth

Conflicting documentation leads to conflicting implementations.

Always establish one authoritative source.

---

## Starting Coding Immediately

Migration begins with understanding.

Not implementation.

---

## Ignoring Previous AI Work

Even imperfect AI-generated work may contain valuable knowledge.

Review before replacing.

---

## Blindly Accepting Previous AI Work

Previous AI output should not automatically become the new source of truth.

Everything important should be reviewed.

---

## Missing Handover

Ending an AI session without documenting progress creates future migration work.

Every significant session should leave the repository in a better state.

---

# Belgrade Metro Case Study

The Belgrade Metro project demonstrates a typical AI-assisted migration.

Over time the project accumulated:

- multiple documentation systems;
- changing product direction;
- evolving repository structure;
- new task organization;
- multiple AI agents;
- implementation reviews;
- architecture pivots.

The migration process focused on:

- identifying the current product vision;
- rebuilding documentation around that vision;
- separating legacy documentation;
- redefining repository structure;
- introducing repeatable AI workflows;
- documenting review practices;
- treating the repository as the primary knowledge base.

The lessons learned from this migration directly influenced the AI Product Delivery Framework.

---

# Final Notes

Artificial Intelligence dramatically accelerates software development.

It also dramatically accelerates knowledge fragmentation if used without discipline.

The purpose of AI-assisted migration is not simply to continue writing code.

It is to transform fragmented conversations into structured project knowledge.

Every migration should leave the repository easier to understand than before.

That is the foundation for long-term AI-assisted software delivery.

---

# Related Documents

- `docs/003_AI_AGENT_ROLES.md`
- `docs/005_PRODUCT_DISCOVERY.md`
- `docs/006_DELIVERY_WORKFLOW.md`
- `docs/008_LEGACY_MIGRATION.md`
- `docs/011_PROMPT_LIBRARY.md`
- `templates/prompts/003_AI_ASSISTED_LEGACY_AUDIT_PROMPT.md`
- `templates/prompts/008_REVIEW_AGENT_PROMPT.md`