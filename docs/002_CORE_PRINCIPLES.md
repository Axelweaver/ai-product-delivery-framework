# Core Principles

## Status

**Status:** Draft  
**Last Updated:** 2026-06-30

---

# Introduction

These principles define the philosophy of the AI Product Delivery Framework.

Every workflow, template, playbook, prompt and architectural recommendation in this framework must align with these principles.

When two possible solutions exist, the one that better follows these principles should normally be preferred.

These principles are intentionally stable.

Processes, templates and AI tools may evolve over time.

The principles should change only when significant practical experience proves that a better approach exists.

---

# Product Principles

---

## Principle 01 — Product Over Code

### Statement

The primary objective is to build successful products, not perfect software.

### Rationale

Software has value only when it solves real problems for real users or businesses.

Beautiful code without users delivers no business value.

### Practical Consequences

- Product decisions take priority over technical elegance.
- Code quality supports delivery rather than replacing it.
- Refactoring should have measurable value.

### Anti-patterns

- Endless rewriting before the first release.
- Prioritizing architecture over validated product hypotheses.
- Optimizing code for imaginary future requirements.

---

## Principle 02 — Business Value Over Technical Beauty

### Statement

Engineering decisions should support business goals.

### Rationale

Technical excellence is important, but it is not the product.

The product exists to create value.

### Practical Consequences

- Prioritize features that validate business hypotheses.
- Accept reasonable technical compromises when justified.
- Balance quality with delivery speed.

### Anti-patterns

- Gold-plating.
- Solving technical problems nobody has.
- Building infrastructure without business need.

---

## Principle 03 — MVP First

### Statement

Deliver the smallest useful product capable of validating the main hypothesis.

### Rationale

Real users provide better feedback than assumptions.

### Practical Consequences

- Define MVP scope early.
- Defer non-essential functionality.
- Release sooner.
- Learn faster.

### Anti-patterns

- Feature creep.
- "One more feature before release."
- Trying to build version 5 before version 1 exists.

---

## Principle 04 — Validate Early

### Statement

Every important assumption should be validated as early as possible.

### Rationale

Incorrect assumptions become increasingly expensive over time.

### Practical Consequences

- Release prototypes.
- Gather user feedback.
- Test ideas before scaling.

### Anti-patterns

- Months of isolated development.
- Assuming user needs without evidence.

---

# Documentation Principles

---

## Principle 05 — Documentation First

### Statement

Documentation is created before implementation begins.

### Rationale

Clear thinking produces better software.

Writing documentation exposes missing decisions.

### Practical Consequences

- Product documentation precedes implementation.
- Architecture is documented before coding.
- Tasks are derived from documentation.

### Anti-patterns

- Code first.
- Documentation after release.
- Reverse engineering architecture from implementation.

---

## Principle 06 — Repository Is The Source Of Truth

### Statement

Knowledge belongs in the repository.

### Rationale

Chats are temporary.

Repositories are persistent.

### Practical Consequences

- Important decisions are documented.
- AI conversations are summarized.
- Product knowledge survives chat history.

### Anti-patterns

- "We discussed it somewhere in ChatGPT."
- Hidden knowledge.
- Critical decisions stored only in conversations.

---

## Principle 07 — Living Documentation

### Statement

Documentation evolves together with the product.

### Rationale

Outdated documentation is worse than missing documentation.

### Practical Consequences

- Documentation changes together with implementation.
- Reviews include documentation.
- Architecture stays synchronized.

### Anti-patterns

- Frozen documentation.
- Forgotten README files.
- Contradicting documents.

---

## Principle 08 — Decisions Must Be Traceable

### Statement

Important decisions should always have documented reasoning.

### Rationale

Future contributors should understand why a decision exists.

### Practical Consequences

- Record architectural decisions.
- Preserve migration rationale.
- Prefer explicit trade-offs.

### Anti-patterns

- Magic decisions.
- Unexplained rewrites.
- Lost context.

---

# AI Collaboration Principles

---

## Principle 09 — Human Owns The Product

### Statement

AI assists.

Humans decide.

### Rationale

Only humans own business goals, responsibility and vision.

### Practical Consequences

- AI proposes.
- Humans approve.
- Product direction remains human-owned.

### Anti-patterns

- Blindly accepting AI output.
- Delegating product strategy entirely to AI.

---

## Principle 10 — AI Has Roles, Not Authority

### Statement

AI systems perform clearly defined roles.

### Rationale

The workflow should not depend on a specific provider.

### Practical Consequences

Roles include:

- Strategic AI
- Implementation AI
- Review AI
- Research AI

Providers may change.

Roles remain stable.

### Anti-patterns

- Vendor lock-in.
- One AI doing everything.
- Mixing responsibilities.

---

## Principle 11 — Context Is A First-Class Asset

### Statement

High-quality context produces high-quality results.

### Rationale

AI performance depends primarily on context quality.

### Practical Consequences

- Preserve context.
- Organize documentation.
- Keep repositories understandable.

### Anti-patterns

- Starting every session from zero.
- Missing documentation.
- Context scattered across chats.

---

## Principle 12 — Independent Review Matters

### Statement

Important work should be reviewed independently.

### Rationale

Different AI systems detect different problems.

Independent reviews reduce blind spots.

### Practical Consequences

- Architecture reviews.
- Documentation reviews.
- Prompt reviews.
- Implementation reviews.

### Anti-patterns

- Reviewing your own work only.
- Assuming generated code is correct.

---

# Engineering Principles

---

## Principle 13 — Architecture Supports Delivery

### Statement

Architecture exists to help deliver products.

### Rationale

Architecture is a tool, not the goal.

### Practical Consequences

- Keep architecture proportional.
- Design for evolution.
- Avoid unnecessary complexity.

### Anti-patterns

- Architecture astronautics.
- Overengineering.
- Premature abstraction.

---

## Principle 14 — Small Safe Iterations

### Statement

Prefer many small improvements over massive rewrites.

### Rationale

Smaller changes reduce risk.

### Practical Consequences

- Incremental delivery.
- Frequent reviews.
- Continuous validation.

### Anti-patterns

- Big bang rewrites.
- Huge unreviewable changes.

---

## Principle 15 — Archive Instead Of Delete

### Statement

Historical knowledge has value.

### Rationale

Previous decisions often explain current architecture.

### Practical Consequences

- Archive legacy documentation.
- Mark deprecated artifacts.
- Preserve migration history.

### Anti-patterns

- Permanent deletion without history.
- Losing product evolution.

---

## Principle 16 — Technical Debt Is Managed

### Statement

Technical debt is neither good nor bad.

It is an engineering investment.

### Rationale

Sometimes debt accelerates delivery.

Sometimes it must be repaid.

### Practical Consequences

- Make debt visible.
- Accept intentional debt.
- Schedule repayment.

### Anti-patterns

- Ignoring debt.
- Eliminating all debt immediately.
- Hidden debt.

---

# Delivery Principles

---

## Principle 17 — Ship Early

### Statement

Real users are the best source of product feedback.

### Rationale

Software improves through usage.

### Practical Consequences

- Release early.
- Observe.
- Improve continuously.

### Anti-patterns

- Endless private development.
- Waiting for perfection.

---

## Principle 18 — Learn From Every Project

### Statement

Every completed project should improve the framework.

### Rationale

The framework evolves through practical experience.

### Practical Consequences

- Capture lessons learned.
- Improve templates.
- Improve prompts.
- Improve workflows.

### Anti-patterns

- Repeating identical mistakes.
- Ignoring retrospective knowledge.

---

## Principle 19 — Process Over Prompts

### Statement

A good workflow is more valuable than a perfect prompt.

### Rationale

Prompts evolve.

Processes endure.

### Practical Consequences

- Build repeatable workflows.
- Standardize collaboration.
- Improve methodology continuously.

### Anti-patterns

- Collecting prompts without process.
- Treating prompts as documentation.

---

## Principle 20 — Knowledge Over Conversations

### Statement

Knowledge should live in the repository, not inside AI conversations.

### Rationale

Chat history is temporary.

Repository knowledge is reusable.

### Practical Consequences

- Summarize important discussions.
- Document conclusions.
- Preserve project memory.

### Anti-patterns

- "The answer is somewhere in an old chat."
- Knowledge loss after context resets.

---

# Final Principle

The framework itself is a living product.

Every real project should improve the framework.

Every improvement to the framework should help future projects become faster, clearer and more successful.