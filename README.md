# PQC AI Skills

Reusable Antigravity agent skills for software project estimation, financial costing, client quotations, and development agreements.

**Repository:** https://github.com/parallelquintillioncoders/pqc-ai-skills



## Intended use: existing projects, not scratch-project creation

**These skills are designed to review and estimate an existing client project or an already-defined project scope. They are not intended to invent, design, or plan a completely new project from zero.**

Use them when you already have one or more of the following:
- An existing application, website, backend, or software product/repository.
- A client-provided PRD, SRS, requirement document, feature list, or scope brief.
- Existing screens, UI/UX designs, user stories, API documentation, or database structure.
- An existing project that needs new modules, enhancements, integrations, migration, or a revised estimate.

The skills should inspect the available project material, understand what has already been built or specified, identify missing modules and gaps, and estimate only the agreed/current scope plus clearly labelled recommendations.

**Do not ask these skills to create a new product idea or invent an entire application's requirements from scratch.** For a greenfield project with no defined scope, first complete product discovery and prepare an approved PRD/feature scope. Then use these skills to audit and estimate that defined scope.

## Available skills

| Skill | Use it for | What it generates |
|---|---|---|
| `software-project-estimation-auditor` | Internal project analysis before quoting | Module audit, missing gaps, technical skill matrix, effort by role, timeline, researched market rates, cost and quote range |
| `client-estimation-payment-quotation` | Sending a simple estimate to a client | Recipient details, project scope, module-wise price, delivery timeline, total amount, advance and milestone payment terms |
| `client-proposal-legal-agreement-generator` | Formal client proposal and agreement | Client proposal, SOW, detailed payment plan, software development service agreement, legal/commercial clauses and signature blocks |

## Repository structure

```text
pqc-ai-skills/
├── README.md
└── .agents/
    └── skills/
        ├── software-project-estimation-auditor/
        │   └── SKILL.md
        ├── client-estimation-payment-quotation/
        │   └── SKILL.md
        └── client-proposal-legal-agreement-generator/
            └── SKILL.md
```

## Requirements

- Node.js and npm/npx for CLI installation.
- Google Antigravity installed.
- Internet access to download the public repository.
- For market-rate research, the estimation skill needs an agent/tool with web browsing access.

## Install in Antigravity — choose one skill

Run these commands in the terminal. They install the selected skill into the **current project workspace**. Run the command from the root directory of the project where you want Antigravity to use the skill.

### 1. Software Project Estimation Auditor

Use this first on an existing project, codebase, or client-defined scope to inspect what exists/is specified, identify missing modules, estimate time and effort, research current developer/agency rates, and calculate project costs. It is not a from-zero product ideation skill.

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity
```

### 2. Client Estimation & Payment Quotation

Use this for an existing project or an already-defined client scope when you only need a short client-facing estimate. It includes who the estimate is prepared for, PQC as the developer/service provider, existing/current scope, module-wise pricing, timeline, total amount, and payment milestones. It does **not** create a full legal agreement or invent a new project from scratch.

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity
```

### 3. Client Proposal & Legal Agreement Generator

Use this for an existing project or an already-defined/approved scope when the client needs a formal proposal, SOW, and software development services agreement with commercial/legal terms and signatures.

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity
```

## Install all three skills together

Run this from your project root if you want every PQC skill available in that project:

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity
```

## Install globally for all Antigravity projects

Use the `--global` flag to install a skill for your user account instead of only the current project. Run one command per skill:

```bash
# 1. Internal project estimation and cost audit
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity --global

# 2. Simple client estimate and payment quotation
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity --global

# 3. Detailed client proposal and legal agreement
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity --global
```

To install all three globally in one command:

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity --global
```

## Manual installation (Windows)

If you prefer not to use the CLI:

1. Clone or download this repository.
2. Copy the skill folders from `.agents\skills\` into your Antigravity workspace's `.agents\skills\` folder.

For global installation, copy the three skill folders into:

```text
%USERPROFILE%\.gemini\antigravity\skills\
```

Example PowerShell commands, when run from the cloned repository folder:

```powershell
$destination = "$env:USERPROFILE\.gemini\antigravity\skills"
New-Item -ItemType Directory -Force $destination | Out-Null
Copy-Item ".\.agents\skills\*" $destination -Recurse -Force
```

After installation, restart or refresh Antigravity and check the Agent Customizations / Skills area. If a newly installed skill is not listed, confirm that its folder contains a `SKILL.md` file and that the folder name matches the skill name.

## How to use each skill

Ask Antigravity to use the skill by name. You can also refer to the skill explicitly in your prompt.

### Estimate a project internally

```text
Use software-project-estimation-auditor.

Inspect the existing project's PRD, current implementation, and repository. Audit every existing and requested module and workflow,
identify missing requirements and technical skills, estimate hours by role,
build a dependency-aware delivery schedule, research current market rates
for the relevant countries, and produce low/likely/high cost scenarios.

Do not invent requirements or rates. Cite current rate sources.
```

### Send only a quotation to the client

```text
Use client-estimation-payment-quotation.

Review the existing project materials and prepare a concise estimate addressed to the correct client.
Use only the current/defined project scope; do not invent a new project.
Include project modules, deliverables, timeline, total price,
and advance/milestone payment terms.

PQC is the development company and service provider.
The client is the customer and pays PQC.
Do not generate a full legal agreement.
```

### Prepare a formal proposal and agreement

```text
Use client-proposal-legal-agreement-generator.

Review the existing project scope and convert the approved estimate into a client-ready proposal, SOW,
payment schedule, and software development services agreement.
Identify PQC as the service provider and the customer as the client.
Include advance payment, milestone invoices, scope changes, acceptance,
IP, warranty, maintenance exclusions, cancellation, confidentiality,
liability, and dispute terms. Use placeholders for unknown legal details.
```

## Update installed skills

To refresh installed skills from the repository:

```bash
npx skills update
```

For command options and supported agents, see the [Skills CLI documentation](https://www.skills.sh/docs/cli) and [Skills CLI repository](https://github.com/vercel-labs/skills).

## Important notes

- The estimation auditor can only live-check market rates when the selected AI agent has web-browsing access. It must not invent rates or citations.
- The client quotation skill is intentionally short and is not a legal agreement.
- The proposal/agreement skill creates a draft. Have jurisdiction-specific clauses reviewed by a qualified lawyer before signing.
- PQC's public-facing brand/contact details do not by themselves prove the registered legal contracting entity. Confirm the legal entity, tax details, and signatory before issuing formal contracts or tax invoices.
- Never commit client-confidential data, credentials, API keys, bank details, or private project information to this public repository.
