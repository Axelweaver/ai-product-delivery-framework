# Product Discovery

## Status

**Status:** Draft  
**Last Updated:** 2026-06-30

---

# Introduction

Every successful software product begins long before the first line of code is written.

Unfortunately, many projects skip the most important stage.

The common workflow often looks like this:

```text
Idea

↓

Let's start coding
```

Sometimes a design prototype is added.

Sometimes a backlog is created.

However, in many projects the product itself has never been properly discovered.

The AI Product Delivery Framework introduces a different approach.

Instead of treating Product Discovery as an optional activity, the framework considers it the foundation of the entire delivery process.

Product Discovery reduces uncertainty before implementation begins.

It aligns business goals, user needs, technical decisions and delivery planning.

---

# What Is Product Discovery?

Product Discovery is the structured process of understanding:

- what should be built;
- why it should exist;
- who it serves;
- how success will be measured;
- what should be built first;
- what should not be built yet.

Discovery is not documentation for its own sake.

Discovery is decision making.

Every discovery activity should reduce uncertainty.

---

# Discovery Never Ends

One of the most common misconceptions is that Product Discovery happens only before development.

The framework rejects this idea.

Discovery is continuous.

The lifecycle looks like this:

```text
Idea
    │
    ▼
Discovery
    │
    ▼
MVP
    │
    ▼
Users
    │
    ▼
Feedback
    │
    ▼
Discovery
    │
    ▼
Improved MVP
    │
    ▼
Feedback
    │
    ▼
Discovery
```

Every release creates new information.

Every user interaction improves understanding.

Every product evolves.

Discovery evolves with it.

---

# Goals Of Product Discovery

The objective is not to produce documents.

The objective is to answer important questions before implementation becomes expensive.

Discovery should answer:

- What problem are we solving?
- Who experiences this problem?
- Why does it matter?
- How are people solving it today?
- Why is our solution better?
- What is the smallest useful product?
- How will we validate our assumptions?
- How will success be measured?

If these questions remain unanswered, implementation carries unnecessary risk.

---

# Product Discovery Principles

The framework follows several principles.

## Start With The Problem

People do not buy features.

They solve problems.

Always understand the problem before designing the solution.

---

## Validate Assumptions

Every assumption is a hypothesis until validated.

Avoid treating opinions as facts.

---

## Focus On Users

Technology is not the customer.

Architecture is not the customer.

The user is the customer.

Every discovery activity should improve user understanding.

---

## Keep The MVP Small

A smaller MVP reaches users faster.

User feedback is more valuable than internal assumptions.

---

## Documentation Is A Tool

Documentation exists to preserve knowledge.

It should support decisions.

It should not become bureaucracy.

---

# The Discovery Pipeline

The framework recommends the following sequence.

```text
Idea
    │
    ▼
Problem Statement
    │
    ▼
Target Audience
    │
    ▼
Market Research
    │
    ▼
Competitor Analysis
    │
    ▼
Business Goals
    │
    ▼
Success Metrics
    │
    ▼
Product Vision
    │
    ▼
Product Principles
    │
    ▼
User Personas
    │
    ▼
User Journeys
    │
    ▼
Information Architecture
    │
    ▼
UX Principles
    │
    ▼
Screen Specifications
    │
    ▼
Product Roadmap
    │
    ▼
MVP Scope
    │
    ▼
Technical Architecture
    │
    ▼
Epic Planning
    │
    ▼
Task Planning
    │
    ▼
Implementation
```

Not every project requires the same depth.

However, changing the order usually increases project risk.

---

# Discovery Phases

## Phase 1 — Idea

Every product begins with an idea.

Ideas should be captured immediately.

The goal is not evaluation.

The goal is preservation.

Typical outputs:

- idea description;
- initial assumptions;
- possible users;
- initial value proposition.

---

## Phase 2 — Problem Statement

Clearly define the problem.

Good problem statements describe reality rather than proposed solutions.

Avoid:

> "Users need AI."

Prefer:

> "Users spend too much time performing repetitive work."

A problem statement should be measurable whenever possible.

---

## Phase 3 — Target Audience

Define who experiences the problem.

Avoid designing for everyone.

Document:

- primary audience;
- secondary audience;
- excluded audience;
- expected user expertise;
- environment;
- limitations.

---

## Phase 4 — Market Research

Study the market before building.

Research should include:

- competitors;
- substitutes;
- regulations;
- trends;
- pricing;
- customer expectations.

Research reduces strategic risk.

---

## Phase 5 — Competitor Analysis

Understand existing solutions.

For each competitor identify:

- strengths;
- weaknesses;
- positioning;
- pricing;
- missing opportunities.

The objective is not copying competitors.

The objective is understanding the market.

---

# AI In Product Discovery

AI accelerates every discovery phase.

Examples:

- generating interview questions;
- researching competitors;
- organizing documentation;
- identifying missing assumptions;
- proposing user personas;
- reviewing consistency;
- highlighting risks.

AI does not replace human judgment.

The human remains responsible for product direction.

---

# Discovery Deliverables

A completed discovery process usually produces:

- Product Vision
- Product Principles
- UX Principles
- Information Architecture
- Screen Specifications
- Product Roadmap
- MVP Definition
- Initial Architecture
- Epic Structure
- Initial Task Backlog

These become the primary inputs for delivery.

---

# Discovery For Different Project Types

Product Discovery is not identical for every project.

The framework supports different discovery paths depending on the starting point.

---

## Greenfield Discovery

Greenfield Discovery is used when the project starts from an idea and no repository exists yet.

The objective is to transform an idea into a clear product direction before implementation begins.

Typical questions:

- What is the product idea?
- Who is the target user?
- What problem does the user have?
- Why does this problem matter now?
- What alternatives already exist?
- Why should this product exist?
- What is the smallest useful MVP?
- How can the hypothesis be validated?
- What does success look like?

Typical outputs:

- Product Vision
- Product Principles
- Target Audience
- User Problems
- MVP Scope
- Product Roadmap
- Initial Architecture Direction
- Initial Epic Backlog

Greenfield Discovery should prevent random coding.

---

## Legacy Discovery

Legacy Discovery is used when a repository already exists, but it was not created using this framework.

The objective is not to erase the existing project.

The objective is to understand it, classify it and decide how to move forward safely.

Typical questions:

- What does the existing product do?
- Which parts are working?
- Which parts are outdated?
- What documentation exists?
- What architecture exists?
- What code is still useful?
- What should be archived?
- What should be rewritten?
- What should be preserved?
- What is the target product direction now?

Typical outputs:

- Repository Audit
- Documentation Audit
- Architecture Review
- Legacy Classification
- Migration Strategy
- Updated Product Documentation
- Updated Architecture Documentation
- Rebuilt Task Backlog

Legacy Discovery should respect existing value.

Not all legacy work is bad.

Not all old decisions were wrong.

---

## AI-Assisted Legacy Discovery

AI-Assisted Legacy Discovery is used when a project already involved AI tools before adopting this framework.

This is a special case.

The repository may contain code, generated documentation, partial prompts, agent rules and decisions hidden inside chat history.

The objective is to reconstruct reliable project knowledge.

Typical questions:

- Which AI tools were used?
- What did they generate?
- Which decisions exist only in chat history?
- Which documents contradict each other?
- Which AI-generated artifacts are still useful?
- Which artifacts should be archived?
- What is the current product direction?
- What should become the source of truth?

Typical outputs:

- AI History Summary
- Knowledge Reconstruction Report
- Documentation Consistency Review
- Source Of Truth Definition
- Legacy Archive Plan
- Updated Agent Rules
- Updated Task Structure

AI-Assisted Legacy Discovery should reduce chaos created by disconnected AI sessions.

---

# Discovery Questions

The following questions can be used during Product Discovery.

Not every project needs every question.

The human owner decides the necessary depth.

---

## Problem Questions

- What problem are we solving?
- Who has this problem?
- How often does the problem happen?
- How painful is the problem?
- What happens if the problem is not solved?
- How do users solve it today?
- Why are current solutions insufficient?

---

## User Questions

- Who is the primary user?
- Who is the secondary user?
- Who is explicitly not the target user?
- What does the user already know?
- What environment does the user operate in?
- What constraints does the user have?
- What does the user need to accomplish quickly?

---

## Business Questions

- Why should this product exist?
- What business goal does it support?
- How can it generate value?
- How can it generate revenue?
- What is the expected market?
- What is the cost of building it?
- What is the cost of maintaining it?
- What is the opportunity cost?

---

## MVP Questions

- What is the smallest useful version?
- Which feature validates the main hypothesis?
- Which features are nice to have?
- Which features can be delayed?
- What must be true for the MVP to be successful?
- What can be intentionally mocked?
- What can be manual at first?

---

## Risk Questions

- What can make this product fail?
- What assumptions are unvalidated?
- What technical risks exist?
- What business risks exist?
- What legal or compliance risks exist?
- What user adoption risks exist?
- What can be tested before implementation?

---

## Differentiation Questions

- Why would users choose this product?
- What does it do better than alternatives?
- What does it intentionally not do?
- What is the product's unique angle?
- What should users remember about it?

---

# Discovery Workshops

Discovery can be performed as a structured workshop with AI assistance.

A practical workshop flow:

1. Human describes the idea.
2. Strategic AI asks clarification questions.
3. Research AI investigates market and competitors.
4. Strategic AI summarizes opportunities and risks.
5. Human selects product direction.
6. Documentation AI creates product documents.
7. Review AI checks for contradictions.
8. Human approves or revises the result.

The workshop may happen in one session or across several days.

The important part is that outputs are saved into the repository.

---

# AI Roles In Discovery

Different AI roles participate in discovery differently.

## Strategic AI

Strategic AI helps define:

- product vision;
- user problems;
- business goals;
- MVP scope;
- roadmap;
- prioritization.

---

## Research AI

Research AI helps investigate:

- market context;
- competitors;
- user behavior;
- regulations;
- platforms;
- technologies.

---

## Documentation AI

Documentation AI converts discovery results into stable repository documents.

---

## Review AI

Review AI checks whether discovery outputs are:

- consistent;
- complete enough;
- actionable;
- aligned with business goals;
- free from obvious contradictions.

---

# Discovery Output Structure

A mature discovery process should usually create the following documentation structure:

```text
docs/product/
├── 001_PRODUCT_VISION.md
├── 002_PRODUCT_PRINCIPLES.md
├── 003_UX_PRINCIPLES.md
├── 004_INFORMATION_ARCHITECTURE.md
├── 005_CORE_USER_EXPERIENCE.md
├── 006_SCREEN_SPECIFICATIONS.md
├── 007_VISUAL_IDENTITY.md
├── 008_DESIGN_LANGUAGE.md
├── 009_MOTION_AND_ANIMATIONS.md
├── 010_LOCALIZATION.md
├── 011_ACCESSIBILITY.md
├── 012_RELEASE_CRITERIA.md
├── 013_PRODUCT_ROADMAP.md
└── 014_CHANGELOG.md
```

Not every project needs all documents immediately.

The structure can grow with the product.

---

# Definition Of Ready For Architecture

Product Discovery is ready to move into architecture when the following are clear:

- product vision;
- target audience;
- primary user problems;
- MVP scope;
- core user flows;
- main product constraints;
- known risks;
- success criteria.

Architecture before this point is likely to be based on assumptions.

---

# Definition Of Ready For Implementation

Implementation should not begin until:

- product direction is clear;
- architecture direction is documented;
- MVP scope is approved;
- tasks are defined;
- acceptance criteria exist;
- the implementation agent has enough context.

This does not mean every future decision must be known.

It means the next implementation step must be clear and safe.

---

# Discovery Anti-Patterns

## Starting With Technology

Choosing a stack before understanding the product often creates unnecessary constraints.

---

## Building For Everyone

A product for everyone usually serves no one well.

---

## Confusing Ideas With Validated Problems

An idea is not evidence.

Discovery should separate assumptions from facts.

---

## Endless Discovery

Discovery should reduce risk, not replace delivery.

If discovery never leads to implementation, it becomes avoidance.

---

## Copying Competitors Blindly

Competitor research should inform positioning.

It should not replace original product thinking.

---

## Letting AI Invent The Product

AI can suggest possibilities.

The human must own the decision.

---

# Discovery And MVP

Discovery should protect MVP scope.

Every new idea should be classified as:

- MVP requirement;
- post-MVP improvement;
- experiment;
- research item;
- rejected idea.

This prevents scope from expanding endlessly.

The question should always be:

> Does this help validate the main hypothesis now?

If not, it probably does not belong in the MVP.

---

# Discovery And Monetization

For commercial products, discovery must include monetization thinking early.

This does not mean the MVP must implement payment immediately.

It means the product should have a plausible path to value capture.

Questions:

- Who would pay?
- Why would they pay?
- When would they pay?
- What value is being captured?
- What pricing models are realistic?
- What must be validated before monetization?

Ignoring monetization until late stages increases business risk.

---

# Discovery And Personal Strategy

For independent developers and founders, product discovery also connects to personal strategy.

A project should be evaluated against:

- personal goals;
- available time;
- financial runway;
- required skills;
- market opportunity;
- expected maintenance cost;
- portfolio value.

A technically interesting product may still be a poor strategic choice.

A simple product with clear business value may be more important.

---

# Real Example — Belgrade Metro

Belgrade Metro is an example of discovery evolving during real work.

The project started with a transport navigation idea.

During discovery, the product direction changed from a generic schematic metro-style interface toward a Map First experience based on the real geography of Belgrade.

This happened because the city does not yet have a widely recognized metro map.

Therefore, the product needed to make users immediately feel:

> This is Belgrade.

The discovery process changed:

- product principles;
- information architecture;
- map strategy;
- task structure;
- architecture needs.

This demonstrates why discovery is not a one-time activity.

Discovery can reveal that the original implementation direction is wrong.

---

# Practical Discovery Rule

Before starting implementation, answer these questions:

1. What problem are we solving?
2. Who has this problem?
3. Why does this product need to exist?
4. What is the MVP?
5. What is explicitly not in the MVP?
6. What is the main hypothesis?
7. How will we validate it?
8. What documentation exists?
9. What decisions are still missing?
10. Which AI role should work next?

If these questions cannot be answered, continue discovery.

---

# Final Notes

Product Discovery is not a formality.

It is the foundation of product delivery.

AI can accelerate discovery dramatically, but it can also accelerate wrong assumptions if the human does not stay in control.

The framework uses discovery to connect:

- human goals;
- user needs;
- business value;
- product decisions;
- architecture;
- delivery planning.

The purpose is simple:

> Build the right thing before building the thing right.

---

# Related Documents

- `docs/001_FRAMEWORK_VISION.md`
- `docs/002_CORE_PRINCIPLES.md`
- `docs/003_AI_AGENT_ROLES.md`
- `docs/004_HUMAN_ROLE.md`
- `docs/006_DELIVERY_WORKFLOW.md`
- `docs/007_MVP_FIRST.md`
- `templates/prompts/001_GREENFIELD_DISCOVERY_PROMPT.md`
- `templates/prompts/002_LEGACY_REPOSITORY_AUDIT_PROMPT.md`
- `templates/prompts/003_AI_ASSISTED_LEGACY_AUDIT_PROMPT.md`
