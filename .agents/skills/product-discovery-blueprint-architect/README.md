# Product Discovery & Blueprint Architect

Turn a rough idea or an existing product into a researched product blueprint for both non-technical stakeholders and development teams.

[← Back to PQC AI Skills](../../../README.md) · [Open skill instructions (`SKILL.md`)](./SKILL.md)

## What it creates

- Product objective, target audience, user problems, and success measures.
- Competitor and market research based on the product's actual target geography (local, global, or multi-market).
- Prioritised modules, features, user roles, and business rules.
- Table-first product deliverable: overview, users, market, modules/features, screens, permissions, APIs, integrations, roadmap, risks, and decisions.
- Screen inventory with stable screen IDs, entry points, actions, destinations, and role access.
- Navigation mapping tables plus mandatory Mermaid flowcharts for app navigation, core user journeys, complex modules, and system architecture.
- Technical comparisons in this order: open-source/self-hosted, hosted free-tier, then paid/managed services.
- Recommended technology stack, architecture, dependencies, risks, and roadmap.
- A single consolidated set of clarification questions at the end.

## When to use it

Use for both:
- **New product:** you have an idea but need to define what to build.
- **Existing product:** you have a website, app, repository, requirements, designs, or current workflows and need a gap analysis or improved blueprint.

For technical services, it compares libraries, SDKs, APIs, and infrastructure. It verifies licensing, quotas, trial expiry, operating costs, pricing, availability, security, and documentation. Open-source software may still require paid hosting and maintenance.

---



## Required deliverable format: tables + flow diagrams

The final product blueprint is **table-first and diagram-led**, not a long paragraph-based report.

It must include structured tables for:
- Product overview and target users.
- Market/competitor research.
- Module and feature breakdown.
- Screen inventory with unique screen IDs.
- Role and permission matrix.
- Screen-to-screen navigation mapping.
- Free/open-source, hosted free-tier, and paid API/library comparisons.
- Recommended technology stack.
- Integrations, prerequisites, and dependencies.
- Roadmap, risks, assumptions, and final decisions.

It must also include Mermaid flowcharts for:
1. Overall application navigation.
2. The main user journey.
3. Complex module workflows.
4. System architecture and external-service integrations.

**Every screen must appear in the screen inventory and navigation mapping.** The names and IDs in the tables must match the diagrams. If the selected AI agent cannot render a diagram preview, it must still provide valid Mermaid source in a fenced code block.

Example screen table:

| Screen ID | Module | Screen name | Main action | Next screen |
|---|---|---|---|---|
| AUTH-01 | Authentication | Login | Enter phone/email | AUTH-02 |
| AUTH-02 | Authentication | Verification | Confirm OTP/code | HOME-01 |
| HOME-01 | Home | Main dashboard | Open messages | CHAT-01 |

Example navigation flow:

~~~mermaid
flowchart TD
    A[AUTH-01 Login] --> B[AUTH-02 Verification]
    B -->|Verified| C[HOME-01 Dashboard]
    C -->|Open messages| D[CHAT-01 Chat List]
    D -->|Choose conversation| E[CHAT-02 Conversation]
~~~

The complete final question list must remain the last substantive section of the blueprint.

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
