# AI Agent Roles

## Status

**Status:** Draft  
**Last Updated:** 2026-06-30

---

# Introduction

One of the fundamental ideas of the AI Product Delivery Framework is the separation of **roles** from **AI providers**.

The framework intentionally avoids depending on a specific AI model or vendor.

Instead of asking:

> "Should I use ChatGPT or Claude?"

the framework asks:

> "Which role is required at this stage of the project?"

A role defines responsibilities, expected outputs, required context and decision boundaries.

Different AI systems may perform the same role.

Likewise, the same AI system may perform different roles in different stages of the project.

This separation makes the framework future-proof and provider-independent.

---

# Human First

Before defining AI roles, one principle must be absolutely clear.

The human always remains:

- Product Owner
- Final Decision Maker
- Business Representative
- Vision Holder

AI systems never own the product.

They assist.

They analyze.

They recommend.

They implement.

They review.

But they never become the owner of business decisions.

This principle is defined in detail in **004_HUMAN_ROLE.md**.

---

# Role Lifecycle

During a product lifecycle, different AI roles participate at different moments.

A simplified flow looks like this:

```text
Idea
    │
    ▼
Strategic AI
    │
    ▼
Research AI
    │
    ▼
Documentation AI
    │
    ▼
Architecture AI
    │
    ▼
Planning AI
    │
    ▼
Implementation AI
    │
    ▼
Review AI
    │
    ▼
QA AI
    │
    ▼
Release AI
```

Not every project requires every role.

Small MVPs may combine multiple roles into one AI session.

Large projects may assign different providers to different roles.

---

# General Responsibilities

Every AI role shares several responsibilities.

An AI agent should:

- follow the framework documentation;
- work from repository context;
- explain important decisions;
- preserve project knowledge;
- identify contradictions;
- report uncertainties;
- prefer references over duplication.

An AI agent should never:

- silently invent requirements;
- overwrite business decisions;
- ignore documented architecture;
- discard historical knowledge;
- rewrite large parts of a project without justification.

---

# Strategic AI

## Purpose

Strategic AI helps shape the product before implementation begins.

It operates at the highest level.

It focuses on business value instead of implementation details.

---

## Responsibilities

Strategic AI helps with:

- product vision;
- business goals;
- MVP definition;
- product principles;
- roadmap planning;
- prioritization;
- feature evaluation;
- trade-off analysis;
- documentation structure.

---

## Expected Inputs

Strategic AI usually receives:

- business idea;
- customer problem;
- market context;
- user goals;
- existing documentation.

---

## Expected Outputs

Typical outputs include:

- Product Vision
- Product Principles
- Roadmap
- Discovery documents
- Feature prioritization
- Architecture recommendations

---

## What Strategic AI Should Avoid

Strategic AI should not:

- write production code;
- optimize implementation details;
- redesign architecture without business reasons;
- solve low-level bugs.

---

# Research AI

## Purpose

Research AI gathers external knowledge required for informed decisions.

It reduces assumptions.

It increases confidence.

---

## Responsibilities

Research AI performs:

- market research;
- competitor analysis;
- technology comparison;
- legal research;
- platform limitations;
- SDK analysis;
- API investigation;
- UX references;
- accessibility research.

---

## Expected Outputs

Research reports.

Comparison matrices.

Risk analysis.

Technology recommendations.

External references.

---

## What Research AI Should Avoid

Research AI should not:

- choose product direction independently;
- modify documentation;
- implement features.

Research informs.

Humans decide.

---

# Documentation AI

## Purpose

Documentation AI transforms ideas into structured project knowledge.

Its goal is clarity.

Not implementation.

---

## Responsibilities

Documentation AI creates and maintains:

- product documentation;
- architecture documentation;
- task documentation;
- README files;
- onboarding documents;
- migration guides;
- changelogs;
- ADR/PDR records.

---

## Quality Goals

Documentation should be:

- consistent;
- versioned;
- discoverable;
- easy to review;
- easy to update;
- referenced instead of duplicated.

---

## Anti-patterns

Documentation AI should never:

- duplicate large sections;
- contradict architecture;
- invent implementation details;
- leave stale references.

---

# Architecture AI

## Purpose

Architecture AI transforms product requirements into technical structure.

Its objective is sustainable delivery.

Not theoretical perfection.

---

## Responsibilities

Architecture AI defines:

- project structure;
- module boundaries;
- dependency rules;
- state management;
- data flow;
- API boundaries;
- repository organization;
- migration strategy.

---

## Expected Deliverables

Examples include:

- Architecture Overview
- Data Model
- Component diagrams
- Module decomposition
- Integration strategy

---

## Anti-patterns

Architecture AI should avoid:

- unnecessary abstraction;
- premature optimization;
- architecture for imaginary requirements;
- rewriting stable systems without measurable value.

---

# Planning AI

## Purpose

Planning AI converts documentation into executable work.

Planning is the bridge between architecture and implementation.

---

## Responsibilities

Planning AI performs:

- epic decomposition;
- task decomposition;
- dependency analysis;
- milestone planning;
- backlog refinement;
- implementation sequencing.

---

## Deliverables

Planning AI produces:

- epics;
- task documents;
- execution order;
- dependency graphs;
- milestone definitions.

---

## Planning Principles

Tasks should be:

- independent whenever possible;
- reviewable;
- testable;
- small enough to complete safely;
- traceable back to product documentation.

---

# Implementation AI

## Purpose

Implementation AI produces production-ready code.

It is responsible for delivery.

Not for redefining the product.

---

## Responsibilities

Implementation AI:

- writes code;
- updates documentation when required;
- follows repository rules;
- respects architecture;
- executes implementation tasks;
- reports blockers;
- suggests improvements without changing direction independently.

---

## Required Context

Implementation AI should receive:

- task document;
- architecture documents;
- coding rules;
- repository guidelines;
- project context.

It should never start from isolated prompts without project context.

---

## Success Criteria

Implementation is successful when:

- requirements are satisfied;
- tests pass;
- documentation remains consistent;
- architecture is respected;
- changes remain understandable.

---

# Review AI

## Purpose

Review AI performs independent quality control.

It checks whether the work is consistent, complete and aligned with the framework.

Review AI should not be the same agent that performed the original implementation whenever practical.

---

## Responsibilities

Review AI checks:

- product consistency;
- documentation consistency;
- architecture alignment;
- implementation quality;
- task completeness;
- missing requirements;
- hidden risks;
- contradictions;
- test coverage;
- migration safety.

---

## Expected Outputs

Review AI produces:

- review reports;
- risk lists;
- recommended changes;
- blocker lists;
- questions for human decision;
- approval or rejection recommendations.

---

## Review Boundaries

Review AI should not silently fix everything it finds.

Its primary task is to detect and explain issues.

Changes should be applied only after human approval or a clearly assigned implementation task.

---

# QA AI

## Purpose

QA AI helps validate that the product works as expected.

It focuses on behavior, quality, edge cases and release readiness.

---

## Responsibilities

QA AI helps with:

- test planning;
- acceptance criteria;
- manual test scenarios;
- regression testing;
- exploratory testing ideas;
- edge case detection;
- accessibility checks;
- localization checks;
- release checklists.

---

## Expected Outputs

QA AI produces:

- QA checklists;
- test cases;
- regression plans;
- bug reports;
- release readiness reports.

---

## QA AI Should Avoid

QA AI should not:

- redefine product requirements;
- accept failed behavior as correct;
- ignore user-facing defects because implementation is technically complete.

---

# Release AI

## Purpose

Release AI supports the final steps before publishing or delivering a product version.

It helps ensure that the product is ready for users.

---

## Responsibilities

Release AI helps with:

- release checklists;
- changelog preparation;
- version notes;
- store descriptions;
- screenshots planning;
- build validation;
- final documentation review;
- rollback planning;
- known issues documentation.

---

## Expected Outputs

Release AI produces:

- release notes;
- release readiness reports;
- publication checklists;
- post-release monitoring plans.

---

# Role Interaction

AI roles should work as a system.

They should not operate as isolated conversations with no shared context.

A typical interaction looks like this:

```text
Strategic AI defines product direction
        │
        ▼
Documentation AI captures it
        │
        ▼
Architecture AI designs structure
        │
        ▼
Planning AI creates executable tasks
        │
        ▼
Implementation AI performs delivery
        │
        ▼
Review AI checks consistency
        │
        ▼
QA AI validates behavior
        │
        ▼
Release AI prepares publication
```

Every handoff should preserve context.

Every major output should be saved into the repository.

---

# Context Handover

Context handover is one of the most important parts of AI-assisted delivery.

An AI role should never depend only on previous chat history.

Important context should be stored in files.

A good handover includes:

- current repository state;
- relevant documentation;
- task scope;
- decisions already made;
- unresolved questions;
- known risks;
- expected output format.

---

## Minimum Handover Package

For most tasks, the next AI role should receive:

```text
README.md
project rules
project context
relevant product documents
relevant architecture documents
current task file
recent review or report files
```

For implementation tasks, include:

```text
agent rules
execution protocol
validation requirements
Git workflow
acceptance criteria
```

For review tasks, include:

```text
original task
implemented changes
relevant documentation
git diff
known limitations
```

---

# Role Composition

Small projects may combine multiple roles into a single AI session.

For example, one AI session may act as both Strategic AI and Documentation AI during early discovery.

However, role boundaries should remain explicit.

The question is not:

> Which AI model is speaking?

The question is:

> Which role is this AI performing right now?

---

## Acceptable Role Combinations

Common combinations:

- Strategic AI + Documentation AI
- Architecture AI + Planning AI
- Review AI + QA AI
- Research AI + Strategic AI

---

## Risky Role Combinations

Risky combinations:

- Implementation AI + final Review AI
- Strategic AI + unchecked Implementation AI
- Research AI + final business decision maker
- Documentation AI + silent architecture owner

These combinations may be used in small projects, but the risks should be understood.

---

# Provider Mapping

The framework does not require specific vendors.

Possible provider mapping:

| Role | Possible Tools |
|---|---|
| Strategic AI | ChatGPT, Claude, Gemini, Grok, local LLM |
| Research AI | ChatGPT with web, Gemini, Perplexity-like tools, browser-enabled AI |
| Documentation AI | ChatGPT, Claude, Gemini, local LLM |
| Architecture AI | ChatGPT, Claude, Gemini, senior developer with AI support |
| Planning AI | ChatGPT, Claude, Gemini |
| Implementation AI | Claude Code, Codex CLI, Cursor Agent, Aider, Cline |
| Review AI | ChatGPT, Claude, Gemini, Grok, local LLM |
| QA AI | ChatGPT, Claude, Gemini, test-generation tools |
| Release AI | ChatGPT, Claude, Gemini |

The mapping is flexible.

The role definitions are more important than the tools.

---

# Recommended Workflows

## New Product Workflow

```text
Human idea
    ↓
Strategic AI discovery
    ↓
Documentation AI creates product docs
    ↓
Architecture AI creates technical structure
    ↓
Planning AI creates epics and tasks
    ↓
Implementation AI delivers MVP
    ↓
Review AI audits quality
    ↓
QA AI validates behavior
    ↓
Release AI prepares launch
```

---

## Existing Repository Workflow

```text
Existing repository
    ↓
Review AI performs repository audit
    ↓
Documentation AI reconstructs knowledge
    ↓
Architecture AI identifies current structure
    ↓
Strategic AI aligns product direction
    ↓
Planning AI creates migration plan
    ↓
Implementation AI applies controlled changes
    ↓
Review AI validates migration
```

---

## Existing AI-Assisted Project Workflow

```text
Repository + AI chat history
    ↓
Documentation AI extracts important knowledge
    ↓
Review AI identifies contradictions
    ↓
Strategic AI reconstructs product intent
    ↓
Architecture AI defines target structure
    ↓
Planning AI creates migration tasks
    ↓
Implementation AI stabilizes repository
    ↓
Review AI confirms consistency
```

---

# Anti-Patterns

## One AI Does Everything Without Boundaries

This creates unclear responsibility.

The same model may perform multiple roles, but the role must be explicit.

---

## Chat History As Source Of Truth

Important project knowledge must not live only in conversations.

If a decision matters, save it into the repository.

---

## Implementation Before Product Direction

Writing code before product discovery often creates waste.

The framework prefers product clarity before implementation.

---

## Review By The Same Context Only

A model reviewing its own output may miss problems.

Independent review reduces blind spots.

---

## Provider Lock-In

The framework should not depend on one AI vendor.

Tools change.

Roles remain.

---

# Real Project Examples

## Belgrade Metro

Belgrade Metro uses this framework as a real validation project.

Example role mapping:

- Strategic AI: product vision, Map First UX, roadmap, task decomposition;
- Implementation AI: Flutter code implementation through CLI agent;
- Review AI: documentation and architecture review;
- Documentation AI: product docs, task docs, epic README files;
- Research AI: map assets, transport data, localization and platform research.

The project revealed the importance of:

- repository-based context;
- archived legacy documentation;
- epic folders;
- review reports saved as files;
- separating product direction from implementation.

---

## Uči Reči

Uči Reči is a language-learning application concept.

It can use the framework as a new or partially existing product.

Possible role mapping:

- Strategic AI: product discovery and monetization model;
- Research AI: language learning market and competitor analysis;
- Documentation AI: product documentation;
- Architecture AI: mobile app architecture;
- Implementation AI: Flutter or native implementation;
- Review AI: MVP scope and learning loop review.

---

## Prodajko

Prodajko is a marketplace/classifieds product concept.

It requires stronger business, monetization and marketplace strategy.

Possible role mapping:

- Strategic AI: marketplace positioning;
- Research AI: competitor and local market research;
- Architecture AI: marketplace platform architecture;
- Planning AI: phased rollout and moderation workflow;
- Implementation AI: backend, frontend and mobile delivery;
- Review AI: risk and scalability review.

---

# Practical Rule

Before starting any AI-assisted work, define:

1. Which role is needed?
2. Which AI tool will perform it?
3. What context does it need?
4. What output is expected?
5. Who reviews the output?
6. Where will the result be stored?

If these questions are unclear, the task is not ready.

---

# Final Notes

AI agents are accelerators.

They are not a substitute for ownership.

The framework works best when each AI system has:

- a clear role;
- clear context;
- clear boundaries;
- clear expected output;
- clear review process.

This makes AI-assisted delivery predictable, repeatable and scalable across projects.

---

# Related Documents

- `docs/001_FRAMEWORK_VISION.md`
- `docs/002_CORE_PRINCIPLES.md`
- `docs/004_HUMAN_ROLE.md`
- `docs/005_PRODUCT_DISCOVERY.md`
- `docs/006_DELIVERY_WORKFLOW.md`
- `templates/agents/STRATEGIC_AI_RULES.md`
- `templates/agents/IMPLEMENTATION_AI_RULES.md`
- `templates/agents/REVIEW_AI_RULES.md`
- `templates/agents/RESEARCH_AI_RULES.md`
