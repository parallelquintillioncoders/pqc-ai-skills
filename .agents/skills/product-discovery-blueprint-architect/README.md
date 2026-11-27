# Product Discovery & Blueprint Architect

Turn a rough software idea or an existing product into a researched product blueprint that both a non-technical stakeholder and a development team can understand.

[← Back to PQC AI Skills](../../../../README.md) · [Open SKILL.md](./SKILL.md)

## When to use this skill

Use this skill in either mode:

- **New product:** You have an idea, but need to define the product, target users, market, modules, screens, and technology.
- **Existing product:** You have an application, website, repository, PRD, SRS, design, or current requirements and want to understand gaps or plan improvements.

Unlike the estimation and client-document skills, this skill can start with a rough idea. It does not start implementation; it creates the product blueprint.

## What it produces

1. Product objective, audience, user problems, and success criteria.
2. Local, global, or multi-market competitor research based on the product's actual target market.
3. Core modules, features, priorities, roles, and business rules.
4. Screen inventory with purpose, actions, and destinations.
5. User journeys and screen-to-screen navigation tables.
6. Mermaid navigation and architecture diagrams.
7. Technical service/API comparisons in this order:
   - Open-source and self-hosted options.
   - Hosted services with a verified free tier.
   - Paid/managed services when justified.
8. Recommended technology stack with trade-offs.
9. MVP and later-phase roadmap, dependencies, assumptions, and risks.
10. One consolidated list of decision questions at the end.

## Free-first technical research

For each capability (for example calling, messaging, payments, maps, file storage, notifications, or authentication), the skill compares relevant libraries, SDKs, APIs, and infrastructure.

It must check documentation, license, hosting needs, free quotas, trial expiry, overage fees, production limits, regional availability, security, maintenance effort, and paid pricing. "Open source" does not mean zero hosting or operating cost, and a temporary trial must not be presented as a permanent free tier.

## How to install in Antigravity

Install from the root of the project where you want the skill to be available.

**Project installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent antigravity
```

**Global installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent antigravity --global
```

## How to update

**Update project installation**

Run from the project root:

```bash
npx skills update product-discovery-blueprint-architect -p
```

**Update global installation**

```bash
npx skills update product-discovery-blueprint-architect -g
```

## Example prompt

```text
Use product-discovery-blueprint-architect.

I want to create/improve this product:
[Describe the idea or provide the existing project/repository]

Understand the business goal and target users. Research the product
market according to its actual target geography. Identify competitors,
modules, features, roles, screens, journeys, and navigation flowcharts.

For every technical service, compare open-source/self-hosted first,
hosted free tiers second, and paid options third. Verify documentation,
licensing, free limits, pricing, and operational costs.

Use simple language. Inspect the available files/code first if this is
an existing product. Collect all decision-changing questions and put
them together at the end with a recommended default for each.
```

## What to provide

For better results, share whatever is available:
- A plain-language idea or client brief.
- Existing website/app/repository URL or local project files.
- PRD, SRS, user stories, screen designs, screenshots, or API docs.
- Target users, business goals, countries/markets, and constraints.

Do not share passwords, secret keys, production credentials, or private customer data.

## Important

- Research depends on the AI agent having web-browsing access.
- Market geography follows the product's audience, not automatically the developer's location.
- The blueprint is provisional until material questions and assumptions are confirmed.
- This skill recommends and documents a solution; it does not create cloud resources, register vendor accounts, or start coding unless separately requested.
