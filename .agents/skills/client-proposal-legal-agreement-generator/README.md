# Client Proposal & Legal Agreement Generator

Convert an approved project estimate into a structured client proposal and draft development agreement with clear commercial terms.

[← Back to PQC AI Skills](../../../README.md) · [Open skill instructions (`SKILL.md`)](./SKILL.md)

## What it creates

- Client-facing project proposal and quotation.
- Detailed scope and deliverables / Statement of Work.
- Advance and milestone payment schedule.
- Client responsibilities, prerequisites, and change-request controls.
- Acceptance and testing process.
- Intellectual-property and source-code terms.
- Confidentiality and data-protection clauses.
- Warranty versus paid maintenance/support.
- Cancellation, termination, liability, and dispute clauses for legal review.
- Correct provider/client signature blocks.

## Party roles

- **Service Provider / Developer:** Parallel Quintillion Coders (PQC).
- **Client / Customer:** the person or company commissioning the work and paying PQC.

The skill recovers available information from the conversation and project files, checks PQC's public contact details, and asks only for missing legal details. PQC's public brand name is not automatically its registered legal entity.

## When to use it

Use after the scope and estimate have been approved, when the client needs a formal proposal, SOW, and draft agreement. For a short estimate only, use Client Estimation & Payment Quotation.

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
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent <agent-id>
~~~

Example for Claude Code:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent claude-code
~~~

### Install globally for your user account

This makes the skill available across projects for the selected agent.

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent <agent-id> --global
~~~

### Install for multiple agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent claude-code codex cursor antigravity
~~~

### Install for all supported agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent '*'
~~~

Add `--global` to the command for global installation.

---

## Update this skill

Update the project installation (run from the project root):

~~~bash
npx skills update client-proposal-legal-agreement-generator -p
~~~

Update the global installation:

~~~bash
npx skills update client-proposal-legal-agreement-generator -g
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
Use client-proposal-legal-agreement-generator.

Use the approved scope and estimate to prepare a client-facing proposal,
SOW, payment schedule, and draft software development services agreement.
PQC is the service provider and the customer is the client. Recover
available party information and use visible placeholders for missing
legal details. Do not expose internal cost or margin.
~~~

## Notes

- Web research, repository access, file reading, and diagram rendering depend on the capabilities of the selected agent and tools connected to it.
- The skill is written in agent-neutral format; some execution features may vary between agents.
- Never share secrets, access tokens, passwords, private customer data, or bank details in prompts or public repositories.
