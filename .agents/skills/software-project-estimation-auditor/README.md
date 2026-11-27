# Software Project Estimation Auditor

Build a realistic, evidence-based estimate for an existing software project, repository, or already-defined client scope.

[← Back to PQC AI Skills](../../../../README.md) · [Open skill instructions (`SKILL.md`)](./SKILL.md)

## What it creates

- Confirmed, assumed, unknown, and recommended scope.
- Module, feature, workflow, and dependency audit.
- Missing-requirement gap register with severity and impact.
- Technical skill and team-role matrix.
- Task-level effort using optimistic, likely, pessimistic, and PERT estimates.
- Role and phase totals, delivery schedule, milestones, and critical path.
- Current market-rate research with sources, dates, geography, and billing model.
- Internal cost, contingency, quote scenarios, profit, and margin.
- Client responsibilities, prerequisites, assumptions, exclusions, and risks.

## When to use it

Use when you already have an existing app, website, backend, repository, client PRD/SRS, feature list, UI design, API documentation, or defined enhancement scope.

**This is not a scratch-project ideation skill.** For a new idea with no defined requirements, use Product Discovery & Blueprint Architect first and approve the product scope.

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
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent <agent-id>
~~~

Example for Claude Code:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent claude-code
~~~

### Install globally for your user account

This makes the skill available across projects for the selected agent.

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent <agent-id> --global
~~~

### Install for multiple agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent claude-code codex cursor antigravity
~~~

### Install for all supported agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill software-project-estimation-auditor --agent '*'
~~~

Add `--global` to the command for global installation.

---

## Update this skill

Update the project installation (run from the project root):

~~~bash
npx skills update software-project-estimation-auditor -p
~~~

Update the global installation:

~~~bash
npx skills update software-project-estimation-auditor -g
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
Use software-project-estimation-auditor.

Inspect this existing project and its available requirements.
Audit the modules, workflows, dependencies, missing gaps, and skills.
Estimate effort by role and phase, build a dependency-aware schedule,
research current market rates for the relevant geography, and calculate
low / likely / high cost scenarios. Cite rate sources and do not invent facts.
~~~

## Notes

- Web research, repository access, file reading, and diagram rendering depend on the capabilities of the selected agent and tools connected to it.
- The skill is written in agent-neutral format; some execution features may vary between agents.
- Never share secrets, access tokens, passwords, private customer data, or bank details in prompts or public repositories.
