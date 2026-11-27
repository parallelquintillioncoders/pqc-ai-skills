---
name: client-estimation-payment-quotation
description: Create a concise client-facing software project estimate/quotation with project scope, module-wise pricing, delivery timeline, total amount, and payment milestones. Always identify who the estimate is prepared for and show PQC as the development service provider. Do not generate a full legal agreement.
---

# Client Estimation & Payment Quotation

## Agent compatibility

This is an agent-neutral Agent Skills instruction file, not an Antigravity-only skill. It can be installed through the Skills CLI into any supported agent, including Claude Code, Codex, Cursor, Antigravity, Gemini CLI, GitHub Copilot, Cline, and other agents listed in the [official supported-agent directory](https://github.com/vercel-labs/skills/blob/main/docs/agents.md).

Install it with `npx skills add parallelquintillioncoders/pqc-ai-skills --skill client-estimation-payment-quotation --agent <agent-id>`. The Skills CLI maps it to the selected agent's supported skill directory. Web browsing, repository/file access, and diagram rendering depend on the selected agent and its connected tools.


## Purpose

Prepare only the estimate/quotation that PQC can send directly to a prospective or existing client.

The output should be short, professional, easy to understand, and commercially clear. It normally fits one or two pages.

**This skill is NOT for a full proposal, Statement of Work, legal agreement, or service contract.** Do not generate long legal clauses, confidentiality terms, indemnities, liability sections, dispute-resolution clauses, or signature-heavy contracts. Keep only the estimate, scope summary, delivery timeline, price, assumptions/exclusions, and payment terms needed for a quotation.

## Party direction — mandatory

- **Prepared by / Developer / Service Provider:** Parallel Quintillion Coders (PQC)
- **Prepared for / Client / Customer:** the person or company receiving the estimate.

PQC is doing the development work and issuing the estimate. The client is the buyer/customer and pays PQC. Never reverse these roles.

## PQC provider details

Use this public-facing provider identity by default:
- Business/brand: Parallel Quintillion Coders (PQC)
- Website: https://parallelquintillioncoders.com/
- Public contact address: D-225 Sumel-11, near Namaste Circle, Ahmedabad, 380004, Gujarat, India
- Phone: +91 9057516113
- Email: info@parallelquintillioncoders.com

When web access is available, verify the contact details on the official PQC website before creating the final estimate. If web access is unavailable, use these saved public contact details and ask the user to confirm if they have changed.

Do not infer that the PQC brand name is the registered legal contracting entity. This estimate can use the PQC public brand identity; do not add company registration, GSTIN, PAN, proprietor/director, or bank details unless provided and verified. Do not label the published contact address as a registered office.

## Step 1 — Identify the recipient before drafting

The estimate must always visibly state:

**Prepared For:** [Client Person Name]
**Client Company:** [Client Company Name, if applicable]

At least one recipient identifier — the client's full name or company name — is mandatory. Prefer both when available.

Before asking the user, retrieve client information from sources actually accessible to the agent:
1. Current conversation and previous messages in this conversation.
2. Relevant accessible conversation/project history.
3. Current workspace files and repository: PRD, estimate, requirements, client brief, proposal, invoice, emails exported to files, etc.
4. Connected email/CRM/drive sources only if a relevant integration is connected and authorized.
5. Any client details explicitly supplied with the estimate request.

Do not claim to have searched inaccessible chats, accounts, or files. Do not take a client identity from an unrelated project. Do not guess a person, company, contact, country, email, or address.

Extract only what is known:
- Client person/contact name
- Client company/business name
- Client email (optional)
- Client billing/country/address (optional; include only when relevant and supplied)

If the client name and company cannot be found, ask the user one direct question:
**"Who should this estimate be addressed to? Please share the client's name or company name."**

If the recipient's name or company is known but optional contact fields are not, do not block the estimate. Simply omit those fields. Never send a final client-facing estimate with an empty "Prepared For" field or a fabricated recipient. If the user explicitly asks for a template, use a clearly visible placeholder.

## Step 2 — Understand project and estimate scope

Use the approved project estimate, PRD, brief, repository, or user instructions. Reuse existing estimates and do not recalculate already-approved figures without a reason.

Include only enough scope detail for the client to understand what is being priced:
- Project name
- One or two sentence project understanding
- Main modules/features included
- Key deliverables/platforms
- Important integrations, where applicable
- Estimated delivery duration and major milestones

If module detail is not yet available, make the limitation clear. Do not invent features or imply they are included.

Do not expose internal developer salaries, internal hourly costs, individual employee rates, profit, markup, margin, confidential estimation notes, or internal risk scores unless the user explicitly asks.

## Step 3 — Price presentation

Use the approved estimate or calculate a quote from the supplied requirements. Present a simple, client-readable price breakdown.

Preferred table:

| Item / Module | Brief scope or deliverable | Amount |
|---|---|---:|

Depending on scope, group very small tasks into sensible phases or modules. Avoid overwhelming the client with low-level developer tasks or internal work breakdown details.

Show:
- Subtotal
- Discount, only if approved
- Taxes (GST/VAT) separately, only when applicability/rate/registration is confirmed
- Third-party charges separately (hosting, domain, SMS/WhatsApp, maps, payment gateway, licenses, app-store fees, etc.)
- **Total estimated project fee**
- Currency

Ensure arithmetic is exact. All module amounts, discounts, taxes, and totals must reconcile. If tax status is unknown, say "Applicable taxes, if any, will be charged separately as per applicable law" rather than inventing a rate or registration status.

If the user has not supplied a currency, infer it only when clearly established by the client/project context; otherwise ask or clearly mark the proposed currency for confirmation. Do not silently mix currencies.

## Step 4 — Payment terms (must be included)

The estimate must include a short, clearly visible Payment Terms section. It is a commercial payment schedule, not a long legal agreement.

If no payment schedule has been agreed, propose this editable default:
- **50% advance** payable to PQC before project kickoff.
- **30% milestone payment** at the agreed development/progress checkpoint.
- **20% final payment** before final handover or production release.

The percentages must total 100%. Calculate actual amounts based on the quote total and show both percentage and amount. Round sensibly and reconcile any rounding difference in the final instalment.

Adapt for the project when appropriate:
- Small/short projects may use 50% advance and 50% before delivery.
- Longer projects may use advance plus monthly or phase-wise payments.
- Use the user's explicit agreed payment terms instead of the default.

State payment direction explicitly:
**Client pays Parallel Quintillion Coders (PQC). PQC issues the invoice/payment request to the Client.**

Clarify when each payment is due, using objective milestones. Example:
- Advance: before project commencement.
- Second instalment: after completion/demo of the named milestone.
- Final instalment: before handover/release of the agreed deliverables.

Do not invent bank details, UPI IDs, payment links, interest rates, late fees, or penalties. Do not state that advance payments are automatically non-refundable. If the user has agreed to different payment terms, reflect them accurately.

## Step 5 — Timeline and commercial notes

Show a realistic estimated delivery duration. Include start-date dependency if kickoff depends on:
- Receipt of advance payment
- Client approval of the estimate
- Receipt of required content, credentials, designs, or access

### Client-side prerequisites

Add a short **Client-Side Prerequisites** section to the estimate. Include only items relevant to this specific project; do not dump a generic checklist onto every client.

Check the project materials and identify what the client must provide, approve, purchase, configure, or make available for PQC to deliver the quoted scope. Common examples include:
- A single authorized point of contact and timely business/technical decisions.
- Final requirements, workflows, business rules, and consolidated approvals.
- Brand assets, logos, text, translations, images, videos, documents, and other content.
- UI/UX references, design files, prototypes, or timely design approvals where applicable.
- Access to existing source code, repositories, hosting/server, domain/DNS, database, and deployment environments.
- API documentation, sandbox/production credentials, vendor contacts, and permissions for third-party integrations.
- Client-owned accounts and approvals for Google Play, Apple App Store, payment gateways, SMS/WhatsApp, maps, email, cloud, analytics, or other external services.
- Sample/import data, test accounts, test cases, devices, or hardware needed for implementation and UAT.
- Legal rights/consents for client-supplied content and permission to process supplied data.
- Client-side testing, UAT feedback, and written milestone acceptance.

For each prerequisite that matters, state:
- What PQC needs from the client.
- When it is required (before kickoff, during development, UAT, or launch).
- Whether it is client-provided/client-paid or included in PQC's price.
- The likely effect if it is late or unavailable (for example, blocked integration, delayed milestone, revised timeline or additional cost).

Do not imply that PQC will purchase third-party subscriptions, provide client-owned accounts, obtain regulatory approvals, produce missing client content, or migrate inaccessible data unless explicitly included in the estimate.

### Notes

Include a concise **Notes** section immediately after Client-Side Prerequisites or Assumptions:
- This estimate is based on the project information and scope available on the issue date.
- Project kickoff depends on the agreed advance payment and receipt of the prerequisites marked "required before kickoff".
- Client delays in providing access, assets, decisions, testing, or approvals may affect delivery dates.
- Items not listed as included are excluded; additional features or changed requirements require a revised estimate/change approval.
- Third-party fees and applicable taxes are separate unless explicitly included in the total.

Use only notes relevant to the project. Keep this section concise and do not add lengthy legal boilerplate. This is an estimate/quotation, not the signed service agreement.

## Required output layout

Produce the estimate in this order:

1. **Header:** ESTIMATE / PROJECT QUOTATION; estimate number if provided; issue date; validity.
2. **Prepared For:** client person and/or company name — this must not be blank.
3. **Prepared By:** Parallel Quintillion Coders (PQC), public website and relevant contact details.
4. **Project:** project name and short understanding.
5. **Scope Included:** short module/feature list with brief deliverables.
6. **Estimated Timeline:** expected duration and key milestones.
7. **Cost Estimate:** simple module/phase price table, subtotal, discount (if any), taxes/third-party charges, total.
8. **Payment Terms:** advance, milestone and final payment percentages, amounts, and due triggers; client pays PQC.
9. **Client-Side Prerequisites:** a project-specific list of materials, access, accounts, decisions, approvals, test data/devices, and UAT support the client must provide, with timing and any client-paid costs.
10. **Assumptions / Not Included:** only material points, in concise language.
11. **Notes:** concise estimate basis, kickoff dependency, delay impact, scope-change treatment, and third-party/tax notes.
12. **Next Step:** client can approve the estimate by replying with written confirmation so PQC can issue the invoice and schedule kickoff. Do not imply that the estimate itself is a full agreement.

## Style and file format

- Use polished business English by default; use the client's preferred language if known or requested.
- Keep it concise and client-friendly — no internal analysis or lengthy legal terms.
- If the user asks for PDF, DOCX, Excel, or email text, create only that requested format using available tools.
- Use a clean branded layout, clear totals, and a prominent recipient name/company.
- Do not include a full contract or SOW as an unsolicited attachment.
- If no file-generation tool is available, provide the complete ready-to-copy estimate text.

## Final checks before sending

- "Prepared For" identifies the correct client person and/or company.
- "Prepared By" identifies PQC as the developer/service provider.
- Client and developer roles are never reversed.
- Recipient details are taken from accessible context, not guessed.
- Scope matches the approved project estimate.
- Total fee, currency, tax notes, and payment amounts reconcile.
- Advance payment is clearly stated and payable to PQC before kickoff unless the user specified otherwise.
- Payment milestones sum to 100%.
- Delivery duration and validity are visible.
- Exclusions and assumptions are concise and material.
- Project-specific client-side prerequisites are listed with timing and responsibility.
- Notes explain kickoff dependencies, delays, scope changes, and external costs where relevant.
- No full legal agreement, lengthy legal clauses, internal margin, or confidential costing is included.
- Unknown information is omitted or clearly marked for confirmation, never invented.

## Interaction behaviour

First use the project/client details already available in conversation history and files. If the recipient cannot be identified, ask only who the estimate should be addressed to. If other optional client contact fields are missing, proceed without them. If price, scope, currency, or payment schedule is genuinely unknown, ask only for the missing information that blocks a reliable estimate; otherwise create a preliminary estimate clearly labelled as such.
