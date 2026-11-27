# Software Project Estimation Auditor

Audit an existing software project or a client-defined scope before preparing a quotation.

[← Back to PQC AI Skills](../../../../README.md) · [Open SKILL.md](./SKILL.md)

## When to use this skill

Use this skill when you already have one or more of the following:
- An existing app, website, backend, or software repository.
- A client PRD, SRS, requirements document, feature list, or approved scope.
- UI/UX designs, user stories, API documentation, or database structure.
- An existing project that needs enhancements, new modules, integrations, migration, or a revised estimate.

**This is not a scratch-project ideation skill.** For a brand-new idea with no defined scope, use [Product Discovery & Blueprint Architect](../product-discovery-blueprint-architect/README.md) first and prepare an agreed product scope.

## What it produces

1. Confirmed, assumed, unknown, and recommended scope.
2. Module, feature, workflow, and dependency audit.
3. Missing requirements and gap register with severity and impact.
4. Technical skill and team-role matrix.
5. Work Breakdown Structure with optimistic, most-likely, pessimistic, and PERT hours.
6. Effort totals by task, role, and phase.
7. Delivery schedule, milestones, dependencies, and critical path.
8. Current market-rate research for relevant roles, geography, and engagement model.
9. Internal cost, contingency, pricing scenarios, profit, and margin calculations.
10. Client responsibilities, prerequisites, assumptions, exclusions, and risks.

## How to install in Antigravity

Run from the root of the project where you want the skill to be available.

**Project installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity
```

**Global installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent antigravity --global
```

## How to update

**Update project installation**

```bash
npx skills update software-project-estimation-auditor -p
```

**Update global installation**

```bash
npx skills update software-project-estimation-auditor -g
```

## Example prompt

```text
Use software-project-estimation-auditor.

Inspect this existing project, its repository, and available requirements.
Audit every requested module and workflow. Identify missing requirements,
technical skills, integrations, backend/data work, QA, deployment, and
handover tasks.

Estimate effort by role using low / likely / high scenarios. Build a
dependency-aware schedule. Research current market rates for the relevant
roles and project geography, cite sources, and calculate project costs.

Do not invent requirements, rates, or citations. Clearly separate confirmed
scope, assumptions, recommendations, and unanswered questions.
```

## What to provide

- Repository or project files, if available.
- PRD/SRS, user stories, designs, or feature list.
- Team, deadline, currency, and target geography if known.
- Existing rate cards or target margin, if you want them used.

## Important

- This skill is intended for existing projects or already-defined scope.
- Live rate research requires web-browsing access. If unavailable, the skill must say rates were not verified.
- Employee salary data, freelancer rates, and agency billing rates must not be treated as interchangeable.
- Internal cost and margin calculations are not automatically included in the client-facing quotation.
