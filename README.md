# PQC AI Skills

Reusable agent skills for software estimation and client-facing commercial documentation.

## Included skills

| Skill | Purpose |
|---|---|
| `software-project-estimation-auditor` | Audits scope, modules, missing requirements, technical skills, effort, schedule, current market rates, and project finances. |
| `client-proposal-legal-agreement-generator` | Converts an approved estimate into a client-facing proposal, SOW, payment plan, and draft software development agreement. |
| `client-estimation-payment-quotation` | Creates a concise client-facing estimate with recipient, module-wise pricing, delivery timeline, and payment milestones — without a full agreement. |

## Repository structure

```text
.agents/
  skills/
    software-project-estimation-auditor/
      SKILL.md
    client-proposal-legal-agreement-generator/
      SKILL.md
```

## Install in Antigravity

Clone the repository into a project workspace so Antigravity can discover the workspace skills:

```bash
git clone https://github.com/parallelquintillioncoders/pqc-ai-skills.git
```

Then use the skills folder in your workspace, or copy both skill directories into the workspace's existing `.agents/skills/` folder.

For global Windows installation, copy the two skill directories into:

```text
%USERPROFILE%\.gemini\config\skills\
```

Restart/refresh Antigravity and confirm the skills appear in Agent Customizations.

## Example prompts

**Estimate a project**

```text
Use software-project-estimation-auditor.
Inspect the PRD and repository. Audit every module and workflow,
identify missing requirements and skills, estimate hours by role,
build a dependency-aware schedule, research current market rates
for the relevant countries, and produce low/likely/high pricing.
Do not invent requirements or rates; cite live sources.
```

**Prepare a short estimate only**

```text
Use client-estimation-payment-quotation.
Prepare a concise client estimate addressed to the right customer.
Include the main modules, deliverables, delivery timeline, total price,
and 50/30/20 payment milestones unless different terms were agreed.
Do not generate a full agreement or lengthy legal clauses.
```

**Prepare a client pack**

```text
Use client-proposal-legal-agreement-generator.
Convert the approved estimate into a client-ready proposal, SOW,
payment schedule, and software services agreement. Include advance
payment, milestone invoices, scope changes, acceptance, IP, warranty,
maintenance exclusions, cancellation, confidentiality, liability,
and dispute terms. Use placeholders for unknown legal details.
```

## Important

These skills generate estimates and draft commercial/legal documents. Legal terms are proposals, not legal advice. Have jurisdiction-specific clauses reviewed by qualified counsel before signature. Never publish client-confidential data, secrets, or credentials in this repository.
