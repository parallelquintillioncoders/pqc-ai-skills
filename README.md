# PQC AI Skills

**A practical collection of AI skills for product discovery, software estimation, client quotations, and development agreements.**

[Browse all skills](https://github.com/parallelquintillioncoders/pqc-ai-skills/tree/main/.agents/skills) · [PQC Website](https://parallelquintillioncoders.com/)

---

## Start here

PQC AI Skills help turn software ideas and client requirements into structured product blueprints, realistic estimates, and client-ready documents.

There are **two kinds of work** in this collection:

- **Product discovery:** Can start from a rough new idea or analyse an existing product. It helps define what should be built.
- **Estimation and client documents:** Intended for existing software projects or a scope already defined by the client. They audit, price, and document the work; they do not invent a new product from zero.

## Choose the right skill

| Skill | Use it when | Main output |
|---|---|---|
| **[Product Discovery & Blueprint Architect](.agents/skills/product-discovery-blueprint-architect/SKILL.md)** | You have a rough idea for a new product OR an existing product that needs analysis | Product overview, market research, modules, features, screen list, user journeys, navigation flowcharts, free-first/paid-second technology options, architecture, roadmap, and consolidated questions |
| **[Software Project Estimation Auditor](.agents/skills/software-project-estimation-auditor/SKILL.md)** | You have an existing project, repository, PRD, or defined scope and need to estimate the work | Missing-gap audit, technical skills, task-level effort, schedule, live market-rate research, cost and quote range |
| **[Client Estimation & Payment Quotation](.agents/skills/client-estimation-payment-quotation/SKILL.md)** | You need to send a simple estimate to a client | Prepared-for details, scope, module-wise pricing, timeline, total amount, payment milestones, client-side prerequisites and notes |
| **[Client Proposal & Legal Agreement Generator](.agents/skills/client-proposal-legal-agreement-generator/SKILL.md)** | The client needs a formal proposal and development agreement | Client proposal, SOW, payment schedule, draft service agreement, commercial/legal terms and signature blocks |

## Recommended workflows

### A. From a new idea to a product blueprint

```text
Rough idea / business problem
          |
          v
Product Discovery & Blueprint Architect
          |
          +--> Market and competitor research
          +--> Product modules and features
          +--> Screens and user journeys
          +--> Navigation flowcharts
          +--> Free/open-source and free-tier options first
          +--> Paid alternatives where justified
          +--> Architecture, technology stack and roadmap
          +--> One consolidated list of questions at the end
          |
          v
Confirm decisions and approve the blueprint
          |
          v
Software Project Estimation Auditor
          |
          v
Client estimate OR formal proposal/agreement
```

### B. For an existing project or client-defined scope

```text
Existing app / website / repository / PRD / client brief
          |
          v
Software Project Estimation Auditor
          |
          v
Choose one:
  1. Client Estimation & Payment Quotation
  2. Client Proposal & Legal Agreement Generator
```

---

## Market research and technology choices

The Product Discovery skill selects research geography based on the actual product audience:

- **Local product:** Research the relevant city, region, or country.
- **Global product:** Research global competitors, usage patterns, providers, and regional differences.
- **Multi-market product:** Research each intended market and compare them.
- **Unclear target market:** State a provisional assumption and place the decision in the final consolidated question list.

For technical services, the research order is:

1. **Open-source / self-hosted:** Free software that you can operate on your own infrastructure. Hosting, bandwidth, maintenance, and engineering effort may still cost money.
2. **Hosted free tier:** A managed service with a verified free allowance. The skill checks quotas, trial expiry, overage fees, and restrictions.
3. **Paid / managed services:** Paid alternatives when free options do not meet reliability, scale, compliance, operations, or feature needs.

The skill must compare documentation, pricing, limits, licensing, security, hosting cost, vendor lock-in, and production suitability. It must not describe a trial as a permanent free plan.

---

## Installation in Google Antigravity

### Before you install

1. Install [Node.js](https://nodejs.org/) (npm/npx is included).
2. Open a terminal in the project folder where you want to use the skills.
3. Choose an individual skill or install the complete collection.

These commands use the [Skills CLI](https://github.com/vercel-labs/skills) and target Antigravity.

### Option A — Install one skill in the current project

Run the selected command from the root folder of the project where the skill should be available.

**1. Product Discovery & Blueprint Architect**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent antigravity
```

**2. Software Project Estimation Auditor**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity
```

**3. Client Estimation & Payment Quotation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity
```

**4. Client Proposal & Legal Agreement Generator**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity
```

### Option B — Install all four in the current project

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity
```

### Option C — Install one skill globally

Global installation makes the skill available across your Antigravity projects for your user account.

**1. Product Discovery & Blueprint Architect**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent antigravity --global
```

**2. Software Project Estimation Auditor**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity --global
```

**3. Client Estimation & Payment Quotation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity --global
```

**4. Client Proposal & Legal Agreement Generator**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity --global
```

### Option D — Install all four globally

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity --global
```

---

## Update installed skills

When PQC publishes changes, update the skills already installed through the Skills CLI. **You do not need to run the installation command again for an already-installed skill.**

### Update all project-installed skills

Run this from the project root where the skills were installed:

```bash
npx skills update -p
```

### Update all globally installed skills

```bash
npx skills update -g
```

### Update one skill in a project

```bash
npx skills update product-discovery-blueprint-architect -p
```

### Update one globally installed skill

```bash
npx skills update product-discovery-blueprint-architect -g
```

Replace `product-discovery-blueprint-architect` with another skill name to update a different skill.

### Check and list skills

```bash
# Check for updates
npx skills check

# List project-installed skills
npx skills list

# List globally installed skills
npx skills list -g
```

**Manual installation note:** The update commands apply to skills tracked by the Skills CLI. If you manually copied folders, download/pull the latest repository version and copy the updated skill folders again.

---

## Use the skills in Antigravity

After installation, open Antigravity and check the Agent / Skills or Customizations area. Restart or refresh Antigravity if a newly installed skill does not appear.

Ask Antigravity to use the skill by its exact name.

### 1. Discover or blueprint a product

Use for a rough new idea or an existing product.

```text
Use product-discovery-blueprint-architect.

I want to create/improve this product:
[Describe the idea or existing product]

Research the target market based on the actual product audience.
Define the product goal, users, modules, features, screens,
user roles, user journeys and navigation flowcharts.

Research technical APIs and libraries free/open-source first,
then hosted free tiers, then paid alternatives. Show actual limits,
pricing, documentation and trade-offs.

Use plain language. Identify requirement gaps and assumptions.
Do the research first and put all decision questions together
at the end with recommended defaults.
```

### 2. Audit and estimate an existing project

Use when the project already has requirements, code, designs, or a defined scope.

```text
Use software-project-estimation-auditor.

Inspect this existing project, its repository and available
requirements. Audit modules and workflows, identify missing
requirements and technical skills, estimate effort by role,
build a dependency-aware timeline, research current market rates,
and calculate low / likely / high cost scenarios.

Do not invent requirements or market rates. Cite current sources.
```

### 3. Send only an estimate to the client

```text
Use client-estimation-payment-quotation.

Review the existing project and prepare a concise estimate addressed
to the correct client. Include scope, modules, deliverables, timeline,
total price, advance/milestone payment terms, client-side prerequisites
and important notes.

PQC is the development company/service provider. The client is the
customer and pays PQC. Do not generate a full legal agreement.
```

### 4. Prepare a formal proposal and agreement

```text
Use client-proposal-legal-agreement-generator.

Use the approved scope and estimate to prepare a client-facing
proposal, SOW, payment schedule and draft software development
services agreement. PQC is the service provider; the customer is
the client. Do not invent missing legal or company information.
Use placeholders where details are unavailable.
```

---

## Repository structure

```text
pqc-ai-skills/
├── README.md
└── .agents/
    └── skills/
        ├── product-discovery-blueprint-architect/
        │   └── SKILL.md
        ├── software-project-estimation-auditor/
        │   └── SKILL.md
        ├── client-estimation-payment-quotation/
        │   └── SKILL.md
        └── client-proposal-legal-agreement-generator/
            └── SKILL.md
```

## Important notes

- Product Discovery performs web research only when the AI agent has browsing access. Current market facts, product features, API plans, pricing, and free-tier limits must be verified and linked.
- The Product Discovery skill can start from a rough new idea or analyse an existing product. The Estimation Auditor and client-document skills are for an existing project or an already-defined scope.
- The estimator must not fabricate market rates or citations.
- The client quotation skill creates a short estimate, not a full legal agreement.
- The proposal/agreement skill creates a draft. Have jurisdiction-specific terms reviewed by a qualified lawyer before signing.
- PQC's public-facing brand/contact details do not automatically establish its registered legal contracting entity. Confirm legal entity, tax details, and authorized signatory before issuing formal contracts or tax invoices.
- Never commit client-confidential information, passwords, API keys, access tokens, bank details, or private project files to this public repository.

## References

- [Skills CLI](https://github.com/vercel-labs/skills)
- [Skills.sh](https://skills.sh/)
- [Andrej Karpathy-style agent guidelines (community repository)](https://github.com/multica-ai/andrej-karpathy-skills)
- [PQC Website](https://parallelquintillioncoders.com/)
- [PQC AI Skills Repository](https://github.com/parallelquintillioncoders/pqc-ai-skills)
