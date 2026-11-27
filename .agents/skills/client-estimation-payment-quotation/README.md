# Client Estimation & Payment Quotation

Create a concise estimate/quotation that PQC can send directly to a client. It is not a full legal agreement.

[← Back to PQC AI Skills](../../../../README.md) · [Open skill instructions (`SKILL.md`)](./SKILL.md)

## What the client estimate includes

1. Prepared For: the correct client person and/or company.
2. Prepared By: Parallel Quintillion Coders (PQC) as developer/service provider.
3. Project overview and included scope.
4. Module/phase-wise deliverables and prices.
5. Estimated delivery timeline.
6. Subtotal, discount (if approved), taxes/third-party charges, and total.
7. Advance and milestone payment amounts and due points.
8. Client-side prerequisites and project-specific notes.
9. Assumptions, exclusions, and next step.

## Default payment proposal

If no payment plan has been agreed, the skill can propose 50% before kickoff, 30% at an agreed development milestone, and 20% before final handover. It calculates actual amounts and checks the total. The client pays PQC; PQC issues the invoice.

## When to use it

Use for an existing project or already-defined client scope when you need a short estimate only. For detailed cost auditing use Software Project Estimation Auditor. For a formal contract use Client Proposal & Legal Agreement Generator.

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
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent <agent-id>
~~~

Example for Claude Code:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent claude-code
~~~

### Install globally for your user account

This makes the skill available across projects for the selected agent.

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent <agent-id> --global
~~~

### Install for multiple agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent claude-code codex cursor antigravity
~~~

### Install for all supported agents

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent '*'
~~~

Add `--global` to the command for global installation.

---

## Update this skill

Update the project installation (run from the project root):

~~~bash
npx skills update client-estimation-payment-quotation -p
~~~

Update the global installation:

~~~bash
npx skills update client-estimation-payment-quotation -g
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
Use client-estimation-payment-quotation.

Review this existing project and prepare a concise estimate addressed
to the correct client. Include scope, modules, deliverables, timeline,
module-wise prices, total amount, payment milestones, client-side
prerequisites, and notes. PQC is the service provider; the client pays PQC.
Do not generate a full legal agreement.
~~~

## Notes

- Web research, repository access, file reading, and diagram rendering depend on the capabilities of the selected agent and tools connected to it.
- The skill is written in agent-neutral format; some execution features may vary between agents.
- Never share secrets, access tokens, passwords, private customer data, or bank details in prompts or public repositories.
