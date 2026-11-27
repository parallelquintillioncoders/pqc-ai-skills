# PQC AI Skills

**Reusable Agent Skills by Parallel Quintillion Coders (PQC).** Use them for product discovery, project estimation, client quotations, and software development agreements across supported AI coding agents.

[Browse all skills](https://github.com/parallelquintillioncoders/pqc-ai-skills/tree/main/.agents/skills) · [PQC Website](https://parallelquintillioncoders.com/)

---

## Choose the skill you need

| Skill | Use it for | Documentation |
|---|---|---|
| **Product Discovery & Blueprint Architect** | New product ideas or existing products; outputs tables for modules/screens plus Mermaid navigation and architecture flowcharts | [Read guide](.agents/skills/product-discovery-blueprint-architect/README.md) |
| **Software Project Estimation Auditor** | Estimate an existing project or a client-defined scope | [Read guide](.agents/skills/software-project-estimation-auditor/README.md) |
| **Client Estimation & Payment Quotation** | Send a concise estimate with price, timeline, payment terms, and prerequisites | [Read guide](.agents/skills/client-estimation-payment-quotation/README.md) |
| **Client Proposal & Legal Agreement Generator** | Prepare a formal proposal, SOW, and draft development agreement | [Read guide](.agents/skills/client-proposal-legal-agreement-generator/README.md) |\n| **Practical Software Engineering Standards** | Apply relevant coding principles, architecture, file-size guidance, testing, and security without overengineering | [Read guide](.agents/skills/practical-software-engineering-standards/README.md) |

Each skill has a separate README with its purpose, install commands, update commands, and example prompt. The Product Discovery blueprint is table-first and includes screen inventories, navigation matrices, and Mermaid flow diagrams. Use Practical Software Engineering Standards alongside it to define only the engineering rules relevant to the project.

## Which project types are supported?

- **New product idea:** Start with Product Discovery & Blueprint Architect. It can help turn a rough idea into a researched product blueprint.
- **Existing project / defined scope:** Use Software Project Estimation Auditor, then choose the client quotation or formal agreement skill.

The three estimation/documentation skills do not invent a complete new product from zero. They expect an existing product or an already-defined scope.

## Recommended workflows

### New product

~~~text
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
Client estimate OR formal proposal/agreement
~~~

### Existing project

~~~text
Existing app / website / repository / PRD / client brief
        |
        v
Software Project Estimation Auditor
        |
        v
Client Estimation & Payment Quotation
        OR
Client Proposal & Legal Agreement Generator
~~~

---

## Works across supported AI agents

These are standard `SKILL.md` Agent Skills, not Antigravity-only instructions. The [Skills CLI](https://github.com/vercel-labs/skills) installs them into the correct folder for the agent you select.

Popular supported agents include:

| Agent | CLI agent ID |
|---|---|
| Claude Code | `claude-code` |
| Codex | `codex` |
| Cursor | `cursor` |
| Google Antigravity | `antigravity` |
| Gemini CLI | `gemini-cli` |
| GitHub Copilot | `github-copilot` |
| Cline | `cline` |

The Skills CLI supports additional agents. See the [official full supported-agent list](https://github.com/vercel-labs/skills/blob/main/docs/agents.md) for current IDs and installation paths.

### Install one skill in a project

Run from the project root. Replace `<skill-name>` and `<agent-id>` with the desired values.

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill <skill-name> --agent <agent-id>
~~~

Example:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent claude-code
~~~

### Install one skill globally

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill <skill-name> --agent <agent-id> --global
~~~

### Install one skill into multiple agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill <skill-name> --agent claude-code codex cursor antigravity
~~~

### Install all PQC skills for the selected agent

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent <agent-id>
~~~

For every supported agent, use:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill '*' --agent '*'
~~~

Add `--global` to install globally rather than into the current project.

---

## Update installed skills

The Skills CLI updates skills that were previously installed/tracked by the CLI. You do not need to run `skills add` again for an already-installed skill.

### Update all project-installed skills

Run from the project root where skills were installed:

~~~bash
npx skills update -p
~~~

### Update all globally installed skills

~~~bash
npx skills update -g
~~~

### Update one skill

Project installation:

~~~bash
npx skills update <skill-name> -p
~~~

Global installation:

~~~bash
npx skills update <skill-name> -g
~~~

### Check updates and list skills

~~~bash
npx skills check
npx skills list
npx skills list -g
~~~

If you manually copied skill folders instead of using the CLI, update them by downloading the latest repository version and replacing the copied folders.

---

## Use a skill

After installing, ask your selected AI agent to use the skill by its name. Example:

~~~text
Use product-discovery-blueprint-architect.

Review this product idea or existing project:
[Describe the product or provide the project context]

Research the relevant market. Define objectives, modules, features,
screens, user roles, journeys, navigation flowcharts, and architecture.
Compare open-source/self-hosted options first, hosted free tiers second,
and paid services third. Put all clarification questions together at the end.
~~~

For detailed examples, prerequisites, and skill-specific commands, open the individual documentation linked at the top of this README.

## Repository structure

~~~text
pqc-ai-skills/
├── README.md
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
~~~

## Important notes

- Basic Agent Skills are broadly portable, but support for tools, browsing, file access, and advanced features differs by agent. Check the selected agent's documentation.
- Product and market research needs web-browsing access in the selected agent.
- Verify API pricing, free-tier limits, licenses, and vendor terms before choosing a technology.
- Legal agreement output is a draft and should be reviewed by qualified counsel in the relevant jurisdiction.
- Never publish client-confidential files, credentials, API keys, bank details, or private project information in this public repository.

## References

- [Skills CLI and installation](https://github.com/vercel-labs/skills)
- [Official supported agents and paths](https://github.com/vercel-labs/skills/blob/main/docs/agents.md)
- [Skills.sh directory](https://skills.sh/)
- [Agent Skills specification](https://agentskills.io/)
- [PQC Website](https://parallelquintillioncoders.com/)
