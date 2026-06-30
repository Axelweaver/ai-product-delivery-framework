

# AI Product Delivery Framework

A practical framework for transforming software ideas and existing repositories into real products with the help of AI agents.

This repository is not a prompt collection only.

It is a product delivery system for people who want to move faster from idea to MVP, from MVP to release, and from release to real business value.

---

## Purpose

Modern AI tools can write code, review repositories, generate documentation, analyze product ideas and help with delivery.

But without a clear process, AI-assisted development quickly becomes chaotic:

- prompts are scattered across chats;
- documentation becomes inconsistent;
- architecture decisions are forgotten;
- AI agents work from outdated context;
- legacy repositories become harder to control;
- MVP delivery slows down instead of accelerating.

This framework defines a repeatable way to work with AI agents while keeping the human owner in control of product direction, business priorities and final decisions.

---

## Core Idea

The framework is based on one principle:

> Build products, not just code.

Good code matters, but business value matters more.

The goal is not to create a perfect codebase before release.

The goal is to:

- validate product hypotheses quickly;
- deliver useful MVPs faster;
- keep enough architecture and documentation to avoid chaos;
- make AI agents productive instead of random;
- preserve project knowledge outside chat history;
- support long-term product evolution after the first release.

---

## Who This Is For

This framework is for:

- solo developers building products;
- indie founders;
- technical founders;
- team leads;
- small software teams;
- developers moving from employment toward entrepreneurship;
- people using AI agents seriously, not casually.

It is especially useful when one person must act as:

- product owner;
- analyst;
- architect;
- engineering lead;
- developer;
- QA coordinator;
- release manager.

---

## Choose Your Scenario

Start with the scenario that matches your current situation.

---

### Scenario 1 — New Product From Scratch

Use this when:

- you have an idea;
- there is no repository yet;
- there is no product documentation yet;
- you want to start correctly from the beginning.

Start here:

```text
playbooks/greenfield/README.md
```

Typical flow:

1. Create repository structure.
2. Choose AI roles and tools.
3. Run Product Discovery.
4. Generate Product Documentation.
5. Create Architecture Documentation.
6. Create Epic and Task Backlog.
7. Start MVP implementation with an Implementation AI agent.

Primary prompts:

```text
templates/prompts/001_GREENFIELD_DISCOVERY_PROMPT.md
templates/prompts/004_PRODUCT_DOCUMENTATION_PROMPT.md
templates/prompts/006_TASK_DECOMPOSITION_PROMPT.md
```

---

### Scenario 2 — Existing Repository Without AI Workflow

Use this when:

- a repository already exists;
- the project was created manually or traditionally;
- AI agents were not part of the process;
- documentation may be incomplete, outdated or missing;
- you want to bring the project under this framework.

Start here:

```text
playbooks/legacy/README.md
```

Typical flow:

1. Make sure the repository is committed and safe.
2. Run Repository Audit.
3. Run Documentation Audit.
4. Identify legacy, active and missing documentation.
5. Create a migration plan.
6. Archive obsolete documentation.
7. Create or rewrite Product Documentation.
8. Create or rewrite Architecture Documentation.
9. Rebuild the task backlog.
10. Continue implementation using the new workflow.

Primary prompts:

```text
templates/prompts/002_LEGACY_REPOSITORY_AUDIT_PROMPT.md
templates/prompts/005_ARCHITECTURE_REVIEW_PROMPT.md
```

---

### Scenario 3 — Existing AI-Assisted Project Without This Framework

Use this when:

- the project already exists;
- AI tools were already used;
- important decisions may be hidden in chat history;
- different AI agents may have produced inconsistent documentation or code;
- prompts, rules and context are not centralized;
- you want to stabilize the project and continue safely.

Start here:

```text
playbooks/ai-assisted-legacy/README.md
```

Typical flow:

1. Collect existing repository documentation.
2. Export or summarize important AI chat history where possible.
3. Ask a Strategic AI to reconstruct product intent.
4. Ask an Implementation AI to audit the repository.
5. Compare repository state against reconstructed product direction.
6. Create a migration strategy.
7. Save important knowledge into repository documentation.
8. Archive outdated or conflicting files.
9. Rebuild agent rules and task structure.
10. Continue delivery through controlled AI-agent workflow.

Primary prompts:

```text
templates/prompts/003_AI_ASSISTED_LEGACY_AUDIT_PROMPT.md
templates/prompts/005_ARCHITECTURE_REVIEW_PROMPT.md
templates/prompts/008_REVIEW_AGENT_PROMPT.md
```

---

## AI Roles

This framework is provider-independent.

It does not require a specific AI product.

Instead, it defines roles.

Different providers can be used for the same role.

| Role | Responsibility | Possible Tools |
|---|---|---|
| Strategic AI | Product discovery, vision, planning, architecture, critique | ChatGPT, Claude, Gemini, Grok, local LLM |
| Implementation AI | Coding, refactoring, tests, validation, Git operations | Claude Code, Codex CLI, Cursor Agent, Aider, Cline |
| Review AI | Independent review, audits, risk detection, consistency checks | ChatGPT, Claude, Gemini, Grok, local LLM |
| Research AI | Web research, market research, technology comparison | Web-enabled AI, browser tools, research assistants |

The exact tools may change.

The roles should remain stable.

---

## Human Role

The human owner is not replaced by AI.

The human owner is responsible for:

- business goals;
- product direction;
- market understanding;
- prioritization;
- final architectural decisions;
- release decisions;
- monetization strategy;
- accepting or rejecting AI recommendations.

AI agents can accelerate work.

They must not silently take ownership of the product.

---

## Recommended Bootstrap Command

Use this command when creating a new framework-based repository manually.

Run it from the directory where the new repository should be created.

```zsh
mkdir -p my-product/{docs/{product,architecture,design,tasks,reviews,reports,archive/legacy},assets,scripts,tools,src,.claude,.github/workflows}

cd my-product || exit

git init

touch \
README.md \
CHANGELOG.md \
LICENSE \
.gitignore \
.editorconfig \
.gitattributes \
CLAUDE.md \
.claude/project-context.md \
docs/README.md \
docs/product/README.md \
docs/architecture/README.md \
docs/design/README.md \
docs/tasks/README.md \
docs/tasks/TASK_EXECUTION_PROTOCOL.md \
docs/reviews/README.md \
docs/reports/README.md \
docs/archive/legacy/README.md

cat > .gitignore <<'EOF'
.DS_Store
.idea/
.vscode/
*.log
EOF

cat > .editorconfig <<'EOF'
root = true

[*]
charset = utf-8
end_of_line = lf
insert_final_newline = true
trim_trailing_whitespace = true

[*.md]
trim_trailing_whitespace = false
EOF

cat > .gitattributes <<'EOF'
* text=auto eol=lf
EOF

git add .
git commit -m "Initial project structure"
```

---

## What To Upload Into An AI Project

When creating a project workspace in ChatGPT, Claude, Gemini or another provider, upload only the files that help the AI understand the current stage.

For a new project, upload:

```text
templates/agents/STRATEGIC_AI_RULES.md
templates/prompts/001_GREENFIELD_DISCOVERY_PROMPT.md
templates/product/
```

For an existing repository, upload:

```text
README.md
docs/
templates/prompts/002_LEGACY_REPOSITORY_AUDIT_PROMPT.md
templates/prompts/005_ARCHITECTURE_REVIEW_PROMPT.md
```

For an existing AI-assisted project, upload:

```text
README.md
docs/
existing AI rules
important exported chat summaries
templates/prompts/003_AI_ASSISTED_LEGACY_AUDIT_PROMPT.md
templates/prompts/008_REVIEW_AGENT_PROMPT.md
```

For implementation agents, provide:

```text
CLAUDE.md
PROJECT_CONTEXT.md
TASK_EXECUTION_PROTOCOL.md
current task file
related product and architecture documents
```

---

## Repository Structure

```text
ai-product-delivery-framework/
├── README.md
├── CHANGELOG.md
├── LICENSE
├── .gitignore
├── .editorconfig
├── .gitattributes
│
├── docs/
│   ├── 001_FRAMEWORK_VISION.md
│   ├── 002_CORE_PRINCIPLES.md
│   ├── 003_AI_AGENT_ROLES.md
│   ├── 004_HUMAN_ROLE.md
│   ├── 005_PRODUCT_DISCOVERY.md
│   ├── 006_DELIVERY_WORKFLOW.md
│   ├── 007_MVP_FIRST.md
│   ├── 008_LEGACY_MIGRATION.md
│   ├── 009_AI_ASSISTED_MIGRATION.md
│   ├── 010_MONETIZATION_AND_BUSINESS.md
│   └── 011_PROMPT_LIBRARY.md
│
├── playbooks/
│   ├── greenfield/
│   ├── legacy/
│   └── ai-assisted-legacy/
│
├── templates/
│   ├── repository/
│   ├── product/
│   ├── architecture/
│   ├── tasks/
│   ├── agents/
│   └── prompts/
│
├── examples/
└── tools/
```

---

## Documentation Language

Default language for framework documentation is English.

Project-owner-facing reports and reviews may be written in the project owner's preferred language.

Generated templates may define their own communication rules.

---

## MVP First

The framework prioritizes MVP delivery.

It intentionally avoids endless architecture work before release.

The correct balance is:

- enough product discovery to avoid building the wrong thing;
- enough documentation to preserve decisions;
- enough architecture to avoid chaos;
- enough testing to avoid obvious breakage;
- fast delivery to real users;
- feedback-driven improvement after release.

---

## What This Framework Is Not

This framework is not:

- a replacement for product thinking;
- a replacement for engineering judgment;
- a promise of perfect code;
- a rigid enterprise methodology;
- a universal answer for every team.

It is a practical operating model for AI-assisted product delivery.

---

## Current Status

Status: Early Draft

This framework is being developed from real project experience.

It is expected to evolve as more products are built, migrated and released using this workflow.

---

## License

License is not finalized yet.