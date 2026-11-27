# Product Discovery & Blueprint Architect

Turn a rough idea or an existing product into a researched product blueprint for both non-technical stakeholders and development teams.

[← Back to PQC AI Skills](../../../README.md) · [Open skill instructions (`SKILL.md`)](./SKILL.md)

## What it creates

- Product objective, target audience, user problems, and success measures.
- Competitor and market research based on the product's actual target geography (local, global, or multi-market).
- Prioritised modules, features, user roles, and business rules.
- Screen inventory with purpose, actions, and destinations.
- User journeys, navigation tables, and Mermaid flowcharts.
- Technical comparisons in this order: open-source/self-hosted, hosted free-tier, then paid/managed services.
- Recommended technology stack, architecture, dependencies, risks, and roadmap.
- A single consolidated set of clarification questions at the end.

## When to use it

Use for both:
- **New product:** you have an idea but need to define what to build.
- **Existing product:** you have a website, app, repository, requirements, designs, or current workflows and need a gap analysis or improved blueprint.

For technical services, it compares libraries, SDKs, APIs, and infrastructure. It verifies licensing, quotas, trial expiry, operating costs, pricing, availability, security, and documentation. Open-source software may still require paid hosting and maintenance.

---

## Install with the Skills CLI

These skills use the shared Agent Skills format. Install them through the Skills CLI into any supported coding agent. The CLI places the skill in the correct location for the selected agent.

### Popular supported agents

| Agent | Agent ID for the CLI |
|---|---|
| Claude Code | `claude-code` |
| Codex | `codex` |
| Cursor | `cursor` |
| Google Antigravity | `antigravity` |
| Gemini CLI | `gemini-cli` |
| GitHub Copilot | `github-copilot` |
| Cline | `cline` |

See the [complete, current supported-agent list](https://github.com/vercel-labs/skills/blob/main/docs/agents.md). Agent IDs and supported targets can change as the Skills CLI evolves.

### Install in the current project

Run from the root of the project where you want this skill available. Replace `<agent-id>` with one of the supported IDs above.

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent <agent-id>
~~~

Example for Claude Code:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent claude-code
~~~

### Install globally for your user account

This makes the skill available across projects for the selected agent.

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent <agent-id> --global
~~~

### Install for multiple agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent claude-code codex cursor antigravity
~~~

### Install for all supported agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill product-discovery-blueprint-architect --agent '*'
~~~

Add `--global` to the command for global installation.

---

## Update this skill

Update the project installation (run from the project root):

~~~bash
npx skills update product-discovery-blueprint-architect -p
~~~

Update the global installation:

~~~bash
npx skills update product-discovery-blueprint-architect -g
~~~

Update all installed project skills:

~~~bash
npx skills update -p
~~~

Update all globally installed skills:

~~~bash
npx skills update -g
~~~

Check for available updates:

~~~bash
npx skills check
~~~

List installed skills:

~~~bash
npx skills list
npx skills list -g
~~~

> The Skills CLI update command updates skills already tracked by that CLI. If you manually copied a skill folder, download the latest folder from this repository and replace the manual copy.

---

## Example prompt

~~~text
Use product-discovery-blueprint-architect.

I want to create or improve this product:
[Describe the idea or share the existing product/repository]

Research the actual target market. Define the objective, users,
modules, features, roles, screens, journeys, and navigation flowcharts.

Compare open-source/self-hosted options first, hosted free tiers second,
and paid alternatives third. Verify docs, licenses, quotas, operating
costs, and pricing. Use plain language and put all decision questions
together at the end with recommended defaults.
~~~

## Notes

- Web research, repository access, file reading, and diagram rendering depend on the capabilities of the selected agent and tools connected to it.
- The skill is written in agent-neutral format; some execution features may vary between agents.
- Never share secrets, access tokens, passwords, private customer data, or bank details in prompts or public repositories.
