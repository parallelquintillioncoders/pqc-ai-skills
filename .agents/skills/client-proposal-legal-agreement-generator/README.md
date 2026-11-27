# Client Proposal & Legal Agreement Generator

Convert an approved project estimate into a professional client proposal, Statement of Work (SOW), payment schedule, and draft software development services agreement.

[← Back to PQC AI Skills](../../../../README.md) · [Open SKILL.md](./SKILL.md)

## Party roles — do not reverse them

- **Development company / Service Provider:** Parallel Quintillion Coders (PQC).
- **Client / Customer:** the person or company commissioning the software and paying PQC.

The skill uses PQC's public-facing contact details as a starting point, checks accessible project/conversation information for both parties, and asks only for missing details. PQC's brand name must not be mistaken for a registered legal entity; legal entity, authorized signatory, and tax details must be confirmed when needed.

## When to use this skill

Use it when:
- The project scope and estimate have been reviewed.
- The client needs a formal proposal and/or SOW.
- You need a draft development agreement with payment, ownership, acceptance, support, cancellation, and other commercial/legal terms.

For a short estimate only, use [Client Estimation & Payment Quotation](../client-estimation-payment-quotation/README.md).

## What it produces

- Client-facing project proposal and quotation.
- Detailed scope and deliverables / SOW.
- Advance and milestone payment schedule.
- Client responsibilities, prerequisites, and change-request rules.
- Acceptance and testing process.
- IP/source-code ownership and transfer terms, as agreed.
- Confidentiality and data-protection clauses.
- Warranty versus paid maintenance/support.
- Cancellation, termination, liability, and dispute clauses for legal review.
- Correct provider/client signature blocks.

## How to install in Antigravity

Run from the root of the project where you want the skill to be available.

**Project installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity
```

**Global installation**

```bash
npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-proposal-legal-agreement-generator --agent antigravity --global
```

## How to update

**Update project installation**

```bash
npx skills update client-proposal-legal-agreement-generator -p
```

**Update global installation**

```bash
npx skills update client-proposal-legal-agreement-generator -g
```

## Example prompt

```text
Use client-proposal-legal-agreement-generator.

Use the approved estimate and project scope to prepare a client-ready
proposal, SOW, payment schedule, and draft software development agreement.

PQC is the development company/service provider. The customer is the client.
Recover existing information from accessible project context and ask only
for missing client or PQC legal details. Use visible placeholders where needed.

Keep internal costs and margins out of the client document.
```

## Legal and privacy notes

- This skill drafts commercial/legal text; it is not a substitute for advice from a qualified lawyer in the relevant jurisdiction.
- Do not assume a legal entity, GSTIN, PAN, bank account, registered office, governing law, or court.
- Payment percentages, refund provisions, liability caps, IP transfer, and dispute terms must be confirmed and reviewed before signing.
- Never commit confidential client details, credentials, bank data, or private agreements to the public repository.
