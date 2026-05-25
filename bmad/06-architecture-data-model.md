# Architecture & Data Model Draft

## Status

Draft. Technical stack and architecture are not finalized.

## Architecture Goal

Build a multi-tenant SaaS that can operate business-specific agents, store every agent action, manage sales pipeline data, generate websites/landing pages, track growth metrics, and provide live reports.

## High-Level Components

```text
Frontend Web App
Admin Dashboard
Merchant Dashboard
Agent Task Board
Website/Landing Page Renderer
API Backend
Agent Orchestrator
Job Queue
AI Service Gateway
Prospect Discovery Service
CRM/Sales Service
Quotation Service
Analytics Service
Notification Service
Database
Object Storage
Event Tracking
Monitoring/Logging
```

## Suggested Stack Direction

Frontend:
- Next.js
- Tailwind or component system
- PWA-ready for mobile owner/admin use

Backend:
- NestJS / Next.js API / Fastify
- PostgreSQL
- Redis + BullMQ or equivalent queue
- Object storage S3-compatible
- Worker services for agent runs

AI:
- AI gateway abstraction
- Prompt templates/versioning
- Guardrails and approval rules
- Usage metering per tenant

Analytics:
- Internal event tracking
- Website visitor tracking
- CTA click tracking
- Form lead tracking
- Search/SEO integration later

## Multi-Tenant Design

Every major table must include:

```text
tenant_id
created_at
updated_at
```

Core tenant relationship:

```text
tenants
  -> business_profiles
  -> products
  -> websites
  -> prospects
  -> leads
  -> tasks
  -> agent_runs
  -> quotations
  -> orders
  -> invoices
  -> analytics_events
```

## Core Entities

### tenants

```text
id
name
slug
owner_user_id
plan_id
status
created_at
updated_at
```

### users

```text
id
name
email
phone
role
created_at
updated_at
```

### business_profiles

```text
id
tenant_id
business_name
business_category
description
area_coverage
target_customers
value_proposition
capacity_notes
margin_assumptions
contact_whatsapp
contact_email
address
website_url
social_links
readiness_score
created_at
updated_at
```

### products

```text
id
tenant_id
name
category
description
price_type
base_price
estimated_margin
minimum_order
production_time
attributes_json
status
created_at
updated_at
```

### websites

```text
id
tenant_id
domain
subdomain
status
published_at
metadata_json
created_at
updated_at
```

### landing_pages

```text
id
tenant_id
website_id
title
slug
page_type
keyword_target
content_json
seo_json
status
published_url
created_at
updated_at
```

### prospects

```text
id
tenant_id
name
organization_type
location
contact_name
contact_email
contact_phone
source_type
source_url
source_notes
relevance_score
buying_signal
recommended_product_id
recommended_approach
consent_status
outreach_status
owner_notes
created_at
updated_at
```

### leads

```text
id
tenant_id
prospect_id nullable
customer_id nullable
source
source_detail
name
phone
email
message
product_interest
status
priority_score
last_contacted_at
next_followup_at
created_at
updated_at
```

### customers

```text
id
tenant_id
name
phone
email
company_name
address
segment
notes
created_at
updated_at
```

### agent_tasks

```text
id
tenant_id
agent_type
title
description
reason
expected_impact
required_owner_action
data_source_json
priority
status
due_date
needs_approval
approved_by
approved_at
executed_at
result_summary
result_data_json
created_at
updated_at
```

### agent_runs

```text
id
tenant_id
agent_type
trigger_type
trigger_ref
input_json
output_json
status
started_at
finished_at
error_message
cost_estimate
created_at
updated_at
```

### recommendations

```text
id
tenant_id
agent_run_id
agent_type
title
summary
recommendation_type
impact_area
confidence_score
evidence_json
status
created_at
updated_at
```

### outreach_templates

```text
id
tenant_id
channel
template_type
title
body
variables_json
compliance_notes
status
created_at
updated_at
```

### outreach_messages

```text
id
tenant_id
prospect_id nullable
lead_id nullable
customer_id nullable
channel
template_id
body
status
requires_approval
approved_by
approved_at
sent_at
response_status
opt_out_detected
created_at
updated_at
```

### quotations

```text
id
tenant_id
lead_id nullable
customer_id nullable
quotation_number
items_json
subtotal
discount
tax
total
gross_profit_estimate
terms
valid_until
status
sent_at
accepted_at
created_at
updated_at
```

### orders

```text
id
tenant_id
quotation_id nullable
customer_id
order_number
status
total_value
gross_profit_estimate
production_status
due_date
created_at
updated_at
```

### invoices

```text
id
tenant_id
order_id
invoice_number
total
paid_amount
payment_status
due_date
issued_at
created_at
updated_at
```

### payments

```text
id
tenant_id
invoice_id
amount
payment_method
paid_at
notes
created_at
updated_at
```

### analytics_events

```text
id
tenant_id
session_id
event_name
event_source
page_url
referrer
utm_source
utm_medium
utm_campaign
lead_id nullable
metadata_json
created_at
```

### pricing_usage_events

```text
id
tenant_id
usage_type
quantity
unit_cost_estimate
total_cost_estimate
metadata_json
created_at
```

### compliance_logs

```text
id
tenant_id
entity_type
entity_id
action
policy_reference
source_url
consent_status
notes
created_at
```

## Agent Orchestration

Agent execution flow:

```text
Trigger
→ Load tenant context
→ Load relevant business data
→ Apply playbook rules
→ Generate task/recommendation/draft
→ Check compliance rules
→ Store output
→ Notify owner if needed
→ Track cost and event
```

## Task Lifecycle

```text
pending
→ running
→ waiting_owner_approval
→ done
```

Alternative paths:

```text
running → failed
pending → cancelled
waiting_owner_approval → blocked
```

## Event Tracking Examples

```text
business_onboarded
website_generated
landing_page_published
cta_whatsapp_clicked
lead_created
prospect_created
prospect_validated
agent_task_created
agent_task_completed
outreach_draft_created
quotation_created
quotation_sent
deal_won
deal_lost
invoice_paid
```

## Live Report Data Sources

Live report should be generated from:

- agent_tasks
- agent_runs
- prospects
- leads
- outreach_messages
- quotations
- orders
- invoices
- analytics_events
- pricing_usage_events

## Cost Metering Requirement

Since pricing is not finalized, the system must track usage from the beginning:

```text
AI tokens/actions
prospect discovery runs
validated prospects
website page views
storage
emails/messages sent
worker execution time
support/manual validation minutes
```

Without cost metering, pricing cannot be calculated accurately.

## Security & Compliance Requirements

- Tenant isolation
- Role-based access control
- Audit logs
- Consent/opt-out tracking
- Source URL tracking for prospects
- Approval gates for outbound outreach
- Avoid storing unnecessary sensitive data
- Data retention rules

## Open Technical Questions

- Should generated websites be hosted as static pages, dynamic pages, or separate tenant deployments?
- Should prospect discovery use third-party APIs, manual research, partner data, or browser automation?
- Which CRM/WhatsApp/email integrations are required first?
- How to attribute deals to agent activity fairly?
- How to calculate per-tenant AI and infrastructure cost accurately?
