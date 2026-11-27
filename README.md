# PQC AI Skills

**Reusable AI skills for software project estimation, client quotations, and development agreements.**

[GitHub Repository](https://github.com/parallelquintillioncoders/pqc-ai-skills) · [Browse all skills](https://github.com/parallelquintillioncoders/pqc-ai-skills/tree/main/.agents/skills)

---

## Start here

These skills help **Parallel Quintillion Coders (PQC)** review an existing client project, estimate the work, and prepare commercial documents.

**They are intended for existing software projects or projects with an already-defined scope.** For example: an existing application, website, backend, repository, PRD, SRS, feature list, UI design, or client requirement document.

They are **not** intended to invent a brand-new product or create an entire project scope from scratch. For a new idea with no defined requirements, complete product discovery and prepare an agreed PRD/scope first.

### Choose the skill you need

| Skill | When to use it | Output |
|---|---|---|
| **[Software Project Estimation Auditor](.agents/skills/software-project-estimation-auditor/SKILL.md)** | Before quoting, to inspect an existing project or defined scope | Module audit, missing gaps, required skills, effort, timeline, market-rate research, internal cost and quote range |
| **[Client Estimation & Payment Quotation](.agents/skills/client-estimation-payment-quotation/SKILL.md)** | When you only need to send an estimate to a client | Client recipient, project scope, module-wise price, timeline, total amount, payment terms, client prerequisites and notes |
| **[Client Proposal & Legal Agreement Generator](.agents/skills/client-proposal-legal-agreement-generator/SKILL.md)** | When the client needs a formal proposal and agreement | Proposal, SOW, milestone schedule, draft software development agreement and signature blocks |

### Recommended workflow

```text
Existing project / client requirements
                |
                v
1. Software Project Estimation Auditor
   Audit scope, modules, gaps, skills, hours, rates and cost
                |
                v
2. Choose the client document
   A. Client Estimation & Payment Quotation
      (short estimate only)
   OR
   B. Client Proposal & Legal Agreement Generator
      (formal proposal and agreement)
                |
                v
Send to client
```

---

## Installation

### Before you begin

1. Install [Node.js](https://nodejs.org/) and npm. Use a current supported Node.js release.
2. Open the terminal in the **existing project folder** where you want to use the skills.
3. Run the command for the skill you need.

The commands below use the [Skills CLI](https://github.com/vercel-labs/skills) and target **Google Antigravity**.

### Option A — Install one skill in the current project

Project installation makes the skill available in that workspace. Run the command from the root of the project where you want to use it.

**1. Software Project Estimation Auditor**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity
```

**2. Client Estimation & Payment Quotation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity
```

**3. Client Proposal & Legal Agreement Generator**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity
```

### Option B — Install all three in the current project

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity
```

### Option C — Install one skill globally

Global installation makes the skill available across your Antigravity projects for your user account.

**1. Software Project Estimation Auditor**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity --global
```

**2. Client Estimation & Payment Quotation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity --global
```

**3. Client Proposal & Legal Agreement Generator**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity --global
```

### Option D — Install all three globally

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent antigravity --global
```

---

## Update installed skills

When PQC publishes changes to a skill, use the update command. **You do not need to run the install command again for skills already installed through the Skills CLI.**

Run the commands from any terminal location for global updates. For project updates, run them from the root of the project where the skills were installed.

### Update all project-installed skills

```bash
npx skills update -p
```

### Update all globally installed skills

```bash
npx skills update -g
```

### Update only one skill in the project

```bash
npx skills update client-estimation-payment-quotation -p
```

### Update only one globally installed skill

```bash
npx skills update client-estimation-payment-quotation -g
```

Replace `client-estimation-payment-quotation` with either of the other skill names to update that skill instead.

### Check for available updates

```bash
npx skills check
```

### List installed skills

```bash
# Project-installed skills
npx skills list

# Globally installed skills
npx skills list -g
```

**Important:** The update commands work for skills installed/tracked by the Skills CLI. If you installed skills by manually copying folders, update them by pulling/downloading the latest repository version and copying the updated skill folders again.

---

## Use the skills in Antigravity

After installation, restart or refresh Antigravity if the skills do not appear immediately. Open the Agent/Skills or Customizations area and confirm the installed skill is listed.

You can invoke a skill by name in your prompt.

### 1. Audit an existing project

```text
Use software-project-estimation-auditor.

Inspect this existing project, its repository and available
requirements. Audit the modules and workflows, identify missing
requirements and technical skills, estimate effort by role, build
a dependency-aware timeline, research current market rates, and
calculate low / likely / high costs.

Do not invent requirements or market rates. Cite current rate sources.
```

### 2. Send a simple estimate to the client

```text
Use client-estimation-payment-quotation.

Review the existing project and prepare a concise estimate addressed
to the correct client. Include project scope, modules, deliverables,
timeline, total price, advance/milestone payment terms, client-side
prerequisites and important notes.

PQC is the developer/service provider. The client is the customer
and pays PQC. Do not generate a full legal agreement.
```

### 3. Prepare a formal proposal and agreement

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
        ├── software-project-estimation-auditor/
        │   └── SKILL.md
        ├── client-estimation-payment-quotation/
        │   └── SKILL.md
        └── client-proposal-legal-agreement-generator/
            └── SKILL.md
```

## Important information

- The estimation auditor can research current market rates only when the AI agent has web-browsing access. It must not fabricate rates or citations.
- The client quotation skill creates a short estimate, not a full legal agreement.
- The proposal/agreement skill creates a draft for review. Have jurisdiction-specific terms checked by a qualified lawyer before signing.
- PQC's public-facing brand/contact details do not automatically establish its registered legal contracting entity. Confirm the legal entity, tax details and authorized signatory before issuing formal contracts or tax invoices.
- Never commit client-confidential information, passwords, API keys, access tokens, bank details or private project files to this public repository.

## Documentation and support

- [Skills CLI documentation](https://github.com/vercel-labs/skills)
- [Skills.sh](https://skills.sh/)
- [PQC website](https://parallelquintillioncoders.com/)
- [PQC AI Skills repository](https://github.com/parallelquintillioncoders/pqc-ai-skills)
