---
Title: Framework MVP Review
Type: Review
Version: 0.1
Author: Claude Code (claude-sonnet-4-6)
Date: 2026-06-30
Time: 20:36 CEST
Branch: main
Repository Revision: dbce4ebb3ae6a19c870df8869f4b328a1d6ebd27
Related Epic:
Status: Final
---

# Framework MVP Review — Version 0.1

---

## Executive Summary

The AI Product Delivery Framework has a strong conceptual foundation. Its 11 core documents (docs/001 through docs/011) are well-written, internally consistent, and represent a genuine contribution to the discipline of AI-assisted product delivery. The framework philosophy — human ownership, repository as memory, roles over providers, MVP first — is sound and practically motivated.

However, the framework currently exists almost entirely as theory. Every practical artifact — all playbooks, all templates, all prompts, all agent rules, all examples, all tools — is an empty file. A developer discovering this repository through GitHub would read a compelling README that promises immediate practical value, follow the "Start here" link to a playbook, and find a blank page.

**Current state in one sentence:** The framework has a well-built roof but no walls or floor.

The framework is not yet ready for adoption by someone other than its creator. It can be recommended as a reference source of methodology today, but not as an actionable toolkit. The critical path to practical usability requires filling the template layer — specifically: CLAUDE.md, TASK_EXECUTION_PROTOCOL.md, IMPLEMENTATION_AI_RULES.md, and one complete working playbook.

**Overall grade: 6/10** — strong philosophy, insufficient implementation artifacts.

---

## Current State

### Repository Inventory

| Directory | Files | Content Status |
|-----------|-------|---------------|
| `docs/` | 11 | Complete — all documents written |
| `playbooks/greenfield/` | 1 | Empty |
| `playbooks/legacy/` | 1 | Empty |
| `playbooks/ai-assisted-legacy/` | 1 | Empty |
| `templates/agents/` | 4 | All empty |
| `templates/repository/` | 3 | All empty |
| `templates/product/` | 5 | All empty |
| `templates/architecture/` | 3 | All empty |
| `templates/tasks/` | 2 | All empty |
| `templates/prompts/` | 8 | All empty |
| `examples/` | 1 | Empty |
| `tools/` | 1 | Empty |
| `CHANGELOG.md` | 1 | Empty |

Of the 41 non-gitignore, non-git files in the repository, 30 are empty placeholders (73%).

### Git History

7 commits. All work was completed on a single day (2026-06-30 based on document dates). The entire theoretical layer was committed in sequence, leaving the practical layer unpopulated.

### Documentation Coverage

The 11 core documents cover the full framework lifecycle:

| Document | Topic | Quality |
|----------|-------|---------|
| 001 | Framework Vision | Strong |
| 002 | Core Principles | Strong |
| 003 | AI Agent Roles | Strong |
| 004 | Human Role | Strong |
| 005 | Product Discovery | Strong |
| 006 | Delivery Workflow | Strong |
| 007 | MVP First | Strong |
| 008 | Legacy Migration | Strong |
| 009 | AI-Assisted Migration | Strong |
| 010 | Monetization and Business | Good |
| 011 | Prompt Library | Good |

---

## Repository Review

### Structure

The top-level structure is logical and well-organized:

```
docs/           ← framework theory
playbooks/      ← scenario-specific guides  
templates/      ← reusable artifacts
examples/       ← real project illustrations
tools/          ← utilities
```

This structure scales well and separates concerns appropriately. The `docs/` layer for framework theory, `templates/` for reusable artifacts, and `playbooks/` for step-by-step guides is a sensible three-layer model.

**Missing:** `docs/` has no `README.md` index. A user navigating into the directory encounters 11 numbered files with no orientation document.

**Missing:** `templates/` has no root-level `README.md` explaining which templates to use and in what order.

**Minor issue:** The bootstrap shell command in `README.md` creates the directory structure correctly but does not copy any template content into the created files. It creates empty files, which is what exists in the repository itself. The command is useful for structure but gives a false impression that the templates are ready.

### Scalability

The flat `docs/001...011` numbering works for the current size but will become unwieldy at 20+ documents. A subdirectory structure (e.g., `docs/principles/`, `docs/workflow/`, `docs/migration/`) would be more scalable but would require migration. This is not urgent now.

### Discoverability

The README is excellent for initial orientation. The three-scenario model ("Choose Your Scenario") is one of the strongest design decisions in the repository. A new user can immediately identify their situation and find a starting path.

The problem is that all three starting paths lead to empty files.

### Separation of Concerns

The conceptual separation between framework theory (`docs/`), reusable templates (`templates/`), and working examples (`examples/`) is clean and correct. The issue is not the architecture of the separation — it is that only the first layer has been populated.

---

## Documentation Review

### Strengths

**Principle structure (002):** Each of the 20 principles follows the same format: Statement → Rationale → Practical Consequences → Anti-patterns. This structure is highly readable and makes the principles actionable rather than abstract.

**Three-scenario model:** The framework correctly identifies the three most common entry points (greenfield, legacy, AI-assisted legacy) and maps workflows to each. This is a practical and accurate classification.

**Agent role lifecycle (003):** The role lifecycle chart (Strategic → Research → Documentation → Architecture → Planning → Implementation → Review → QA → Release) is comprehensive and gives the framework genuine architectural depth.

**Belgrade Metro as live example:** Grounding the theory in a real project is valuable. The specific examples in 008 (legacy migration) and 009 (AI-assisted migration) make the abstract concepts concrete.

**"Minimum Validated Product" concept (007):** Extending the MVP concept with the idea of validation evidence is a meaningful addition. The framework correctly identifies that shipping is not the goal — learning is.

**"AI Legacy" concept (009):** Naming the problem of knowledge fragmentation caused by AI tooling is original and important. This is a real problem that hasn't been well-articulated elsewhere.

**Delivery Anti-patterns (006):** The list of anti-patterns is practically motivated. "Perfect Architecture Before MVP," "Knowledge Trapped In Chat," and "AI Scope Expansion" reflect real patterns from real projects.

### Weaknesses

**No docs/ README:** There is no index document for the docs/ directory. A user browsing GitHub will see a list of 11 files with no navigation aid.

**All documents dated the same day:** Every document shows "Last Updated: 2026-06-30." While accurate, this creates an impression that the framework was written in a single theoretical burst rather than evolved through practice. This is currently true, and the framework should acknowledge it more explicitly.

**Framework status understated:** The README says "Status: Early Draft" which is honest but doesn't fully communicate that all practical artifacts are empty. A clearer statement would be: "Theory: Complete / Templates: In Progress / Examples: Planned."

**Missing CONTRIBUTING.md:** There are no contribution guidelines. The framework claims it should evolve through practical experience (Principle 18), but there is no process for contributions.

**Missing framework CHANGELOG:** `CHANGELOG.md` exists but is empty. A framework that preaches documentation discipline should practice it.

### Inconsistencies

**Prompt naming mismatch (011 vs. templates/prompts/):** Document 011 suggests a naming convention:
```
001_PROJECT_INITIALIZATION_PROMPT.md
003_PRODUCT_DISCOVERY_PROMPT.md
004_ARCHITECTURE_REVIEW_PROMPT.md
```
But the actual files in `templates/prompts/` use different names:
```
001_GREENFIELD_DISCOVERY_PROMPT.md
004_PRODUCT_DOCUMENTATION_PROMPT.md
```
This is a minor inconsistency today but will create confusion once templates are populated.

**Agent roles mismatch (003 vs. templates/agents/):** Document 003 defines 8 AI roles (Strategic, Research, Documentation, Architecture, Planning, Implementation, Review, QA, Release). But `templates/agents/` contains only 4 files (IMPLEMENTATION_AI_RULES.md, STRATEGIC_AI_RULES.md, REVIEW_AI_RULES.md, RESEARCH_AI_RULES.md). The other 5 roles have no corresponding template. Even if some roles are intentionally combined (e.g., Documentation AI may use Strategic AI rules), this should be explicitly stated.

**Subdirectory structure suggested but not created (011):** Document 011 recommends:
```
templates/prompts/
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
But the actual `templates/prompts/` uses flat numbered files. The suggested structure is better for long-term scalability but was not implemented.

**"Product Decisions" mentioned but no template:** Document 003 mentions "ADR/PDR records" as a Documentation AI output. The Belgrade Metro project already uses PDR files (`docs/product/pdr/`). But the framework templates contain no PDR or ADR template.

### Broken or Missing References

All references from docs to templates/prompts point to empty files. This is systematic, not a case-by-case issue.

`docs/006_DELIVERY_WORKFLOW.md` references `templates/tasks/EPIC_README.md` and `templates/tasks/TASK_TEMPLATE.md` — both empty.

---

## Framework Review

### Framework Completeness Assessment

#### Scenario 1 — Starting a New Project

| Step | Covered by Theory | Practical Artifact Exists |
|------|------------------|--------------------------|
| Create repository structure | Yes (README bootstrap command) | Partial (command creates structure, no templates) |
| Choose AI roles | Yes (003) | No (agent rules are empty) |
| Run Product Discovery | Yes (005) | No (001_GREENFIELD_DISCOVERY_PROMPT.md is empty) |
| Generate Product Documentation | Yes (005, 006) | No (product templates are empty) |
| Create Architecture Documentation | Yes (006) | No (architecture templates are empty) |
| Create Task Backlog | Yes (006) | No (TASK_TEMPLATE.md is empty) |
| Start MVP Implementation | Yes (007) | No (CLAUDE.md template is empty) |

**Verdict:** Not actionable without significant effort from the adopter.

#### Scenario 2 — Existing Repository

| Step | Covered by Theory | Practical Artifact Exists |
|------|------------------|--------------------------|
| Run Repository Audit | Yes (008) | No (prompt is empty) |
| Run Documentation Audit | Yes (008) | No |
| Create Migration Plan | Yes (008) | No |
| Archive Legacy Docs | Yes (008) | Partially (archive path defined, no README template) |
| Rebuild Task Backlog | Yes (008) | No |

**Verdict:** Methodology is excellent; actionable only if the user reads 008 and implements the 10-step process manually.

#### Scenario 3 — AI-Assisted Legacy

| Step | Covered by Theory | Practical Artifact Exists |
|------|------------------|--------------------------|
| Collect documentation | Yes (009) | No |
| Reconstruct product intent | Yes (009) | No |
| Audit repository | Yes (009) | No (003_AI_ASSISTED_LEGACY_AUDIT_PROMPT.md is empty) |
| Compare against product direction | Yes (009) | No |
| Create migration strategy | Yes (009) | No |

**Verdict:** Same as above — strong methodology, no executable starting point.

### Framework Philosophy Consistency

The framework's stated philosophy (20 principles in 002) is well-reflected in the documents.

**Strong alignment:**
- "Process Over Prompts" (Principle 19) is practiced — the framework builds workflow before prompts.
- "Repository Is The Source Of Truth" (Principle 06) is practiced in the framework's own design.
- "Archive Instead Of Delete" (Principle 15) is explicitly modeled in the repository structure.
- "Human Owns The Product" (Principle 09) is consistently reinforced across all 11 documents.

**Slight tension:**
- "Ship Early" (Principle 17) and "Validate Early" (Principle 04) are core principles — but the framework itself was not shipped with working examples before the theory was complete. The framework preaches MVP-first but was itself built theory-first.
- "Living Documentation" (Principle 07) implies documentation evolves with the product. All documents share the same date, suggesting they were written at once rather than evolved through iteration. This is not wrong — it is early days — but the principle and practice are not yet aligned.

### Where Theory Is Stronger Than Practice

The following sections have strong theoretical development but no practical counterpart:

1. **Prompt Library (011):** A full theory of prompt engineering, lifecycle, quality criteria, metadata requirements, and maintenance — but zero prompts.

2. **Agent Rules:** Detailed description of 8+ roles with responsibilities, context requirements, and anti-patterns — but empty rule files.

3. **Context Handover (003):** A precise specification of what a "Minimum Handover Package" should contain — but no handover template.

4. **Review Reports (006):** Clear requirements for review report format, location, and metadata — but no review report template (only the format implied by this review's own structure).

5. **Checkpoints (006):** Checkpoints are described as important project artifacts — but no checkpoint template exists.

---

## AI Workflow Review

### Role Model

The role-based model (Strategic AI, Implementation AI, Review AI, Research AI, plus Documentation, Architecture, Planning, QA, Release) is the strongest architectural decision in the framework. It solves the provider lock-in problem elegantly: roles are stable, providers are interchangeable.

The practical consequence — that the same Claude instance can act as Strategic AI in one session and Implementation AI in another — is correct and important.

### Context Management

The framework correctly identifies context quality as the primary determinant of AI output quality. Principle 11 ("Context Is A First-Class Asset") and the Context Package definition in 006 reflect real-world observation.

The recommendation to use repository files rather than conversation history as context is particularly valuable for long-running projects.

**Missing piece:** There is no concrete guidance on *how much* context to provide. Providing too much context can reduce AI performance (dilution, context window limits). Providing too little leads to guessing. The framework would benefit from a "context budget" section — what to always include, what to include for specific roles, what to never include.

### Prompt Strategy

The Prompt Library theory (011) is well-developed. The categorization by purpose rather than provider is correct. The principle that prompts should evolve through practical use before joining the library is sound.

**Critical gap:** The actual prompts that should validate these theories are empty. Without at least one complete, worked example of a prompt (ideally the greenfield discovery prompt), the entire prompt theory chapter is purely academic.

### Repository-First Approach

The repository-first approach is one of the framework's strongest ideas and is consistently applied throughout the documents. The AI session handover protocol (009) correctly identifies that sessions should end by writing knowledge back to the repository.

**Missing:** An explicit AI Session Handover template. Sessions in real projects produce context summaries, but no structured format is defined.

### Review Workflow

The review workflow is well-defined: Review AI operates independently, produces reports, saves them to `docs/reviews/`, does not silently fix issues, and escalates to the human owner.

This workflow is sound. The Belgrade Metro project already practices it (the current review document is an example). The gap is that `REVIEW_AI_RULES.md` is empty, so a new project adopting the framework has no starting point.

### Multi-Agent Collaboration

The framework correctly identifies multi-agent collaboration as a first-class scenario. Document 009 has a dedicated section. The principle that knowledge belongs to the repository rather than to any individual AI is the correct foundation.

**Not addressed:** What happens when two AI agents produce contradictory outputs? The Human Role document (004) covers this briefly ("Resolving AI Disagreements") but doesn't specify how contradictions should be documented and resolved in the repository.

### Knowledge Preservation

The framework's approach to knowledge preservation is one of its most valuable contributions. The concept that chat history is temporary while repository documentation is permanent, and that every session should leave the repository in a better state, is actionable and important.

---

## Strengths

### 1. Role-Based, Provider-Independent Architecture

Separating AI roles from AI providers is the framework's most important architectural decision. As AI tools evolve rapidly, a workflow that depends on ChatGPT or Claude Code specifically would require constant updates. A workflow based on roles (Strategic, Implementation, Review) remains stable.

### 2. Three-Scenario Entry Model

Greenfield / Legacy / AI-Assisted Legacy covers the realistic starting points for most projects. The classification is accurate and the different entry workflows are correctly differentiated.

### 3. Human Ownership as First Principle

The consistent, explicit insistence that humans own product direction is counterintuitive in an AI framework but important. Document 004 (Human Role) is one of the strongest documents in the repository.

### 4. "AI Legacy" Concept

Naming and defining the problem of knowledge fragmentation caused by AI tool usage is a genuine contribution. This is a real problem that doesn't have standard terminology yet.

### 5. Discovery Pipeline Depth

Document 005 contains one of the most complete Product Discovery specifications available, including the discovery-for-different-project-types distinction and the "Definition Of Ready For Architecture" gate.

### 6. Archive-Instead-Of-Delete

Principle 15 and its practical implementation in the migration documents reflects lessons from real projects. The structured archive path (`docs/archive/legacy/`) with explanation requirements is practical and important.

### 7. Business-Grounded Philosophy

Document 010 (Monetization and Business) integrates business thinking into what is usually a purely technical framework. Connecting product delivery to validated business value and founder-level thinking differentiates this from generic engineering methodologies.

### 8. Bootstrap Shell Command

The `README.md` bootstrap command that creates a complete repository skeleton is immediately practical. It reflects real-world usage and reduces the friction of starting a new project.

### 9. Belgrade Metro as Living Validation

Having a real project mentioned throughout the framework — and being actively used to validate it — is a significant credibility advantage over purely theoretical frameworks.

### 10. Anti-Pattern Sections

Every major document includes an anti-patterns section. These are practically grounded and prevent common mistakes that abstract principles alone would not prevent.

---

## Weaknesses

### 1. Empty Template Layer (Critical)

The most serious weakness. 30 of 41 framework files are empty. The template layer — the primary practical value of a framework — contains no content. A user following the documented workflow will encounter empty files at every actionable step.

**Impact:** High. Blocks practical adoption.

### 2. Playbooks Are Empty (Critical)

The three playbooks are the primary entry points described in the README. All three are empty. A user directed to `playbooks/greenfield/README.md` finds a blank page. This creates immediate trust erosion.

**Impact:** High. First impression failure.

### 3. No docs/ Index (Medium)

There is no `docs/README.md`. Users browsing the docs/ directory on GitHub see 11 numbered files with no navigation, reading order, or summary.

**Impact:** Medium. Reduces discoverability.

### 4. Theory-Practice Gap Acknowledged But Not Bridged (Medium)

The framework documents extensively discuss the importance of practical validation, evolving through real use, and shipping early. But the framework itself was shipped in a theory-only state. This is an acceptable early state, but the gap should be explicitly acknowledged in the README with a roadmap.

**Impact:** Medium. Reduces credibility.

### 5. Agent Role Count Mismatch (Medium)

003 defines 9 roles but `templates/agents/` has 4 files. No explanation is provided for why 5 roles have no corresponding template. Even if the intention is to merge them, this should be documented.

**Impact:** Medium. Creates confusion about which roles require rule files.

### 6. No Context Budget Guidance (Medium)

The framework emphasizes context quality but provides no guidance on context quantity. Context window limits are a real constraint that determines what files to include in an AI session. This is missing from the practical workflow.

**Impact:** Medium. Users will either over-provide or under-provide context.

### 7. No Contribution Process (Low-Medium)

The framework states it should evolve through practical experience (Principle 18) but provides no mechanism for contributing lessons back. No CONTRIBUTING.md, no issue template, no PR guidelines.

**Impact:** Low now, medium as the framework matures.

### 8. Prompt Subdirectory Structure Not Implemented (Low)

011 recommends a subdirectory structure for prompts (`project/`, `discovery/`, etc.) but the actual `templates/prompts/` uses flat numbered files. The recommended structure is better but wasn't built.

**Impact:** Low. Only matters when prompts are populated.

### 9. Empty CHANGELOG (Low)

The CHANGELOG.md exists but is empty. The framework that advocates for documentation discipline should practice it.

**Impact:** Low. Minor credibility issue.

---

## Risks

### Risk 1 — First Impression Failure

**Description:** A developer discovering this repository on GitHub follows the README to a playbook and finds an empty file. Trust is immediately damaged, and they may dismiss the framework before reading the core documents.

**Probability:** High (given current state).

**Mitigation:** Populate at least one playbook fully before any public promotion. Alternatively, add an explicit "Work In Progress" notice to all empty files explaining that content is coming.

### Risk 2 — Theory Without Validation

**Description:** All 11 core documents were written in a single day based primarily on Belgrade Metro experience. This is a small sample of one project type (mobile app, Flutter, solo developer). The framework's applicability to web apps, teams, legacy enterprise systems, or multi-platform products has not been validated.

**Probability:** Medium. The principles are general enough to be applicable, but edge cases may reveal gaps.

**Mitigation:** Explicitly acknowledge scope. Add a "Validated For" section to the README describing which project types have been tested.

### Risk 3 — Prompt Drift

**Description:** The prompt naming convention described in 011 conflicts with the file names in `templates/prompts/`. When the empty prompt files are eventually populated, there is risk that the naming standard changes but 011 is not updated, creating permanent documentation-to-implementation drift.

**Probability:** Medium.

**Mitigation:** Decide on one naming convention and update 011 to match it before populating any prompts.

### Risk 4 — Framework Becoming Academic

**Description:** A framework with strong theory and weak practical artifacts risks becoming an academic reference rather than a working tool. If the template layer is not populated during real project work, the theory may evolve in ways disconnected from practical constraints.

**Probability:** Medium. The Belgrade Metro project is actively using the framework, which partially mitigates this risk.

**Mitigation:** Prioritize filling templates based on immediate Belgrade Metro needs.

### Risk 5 — Agent Rules Divergence

**Description:** The actual CLAUDE.md in Belgrade Metro has become significantly more detailed than what is documented in the framework. If the template CLAUDE.md is never populated from real experience, the framework and real project practice will diverge.

**Probability:** High (already partially happening).

**Mitigation:** Extract and generalize the Belgrade Metro CLAUDE.md into the framework template after the epic 005 milestone.

---

## Missing Concepts

### 1. Context Budget Framework

The framework discusses context quality extensively but never addresses context quantity. With AI tools having context window limits, practitioners need guidance on:

- What is always required in context (CLAUDE.md, current task, related product docs).
- What is role-dependent (architecture docs for Implementation AI, competitor analysis for Research AI).
- What should not be included (full test suites, complete codebases, historical reports).

### 2. AI Session Handover Template

Document 006 describes what a handover should contain. Document 009 discusses handover as part of AI migration. But there is no structured template that an AI agent can actually fill in at the end of a session.

### 3. ADR / PDR Templates

Document 003 mentions "ADR/PDR records" as Documentation AI outputs. The Belgrade Metro project has already created `docs/product/pdr/`. The framework should include templates for both Architecture Decision Records and Product Decision Records.

### 4. Repository Health Checklist

A simple checklist for evaluating whether a repository is framework-compliant:
- Does a CLAUDE.md exist?
- Does a TASK_EXECUTION_PROTOCOL.md exist?
- Is docs/product/ complete?
- Are legacy documents archived?
- Do reviews live in docs/reviews/?

### 5. Testing Strategy Guidance

The delivery workflow describes a testing stage but provides no guidance on what to test, how to balance unit/integration/manual testing, or what level of test coverage is appropriate for an MVP versus a mature product.

### 6. Release Checklist Template

"Release AI" is defined as a role. A release checklist template would be the most practical artifact that role could produce.

### 7. Framework Evolution Protocol

The framework states that every project should improve the framework (Principle 18). But there is no defined process for how a project improvement becomes a framework improvement. No contribution flow, no validation criteria, no versioning plan.

### 8. Error Handling for AI Failures

What happens when an AI agent produces incorrect output? The Review AI role partially addresses this, but the framework has no explicit guidance on what to do when AI output is wrong, contradictory, or harmful to the project.

### 9. Team Adaptation Guide

The framework is clearly designed for solo developers and small teams. A section addressing how the framework adapts to larger teams (distributed roles, PR-based review, multiple implementation agents) would increase its applicability.

### 10. Framework Versioning Strategy

The framework should version itself. When templates change, when principles are updated, or when new concepts are introduced, downstream projects should be able to understand what changed and whether they need to update their implementations.

---

## Recommendations

### Priority 1 — Fill the Three Critical Templates

Before any other work, the following three files must be populated. They are the minimum required to make the framework actionable:

**`templates/repository/CLAUDE.md`** — This is the single most important template. Every Implementation AI session in a framework-based project starts by reading CLAUDE.md. Without a working template, Implementation AI adoption is impossible. Extract and generalize from Belgrade Metro.

**`templates/repository/TASK_EXECUTION_PROTOCOL.md`** — The second most important file for Implementation AI. Extract and generalize from Belgrade Metro.

**`templates/agents/IMPLEMENTATION_AI_RULES.md`** — The rules that govern what an Implementation AI agent should and should not do. These are the constraints that make AI-assisted development safe and predictable.

### Priority 2 — Complete One Full Playbook

`playbooks/greenfield/README.md` should be the first playbook to receive complete content. It is the simplest scenario and the most likely starting point for new adopters. A complete greenfield playbook demonstrates the full workflow from idea to first commit.

### Priority 3 — Add docs/ README

Create `docs/README.md` with:
- Purpose of the docs/ directory.
- Recommended reading order for new adopters.
- Brief description of each document.
- Link to the active templates.

### Priority 4 — Populate at Least One Prompt

`templates/prompts/001_GREENFIELD_DISCOVERY_PROMPT.md` should be the first prompt to receive real content. It is referenced in the README as the starting point for new projects. Populate it based on the prompts actually used for Belgrade Metro discovery.

### Priority 5 — Resolve Naming Inconsistencies

Before populating more content:
- Align the prompt naming convention between 011 and the actual files in `templates/prompts/`.
- Clarify which agent rules files exist for which roles (4 vs. 9 roles).

### Priority 6 — Update README Status

Add a "Framework Completion Status" section to the README with a table:

| Layer | Status |
|-------|--------|
| Framework Theory (docs/) | Complete — Draft |
| Playbooks | Planned |
| Repository Templates | In Progress |
| Product Templates | Planned |
| Architecture Templates | Planned |
| Agent Rules | Planned |
| Prompt Library | Planned |
| Examples | Planned |

This sets honest expectations for first-time visitors.

### Priority 7 — Write CONTRIBUTING.md

Document how practical experience from real projects should flow back into the framework. The "Learn From Every Project" principle (18) needs a mechanism.

### Priority 8 — Add Context Budget Section

Add a "Context Budget" section to document 006 (Delivery Workflow) or create a dedicated short document covering the context quantity question: what to always include, what to include per role, what to exclude.

---

## Proposed Roadmap

### Phase 1 — Minimum Viable Framework (Weeks 1–2)

Goal: Make the framework actionable for a new adopter without requiring manual extraction from theory documents.

- [ ] Populate `templates/repository/CLAUDE.md` from Belgrade Metro experience.
- [ ] Populate `templates/repository/TASK_EXECUTION_PROTOCOL.md` from Belgrade Metro experience.
- [ ] Populate `templates/repository/PROJECT_CONTEXT.md`.
- [ ] Populate `templates/agents/IMPLEMENTATION_AI_RULES.md`.
- [ ] Complete `playbooks/greenfield/README.md` as one working playbook.
- [ ] Add `docs/README.md` index.
- [ ] Resolve prompt naming inconsistency.
- [ ] Write `CHANGELOG.md` initial entry.

### Phase 2 — Core Prompt Library (Weeks 3–4)

Goal: Provide at least one working prompt for each major workflow stage.

- [ ] Populate `templates/prompts/001_GREENFIELD_DISCOVERY_PROMPT.md`.
- [ ] Populate `templates/prompts/007_IMPLEMENTATION_AGENT_PROMPT.md`.
- [ ] Populate `templates/prompts/008_REVIEW_AGENT_PROMPT.md`.
- [ ] Populate `templates/prompts/002_LEGACY_REPOSITORY_AUDIT_PROMPT.md`.
- [ ] Populate `templates/tasks/TASK_TEMPLATE.md`.
- [ ] Populate `templates/tasks/EPIC_README.md`.

### Phase 3 — Product and Architecture Templates (Weeks 5–6)

Goal: Give framework adopters a ready-to-use documentation skeleton.

- [ ] Populate `templates/product/001_PRODUCT_VISION.md` through `005_PRODUCT_ROADMAP.md`.
- [ ] Populate `templates/architecture/001_ARCHITECTURE_OVERVIEW.md` through `003_DATA_MODEL.md`.
- [ ] Create ADR and PDR templates.
- [ ] Create `templates/repository/REVIEW_REPORT_TEMPLATE.md`.
- [ ] Create `templates/repository/CHECKPOINT_TEMPLATE.md`.

### Phase 4 — Examples and Validation (Weeks 7–8)

Goal: Validate the framework against a second real project and extract lessons.

- [ ] Add Belgrade Metro as a documented example in `examples/`.
- [ ] Complete the remaining two playbooks (`legacy/`, `ai-assisted-legacy/`).
- [ ] Add CONTRIBUTING.md.
- [ ] Add framework versioning strategy.
- [ ] Run the framework against a second project type (not mobile, not solo).

### Phase 5 — Framework Maturity (Ongoing)

- Continuous improvement based on real project feedback.
- Add team adaptation guide.
- Add context budget guidance.
- Validate prompts against multiple AI providers.
- Create onboarding guide for new team members.

---

## Ordered Action Plan

The following actions are ordered by priority. Each action has a clear owner (human or AI role) and expected output.

| Priority | Action | Owner | Output |
|----------|--------|-------|--------|
| 1 | Populate CLAUDE.md template from Belgrade Metro | Human + Documentation AI | Working CLAUDE.md template |
| 2 | Populate TASK_EXECUTION_PROTOCOL.md | Human + Documentation AI | Working protocol template |
| 3 | Populate IMPLEMENTATION_AI_RULES.md | Human + Documentation AI | Agent rules file |
| 4 | Complete greenfield playbook | Human + Strategic AI | First working playbook |
| 5 | Create docs/README.md | Documentation AI | Navigation index |
| 6 | Fix prompt naming (011 vs. actual files) | Human decision + Documentation AI | Naming consistency |
| 7 | Populate first discovery prompt | Human + Documentation AI | Working prompt |
| 8 | Write CHANGELOG initial entry | Documentation AI | Active changelog |
| 9 | Write CONTRIBUTING.md | Human | Contribution process |
| 10 | Populate TASK_TEMPLATE.md and EPIC_README.md | Documentation AI | Task system templates |
| 11 | Create ADR + PDR templates | Documentation AI | Decision record templates |
| 12 | Complete product templates (5 files) | Documentation AI | Product documentation skeleton |
| 13 | Create AI Session Handover template | Documentation AI | Handover artifact |
| 14 | Add Belgrade Metro to examples/ | Human + Documentation AI | First working example |
| 15 | Complete legacy playbook | Human + Documentation AI | Second working playbook |

---

## Final Recommendation

The AI Product Delivery Framework has a strong theoretical foundation that is worth preserving and building on. The core documents (001–011) represent genuine intellectual work and reflect real experience from the Belgrade Metro project. The principles are sound, the three-scenario model is accurate, and the role-based AI architecture is the right approach.

However, the framework is not yet suitable for adoption by someone other than its creator.

The gap is not conceptual — it is practical. An engineer who discovers this repository today would find:

1. A compelling README with clear promises.
2. Eleven excellent theory documents.
3. Empty files at every actionable starting point.

This gap must be closed before the framework can be promoted or recommended.

The highest-leverage actions are:
1. Populate CLAUDE.md and TASK_EXECUTION_PROTOCOL.md — these unlock Implementation AI adoption.
2. Complete the greenfield playbook — this fulfills the README's primary promise.
3. Add docs/README.md — this makes the theory layer discoverable.

If these three actions are taken, the framework moves from "interesting reading material" to "actionable starting point." Everything else is valuable but secondary.

The framework's guiding principle — "Human direction, AI acceleration, product delivery" — is good. The framework should now apply that same principle to itself.

---

## Related Documents

- `README.md`
- `docs/001_FRAMEWORK_VISION.md`
- `docs/002_CORE_PRINCIPLES.md`
- `docs/003_AI_AGENT_ROLES.md`
- `docs/006_DELIVERY_WORKFLOW.md`
- `docs/008_LEGACY_MIGRATION.md`
- `docs/009_AI_ASSISTED_MIGRATION.md`
- `docs/011_PROMPT_LIBRARY.md`
