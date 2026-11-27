# PQC AI Skills

**A collection of reusable AI skills by Parallel Quintillion Coders (PQC) for product discovery, software estimation, client quotations, and development agreements.**

[View all skills](https://github.com/parallelquintillioncoders/pqc-ai-skills/tree/main/.agents/skills) · [PQC Website](https://parallelquintillioncoders.com/)

---

## Choose a skill

Each skill has its own README with its purpose, workflow, installation commands, update commands, and example prompts. Open the guide for the skill you need.

| Skill | Use it for | Documentation |
|---|---|---|
| **Product Discovery & Blueprint Architect** | Start from a new product idea or analyse an existing product. Research the market, define modules, screens, navigation, technical options, and roadmap. | [Read installation & usage guide](.agents/skills/product-discovery-blueprint-architect/README.md) |
| **Software Project Estimation Auditor** | Audit an existing project or client-defined scope. Find gaps, map required skills, estimate effort and timeline, research market rates, and calculate costs. | [Read installation & usage guide](.agents/skills/software-project-estimation-auditor/README.md) |
| **Client Estimation & Payment Quotation** | Prepare a short client-facing estimate with the recipient, scope, module-wise price, timeline, payment terms, prerequisites, and notes. | [Read installation & usage guide](.agents/skills/client-estimation-payment-quotation/README.md) |
| **Client Proposal & Legal Agreement Generator** | Prepare a formal client proposal, SOW, payment schedule, and draft software development services agreement. | [Read installation & usage guide](.agents/skills/client-proposal-legal-agreement-generator/README.md) |

---

## Which workflow should I follow?

### New product idea

```text
Rough idea or business problem
          |
          v
Product Discovery & Blueprint Architect
          |
          v
Confirm and approve the product scope
          |
          v
Software Project Estimation Auditor
          |
          v
Client Estimation OR Formal Proposal & Agreement
```

### Existing product or client-defined scope

```text
Existing app / website / codebase / PRD / client brief
          |
          v
Software Project Estimation Auditor
          |
          v
Client Estimation OR Formal Proposal & Agreement
```

## Important scope distinction

- **Product Discovery & Blueprint Architect** supports both new ideas and existing products.
- **Software Project Estimation Auditor**, **Client Estimation & Payment Quotation**, and **Client Proposal & Legal Agreement Generator** are intended for existing projects or a scope that has already been defined. They do not invent a complete new product from zero.

## Quick installation — Google Antigravity

Install one skill from the root of the project where you want it available. Replace the skill name with one of the four names below.

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill <skill-name> --agent antigravity
```

Install all four in the current project:

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity
```

Install all four globally:

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity --global
```

## Quick update commands

Update all project-installed skills (run from the project root):

```bash
npx skills update -p
```

Update all globally installed skills:

```bash
npx skills update -g
```

For an individual skill's install/update commands, open that skill's README from the table above.

> These update commands apply to skills tracked by the Skills CLI. If you manually copied a skill folder, download the latest version from this repository and replace the copied folder.

## Repository structure

```text
pqc-ai-skills/
├── README.md                         # Main index and quick start
└── .agents/
    └── skills/
        ├── product-discovery-blueprint-architect/
        │   ├── SKILL.md
        │   └── README.md
        ├── software-project-estimation-auditor/
        │   ├── SKILL.md
        │   └── README.md
        ├── client-estimation-payment-quotation/
        │   ├── SKILL.md
        │   └── README.md
        └── client-proposal-legal-agreement-generator/
            ├── SKILL.md
            └── README.md
```

## General notes

- Live product/market/rate research requires web-browsing access in the AI agent.
- Verify API pricing, free-tier limits, licenses, and vendor terms before committing to a technology.
- Legal agreement output is a draft and should be reviewed by qualified counsel in the relevant jurisdiction.
- Never publish client-confidential files, credentials, API keys, access tokens, bank details, or private customer information in this public repository.

---

**Maintained by [Parallel Quintillion Coders (PQC)](https://parallelquintillioncoders.com/).**
