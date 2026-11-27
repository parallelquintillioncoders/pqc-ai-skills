# Practical Software Engineering Standards

A compact, language-neutral skill for applying the right engineering practices without overengineering.

## Use it for

- Defining engineering rules in a new-project blueprint.
- Reviewing architecture and code organization in an existing project.
- Applying DRY, SOLID, KISS, YAGNI, separation of concerns, security, and testing appropriately.
- Reviewing file/function size without enforcing arbitrary line limits.

## Install

Project-local:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill practical-software-engineering-standards
~~~

For a specific agent:

~~~bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill practical-software-engineering-standards --agent <agent-id>
~~~

Global install: add `--global`.

## Example prompts

~~~text
Use practical-software-engineering-standards.
Define only the engineering standards needed for this project.
Keep the rules concise and avoid unnecessary architecture.
~~~

~~~text
Use practical-software-engineering-standards.
Inspect this existing codebase and identify actionable architecture,
maintainability, security, and testing issues. Do not rewrite unrelated code.
~~~

## Included AI-coding workflow

Adapted from the community-maintained [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills):

- Think before coding; surface assumptions and material ambiguity.
- Prefer the smallest complete solution.
- Make surgical changes; avoid unrelated refactoring.
- Define success criteria and verify with relevant tests/checks.

The source project says its guidance is derived from Andrej Karpathy's observations; it is not an official Andrej Karpathy project or endorsement.

## Important

File and function sizes are review signals, not mandatory limits. The skill prioritizes project conventions, cohesion, simplicity, and risk over rigid rules.

## Update

~~~bash
npx skills update practical-software-engineering-standards -p
npx skills update practical-software-engineering-standards -g
~~~

The update commands apply to skills tracked by the Skills CLI. Manually copied folders must be refreshed manually.

## Source

- [andrej-karpathy-skills repository](https://github.com/multica-ai/andrej-karpathy-skills)
