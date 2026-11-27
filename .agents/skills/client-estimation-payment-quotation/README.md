# Client Estimation & Payment Quotation

Create a concise estimate that PQC can send directly to a client. It includes the recipient, scope, price, timeline, payment milestones, client-side prerequisites, and notes — **not a full legal agreement**.

[← Back to PQC AI Skills](../../../../README.md) · [Open SKILL.md](./SKILL.md)

## When to use this skill

Use it when:
- The project already exists, or the client has supplied a defined scope.
- You have reviewed/approved the project estimate.
- You need a short, client-friendly quotation with prices and payment terms.

For a new product idea without a defined scope, use [Product Discovery & Blueprint Architect](../product-discovery-blueprint-architect/README.md) first. For detailed cost auditing, use [Software Project Estimation Auditor](../software-project-estimation-auditor/README.md).

## What the client estimate includes

1. **Prepared For:** correct client person and/or company name.
2. **Prepared By:** Parallel Quintillion Coders (PQC) as developer/service provider.
3. Project overview and scope included.
4. Module/phase-wise deliverables and cost.
5. Estimated delivery timeline.
6. Subtotal, approved discount, taxes/third-party charges, and total.
7. Payment terms and actual instalment amounts.
8. Client-side prerequisites.
9. Concise assumptions, exclusions, and notes.
10. Next step for estimate approval.

## Default payment proposal

Unless different terms have already been agreed, the skill may propose:

| Payment stage | Percentage | When due |
|---|---:|---|
| Advance | 50% | Before project kickoff |
| Development milestone | 30% | At the agreed progress/demo checkpoint |
| Final payment | 20% | Before final handover/release |

These are proposed defaults, not automatically agreed terms. The skill calculates actual amounts, checks that percentages total 100%, and states clearly that **the client pays PQC**.

## Client-side prerequisites

The estimate lists only prerequisites relevant to the project, for example:
- Brand assets, content, text, images, and design approvals.
- Existing source-code, hosting, server, domain, database, and deployment access.
- API documentation, vendor credentials, and third-party accounts.
- Client-owned app-store, payment, messaging, maps, email, or cloud accounts.
- Sample data, test accounts/devices, UAT, and timely approvals.

It explains who provides each item, when it is needed, who pays any external charges, and what may be delayed if it is missing.

## How to install in Antigravity

Run from the root of the project where you want the skill to be available.

**Project installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity
```

**Global installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent antigravity --global
```

## How to update

**Update project installation**

```bash
npx skills update client-estimation-payment-quotation -p
```

**Update global installation**

```bash
npx skills update client-estimation-payment-quotation -g
```

## Example prompt

```text
Use client-estimation-payment-quotation.

Review the existing project and prepare a professional estimate addressed
to the correct client. Include the project scope, modules, deliverables,
timeline, module-wise price, total amount, and proposed payment milestones.

Add the client-side prerequisites and concise notes. PQC is the developer
and service provider; the client is the customer and pays PQC.

Do not generate a full legal agreement. Do not invent missing client details,
prices, tax information, or payment instructions.
```

## Important

- The client name or company must be identified from accessible context; if missing, ask who the estimate should be addressed to.
- Do not expose internal developer costs, profit, or margins unless requested.
- Do not invent GST details, bank details, or tax rates.
- This estimate is a quotation, not a signed service contract.
