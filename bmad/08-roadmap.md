# Roadmap

## Status

Draft. Roadmap should be updated after pilot research.

## Roadmap Principle

Build the product around visible daily agent work and measurable sales opportunity creation.

Do not start by building too many advanced features. Start with the smallest system that proves:

```text
Business onboarding → Agent task generation → Prospect/lead tracking → Follow-up/quotation → Live sales progress report
```

## Phase 0 — Research & Validation

Goals:
- Validate target segment.
- Validate real UMKM pain points.
- Validate willingness to pay.
- Validate cost-to-serve assumptions.
- Validate prospect discovery sources.

Deliverables:
- Interview notes from 10–20 UMKM owners.
- Segment selection.
- Pilot merchant criteria.
- Pricing hypothesis.
- Cost model spreadsheet.
- Compliance source review.
- Manual playbook prototype.

Success criteria:
- At least 3 verticals researched.
- At least 1 vertical selected for pilot.
- Clear evidence that users care about sales opportunity creation, not just website/content.

## Phase 1 — Concierge MVP

Goal:
Prove the workflow manually/semi-manually before heavy automation.

Features:
- Business onboarding form
- Product catalog setup
- Manual website/landing page draft
- Agent task board
- Prospect list database
- Manual prospect validation
- Outreach draft templates
- Lead CRM
- Quotation draft
- Live report dashboard mock or simple app

Human-assisted operations:
- Validate prospects manually.
- Review task quality.
- Help owner execute follow-up.
- Measure results weekly.

Success criteria:
- 5–10 pilot merchants onboarded.
- Daily/weekly tasks generated.
- Prospects and leads tracked.
- Quotations/follow-ups tracked.
- Early ROI/cost data collected.

## Phase 2 — SaaS MVP

Goal:
Turn the concierge process into a repeatable product.

Features:
- Multi-tenant auth
- Business onboarding wizard
- Product/service catalog
- Website/landing page generator
- Agent task engine
- Prospect database
- Lead CRM pipeline
- Outreach draft generator
- Quotation builder
- Basic analytics events
- Live report dashboard
- Usage/cost metering

Success criteria:
- Owner can see daily agent activity.
- Agent tasks have reasons and expected impact.
- Leads and prospects connect to follow-up and quotations.
- Per-tenant cost can be measured.

## Phase 3 — Automation & Integrations

Goal:
Reduce manual work while keeping compliance and quality.

Features:
- Integrate website analytics.
- Integrate email sending/drafts.
- Integrate WhatsApp-approved workflows where compliant.
- Prospect source connectors with provenance tracking.
- AI-based lead scoring.
- AI-based next-best-action recommendation.
- Scheduled daily/weekly reports.
- Follow-up reminder automation.

Success criteria:
- More tasks are generated from real data.
- Prospect discovery quality improves.
- Follow-up completion rate improves.
- Merchant cost-to-serve decreases.

## Phase 4 — Capital Readiness & Business Strategy

Goal:
Expand beyond sales execution into business growth and financing readiness.

Features:
- Finance readiness checklist
- Revenue/invoice summary
- Customer repeat-order evidence
- Business profile one-pager
- Funding option research tasks
- Strategy recommendation engine
- Pricing/package recommendation
- Lost deal analysis

Success criteria:
- Merchant can export basic business profile and performance summary.
- Owner receives actionable strategy recommendations.
- Capital readiness score improves over time.

## Phase 5 — Managed Growth Layer

Goal:
Offer higher-value assisted service where software alone is not enough.

Features:
- Human prospect validation
- Campaign setup support
- Monthly/weekly growth review
- Managed onboarding
- Performance report
- Optional success-fee model

Success criteria:
- Higher retention.
- Better merchant ROI.
- Clear separation between self-service and managed service costs.

## Initial MVP Backlog

### Epic 1 — Tenant & Business Onboarding

- Create tenant model
- Create user/role model
- Create business profile form
- Create product catalog form
- Create readiness score draft

### Epic 2 — Agent Task Board

- Create task model
- Create task status workflow
- Create daily task list UI
- Create owner approval flow
- Create task result logging

### Epic 3 — Prospect & Lead Management

- Create prospect model
- Create lead model
- Add source/provenance fields
- Add relevance score
- Add manual validation status
- Add pipeline status

### Epic 4 — Outreach & Follow-Up

- Create outreach template model
- Create message draft generator
- Add owner approval
- Add follow-up reminder
- Track response/outcome

### Epic 5 — Quotation

- Create quotation model
- Create quotation item builder
- Add quotation status
- Add follow-up reminder
- Add PDF/share link later

### Epic 6 — Website & Landing Pages

- Create website model
- Create landing page model
- Generate draft content
- Add CTA tracking
- Add published URL tracking

### Epic 7 — Live Report

- Daily agent activity report
- Prospect/lead summary
- Follow-up/quotation summary
- Pipeline summary
- ROI/break-even placeholder

### Epic 8 — Cost Metering

- Track AI actions
- Track prospect discovery runs
- Track website/page usage
- Track support/manual validation minutes
- Track per-tenant cost estimates

## Critical Build Order

1. Data model and tenant isolation
2. Business onboarding
3. Agent task board
4. Prospect/lead database
5. Manual task/recommendation generation
6. Live report dashboard
7. Quotation/follow-up workflow
8. Website/landing page generator
9. Usage/cost metering
10. Automation/integrations

## Things Not To Build Too Early

- Native mobile app
- Full ERP/accounting
- Fully automated cold outreach
- Complex inventory
- Large-scale scraping engine
- Sophisticated AI agent autonomy without guardrails
- Performance guarantee engine before pilot data
