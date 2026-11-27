---
name: practical-software-engineering-standards
description: Apply pragmatic software engineering principles, architecture boundaries, code-size guidelines, security, testing, and review rules when planning, writing, or reviewing a new or existing software project.
---

# Practical Software Engineering Standards

Use these standards when creating a project blueprint, implementing features, or reviewing an existing codebase. Keep recommendations proportional to project size and risk. **Do not apply every principle mechanically.**

## 1. First inspect the project

For an existing project, inspect its language, framework, folder structure, architecture, dependencies, formatter, tests, and established conventions before recommending changes. Follow sound existing patterns; do not propose a rewrite just to match a preferred architecture.

For a new project, choose the simplest structure that supports its expected complexity, team size, security needs, and growth. State important assumptions.

## 2. AI-assisted coding workflow

Apply these behaviors to non-trivial implementation and review tasks:

1. **Think before coding:** inspect relevant files and call paths. Surface assumptions and trade-offs. Ask only when ambiguity blocks a safe, correct decision; otherwise state a reasonable assumption.
2. **Simplicity first:** deliver the smallest complete solution. Avoid speculative features, single-use abstractions, and unrequested configurability.
3. **Surgical changes:** in existing projects, change only what the request requires. Preserve established conventions and contracts; avoid drive-by refactoring. Remove only unused code made obsolete by your change. Report unrelated issues separately.
4. **Verifiable goals:** define acceptance checks before implementation. Reproduce bugs with a test where practical; run relevant tests, lint, build, or type checks after changes. Clearly report what passed, failed, or could not be run.

For trivial, obvious changes, use judgment rather than performing a heavyweight process. These practices are adapted from the community-maintained [andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) project, which describes its guidance as derived from Andrej Karpathy's observations on LLM coding pitfalls; it is not an official Andrej Karpathy project or endorsement.

## 3. Core principles

| Principle | Apply it when | Practical rule |
|---|---|---|
| KISS | Always | Prefer the simplest solution that meets the requirement. |
| YAGNI | Designing scope | Do not build speculative features or abstractions. |
| SoC | Separating responsibilities | Keep UI, business rules, data access, and infrastructure concerns distinct where useful. |
| DRY | Repeated knowledge or business rules | Centralize logic when duplication risks inconsistent behavior. Similar-looking code is not automatically the same responsibility. |
| SOLID | Object-oriented code with meaningful complexity | Use focused responsibilities and interfaces; avoid abstractions that add no real flexibility. |
| Composition over inheritance | Reusing behavior | Prefer small composable units over deep inheritance trees. |
| Encapsulation | Protecting state and invariants | Expose deliberate operations, not uncontrolled internal state. |
| Least privilege | Accessing data or capabilities | Grant only the permissions required. |

Do not force SOLID onto simple scripts, CRUD handlers, data models, or small functions. Avoid premature generalization. A little duplication is often safer than a misleading shared abstraction.

## 4. Architecture and dependencies

- Keep business rules independent of UI, framework, database, and network details when project complexity justifies the separation.
- Define clear module ownership and interfaces; avoid circular dependencies.
- Keep dependency direction intentional. High-level business rules should not be coupled directly to replaceable infrastructure.
- Put validation and business invariants at the appropriate boundary; do not rely only on UI validation.
- Use one authoritative source for each piece of state. Avoid duplicated mutable state unless synchronization is explicit.
- Prefer a modular monolith until independent deployment, scaling, ownership, or reliability needs justify services.

Do not add layers, repositories, use cases, dependency-injection frameworks, or microservices by default. Explain the concrete problem each abstraction solves.

## 5. File, class, and function size

These are **review signals, not hard limits**. Cohesion, readability, complexity, and change frequency matter more than line count.

| Element | Useful starting range | Review when |
|---|---:|---|
| Function / method | 5–30 lines | It exceeds ~40–50 lines or performs multiple tasks |
| Class / component | 50–200 lines | It exceeds ~300 lines or has multiple reasons to change |
| Source file | 100–300 lines | It exceeds ~400–500 lines or contains unrelated responsibilities |
| Nesting | 1–3 levels | It exceeds 3–4 levels |
| Parameters | 2–4 | Many related values should be grouped into a meaningful type |

Exceptions are valid for generated code, schemas, declarative UI, migrations, configuration, and cohesive data definitions. Never split code solely to satisfy a number. Extract only when it improves naming, testability, reuse, or comprehension.

## 6. Implementation quality

- Use clear, consistent names and the repository's formatter, linter, and language conventions.
- Keep functions focused; validate inputs at trust boundaries.
- Handle errors deliberately. Never silently swallow failures or expose internal stack traces to end users.
- Avoid global mutable state, hidden side effects, unexplained constants, dead code, and unnecessary dependencies.
- Keep secrets out of source control and logs. Do not log passwords, tokens, or sensitive personal data.
- Add comments for intent, constraints, and non-obvious decisions—not to narrate obvious code.
- Make changes narrowly in existing projects; avoid unrelated refactoring.

## 7. Testing, security, and reliability

- Test important business rules with unit tests; test database, API, and integration boundaries with integration tests.
- Add UI/end-to-end tests for critical user journeys, not every minor visual detail.
- Cover success, failure, boundary, and authorization cases for high-risk behavior.
- Enforce authentication and authorization on trusted server boundaries. Validate and constrain untrusted input.
- Use secure secret storage, transport encryption, safe data handling, and dependency updates appropriate to the platform.
- Consider accessibility, performance, offline behavior, backups, migrations, and observability when relevant to the product—not as boilerplate for every project.

## 8. Review checklist

Before completing a feature or recommending approval, check:

1. Does it meet the requirement without unnecessary complexity?
2. Are responsibilities and dependencies clear?
3. Is business logic duplicated or incorrectly coupled?
4. Are validation, errors, permissions, and sensitive data handled safely?
5. Are important success, failure, and boundary cases tested?
6. Does it follow the existing project conventions?
7. Is documentation needed for setup, configuration, APIs, or important decisions?

Report only actionable findings. Prioritize **critical security/data-loss issues**, then correctness, maintainability, performance, and style. Do not block a change for subjective preferences.

## 9. Output rules

For a project blueprint, include a compact **Engineering Standards** section containing only applicable principles, architecture boundaries, naming/file conventions, testing, and security requirements.

For code review, report: severity, file/location, issue, impact, and recommended fix. Separate confirmed defects from suggestions.

Do not repeat this entire standard in every response. Mention only decisions that affect the current project. If a project-specific convention conflicts with this guide, inspect and explain the trade-off before changing it.

## Source

- [multica-ai/andrej-karpathy-skills](https://github.com/multica-ai/andrej-karpathy-skills) — community-maintained, MIT-licensed reference for the four AI-coding workflow behaviors above. The PQC skill summarizes and adapts the ideas; it does not reproduce the source files.
