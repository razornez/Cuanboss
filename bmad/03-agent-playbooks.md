# Agent Playbooks

## Status

Draft. Playbooks must be validated through market research and pilot data before becoming automated rules.

## Core Principle

Daily to-do lists must not be random.

Every task must be generated from one of these sources:

1. Business onboarding data
2. Sales funnel stage
3. Prospect/customer behavior
4. Proven sales/marketing playbook
5. Website/SEO analytics
6. Campaign performance
7. Owner capacity and constraints
8. Capital readiness gap
9. Previous task outcomes

## Agent Types

### 1. Sales Agent

Goal:
Create and move sales opportunities toward order/DP/payment.

Responsibilities:
- Identify potential prospects.
- Score prospect relevance.
- Create outreach tasks.
- Create follow-up reminders.
- Prepare sales scripts.
- Prepare quotation tasks.
- Detect hot leads.
- Track lost reasons.
- Recommend next-best action.

Example tasks:
- Follow up 5 leads that requested price but have not responded.
- Send quotation draft to prospects that already provided quantity and deadline.
- Ask for missing information from leads stuck at `Need Info`.
- Reactivate old customers that previously purchased similar products.

### 2. Marketing Agent

Goal:
Create demand and trust through sales-oriented content and channels.

Responsibilities:
- Generate landing page ideas.
- Create content from real products, portfolio, FAQs, and customer problems.
- Recommend weekly campaigns.
- Monitor visitor/CTA trend.
- Recommend content improvements.
- Generate Google Business Profile/posting tasks where relevant.

Example tasks:
- Publish a portfolio case study from a completed order.
- Add FAQ based on repeated customer questions.
- Create a campaign for seasonal/event-based demand.
- Improve CTA copy on a page with visitors but low WhatsApp clicks.

### 3. Business Strategy Agent

Goal:
Help owner make better growth decisions.

Responsibilities:
- Analyze product/service performance.
- Identify strongest customer segment.
- Recommend package/pricing experiments.
- Analyze lost deal reasons.
- Recommend repeat order strategy.
- Recommend new target market opportunities.

Example tasks:
- Review top 3 products by inquiry and closing rate.
- Create a lower-risk entry package for price-sensitive prospects.
- Recommend focusing on a segment with higher closing rate.

### 4. IT Agent

Goal:
Ensure the digital sales infrastructure works.

Responsibilities:
- Setup website/landing page.
- Setup forms and WhatsApp CTA tracking.
- Monitor website health.
- Monitor tracking events.
- Detect broken links/forms.
- Create technical SEO tasks.

Example tasks:
- Fix missing WhatsApp CTA on a landing page.
- Add tracking to a campaign link.
- Create event tracking for quotation clicks.

### 5. Capital Readiness Agent

Goal:
Help business become more financing-ready.

Responsibilities:
- Check completeness of business profile.
- Track invoice/payment evidence.
- Summarize sales history.
- Identify missing legal/financial documents.
- Recommend funding option research.
- Generate capital readiness tasks.

Example tasks:
- Complete business profile and owner identity fields.
- Upload transaction history for the last 3 months.
- Create revenue summary from invoices.
- Prepare one-page business profile for financing/investor discussion.

## Task Quality Standard

Every generated task must include:

```text
title
agent_type
priority
reason
expected_impact
required_owner_action
data_source
status
due_date
success_criteria
```

Bad task:

```text
Post content today.
```

Good task:

```text
Create a portfolio post for the latest 24-piece jersey order.
Reason: Completed orders improve trust and can become proof for prospects asking about quality.
Expected impact: Improve conversion confidence and provide content for website/social/WhatsApp catalog.
Owner action: Upload 3 photos and approve caption.
Success criteria: Post published, linked to landing page, and CTA tracked.
```

## Daily Task Generation Logic

### Step 1 — Business State Check

Questions:
- Is onboarding complete?
- Are products defined?
- Is the website live?
- Are landing pages live?
- Are CTA/form tracking active?
- Are prospects available?
- Are leads waiting for response?
- Are quotations waiting for follow-up?
- Are orders waiting for payment/status update?

### Step 2 — Funnel Gap Detection

Possible gaps:
- No visitors
- Visitors but no CTA clicks
- CTA clicks but no lead capture
- Leads but no quotation
- Quotations but no follow-up
- Follow-up but low closing
- Orders but no repeat activation
- Revenue but no finance record

### Step 3 — Generate Next-Best Actions

Task priority rules:

1. Hot lead/follow-up due beats content creation.
2. Quotation requested beats prospect discovery.
3. Broken website/form/CTA blocks all growth tasks.
4. If pipeline is empty, prospect discovery and campaign tasks become high priority.
5. If leads exist but no closing, closing diagnostics and follow-up tasks become high priority.
6. If orders exist, testimonial/repeat order/content-from-proof tasks become high priority.

## Example Daily Report

```text
Daily Agent Report

Completed:
- Business profile analyzed
- Website draft created
- 3 landing page ideas generated

In Progress:
- Prospect discovery for schools, communities, and local organizations
- Lead scoring for 20 prospect candidates

Needs Owner Approval:
- Outreach message draft for 5 high-priority prospects
- Package offer draft for minimum order segment

High Priority Today:
- Follow up 3 leads that requested price yesterday
- Upload 3 product photos for trust-building content
- Approve quotation template

Estimated Impact:
- Pipeline potential: based on active opportunities, not guaranteed revenue
- Main blocker: owner approval needed for outreach and quotation template
```

## Automation Level

Each action must have automation mode:

1. `guide_only` — system recommends, owner executes.
2. `draft_for_approval` — system prepares, owner approves.
3. `semi_automatic` — system executes approved workflow.
4. `managed_service` — human/team helps execute for higher tiers.

Cold outreach must default to `guide_only` or `draft_for_approval` unless compliance and consent requirements are satisfied.
