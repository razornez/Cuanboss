# PRD Draft — AI UMKM Growth Agent OS

## Status

Draft. Product name and pricing are not finalized.

## Product Goal

Create a SaaS platform that helps UMKM owners grow sales opportunities through daily-working AI agents, visible execution, structured data, and measurable business outcomes.

## Primary User

UMKM owner/operator who needs more customers, better follow-up, better sales pipeline visibility, and practical daily growth direction.

## Key Jobs To Be Done

1. When I register my business, I want the system to understand my products, customers, area, margins, and capacity so it can recommend realistic growth actions.
2. When I do not have a strong website, I want the system to generate and maintain a simple sales-oriented website and landing pages.
3. When I need customers, I want the system to discover relevant prospect opportunities safely and explain why they are relevant.
4. When I am busy, I want the system to give me prioritized daily tasks so I know what to do next.
5. When leads come in, I want the system to track them, guide follow-up, and help me close.
6. When prospects ask for pricing, I want the system to help prepare quotations quickly.
7. When I want to know whether the system is working, I want live reports showing tasks, leads, prospects, follow-ups, pipeline, orders, ROI, and live visitor activity.
8. When I need capital, I want the system to help organize my business data and recommend readiness steps.

## Core Modules

### 1. Business Onboarding

Input:
- Business identity
- Products/services
- Area coverage
- Target customers
- Price/margin assumptions
- Production/service capacity
- WhatsApp/contact details
- Photos/portfolio/testimonials
- Existing website/social links

Output:
- Business profile
- Customer personas
- Positioning draft
- Product catalog
- Sales script draft
- FAQ draft
- Initial growth strategy
- Readiness score

### 2. Website & Landing Page Generator

Features:
- Generate homepage
- Generate product/service landing pages
- Generate location pages when valid
- Portfolio/case study pages
- FAQ section
- CTA WhatsApp tracking
- Lead capture form
- Analytics events
- SEO metadata
- Structured content plan

Important:
- Do not generate low-quality mass pages only for search manipulation.
- Pages must be based on real products, services, locations, photos, portfolio, and useful buyer information.

### 3. Prospect Discovery

Features:
- Discover relevant prospect opportunities from safe/public/compliant sources.
- Store source URL and data origin.
- Score relevance.
- Explain buying signal.
- Recommend product/service fit.
- Mark contact permission/consent status.
- Generate outreach task, not automatic spam.

Prospect quality fields:
- Prospect name
- Business/organization type
- Location
- Source
- Relevance score
- Buying signal
- Recommended product
- Suggested approach
- Consent/contact status
- Owner notes

### 4. Daily Agent Task Board

Task types:
- Setup task
- Sales task
- Marketing task
- Follow-up task
- Quotation task
- Capital readiness task
- IT/website task
- Strategy task

Task statuses:
- pending
- running
- waiting_owner_approval
- done
- failed
- blocked
- cancelled

Every task must include:
- Why this task matters
- Expected sales/business impact
- Required owner action
- Data source/evidence
- Deadline/priority
- Result after completion

### 5. Sales CRM & Pipeline

Features:
- Lead capture from website/WhatsApp/form/manual input
- Source tracking
- Lead status
- Follow-up reminders
- Notes/activity log
- Quotation status
- Deal status
- Lost reason
- Customer history

Suggested pipeline:
- New lead
- Qualified
- Need info
- Quotation needed
- Quotation sent
- Follow-up
- Negotiation
- Won
- Lost
- Repeat/nurture

### 6. Outreach Assistant

Features:
- Generate contextual message drafts
- Generate email drafts
- Generate WhatsApp templates for inbound/opt-in/customer context
- Generate call scripts
- Generate follow-up sequence
- Require owner approval before outbound outreach
- Track opt-out/consent where applicable

### 7. Quotation & Offer Assistant

Features:
- Product/package selection
- Quantity
- Price estimation
- Terms and conditions
- DP/payment terms
- Validity period
- PDF/export/share link
- Follow-up reminder after quotation sent

### 8. Live Report Dashboard

Owner should see:
- What the agent did today
- Tasks completed/in progress/blocked
- Prospects discovered
- Qualified prospects
- Leads captured
- Follow-ups due
- Quotations sent
- Pipeline value
- Deals won/lost
- Website visitor trend
- WhatsApp CTA clicks
- Break-even/ROI estimate
- Capital readiness progress
- Live visitor activity and conversion flow

### 8A. Live Visitor Intelligence & Conversion Monitoring

Purpose:
- Show the direct impact of website, landing page, campaign, and agent activity in real time.
- Make the business feel alive and measurable.

Live activity examples:
- Visitor opened product landing page
- Visitor clicked WhatsApp CTA
- Visitor viewed contact page
- Returning visitor revisited portfolio page
- Visitor submitted inquiry form

Tracked events:
- page_view
- session_start
- CTA_click
- WhatsApp_click
- form_submit
- quotation_request
- repeat_visit
- campaign_visit

Suggested event fields:
- timestamp
- page_url
- referrer
- campaign_source
- device_type
- browser
- operating_system
- city/country
- anonymous_visitor_id
- session_id
- tenant_id

Important:
- Focus on business intelligence and conversion visibility.
- Default tracking should be anonymous/pseudonymous.
- Do not become invasive surveillance or spyware.
- Avoid sensitive personal data collection.

### 9. Capital Readiness Agent

Features:
- Business profile completeness
- Revenue/transaction record checklist
- Invoice/payment data checklist
- Customer repeat order evidence
- Legal document checklist
- Cashflow summary
- Funding option research tasks
- Investor/financing one-pager draft

Important:
- Do not promise funding approval.
- The system helps improve readiness and organize evidence.

## MVP Scope

MVP should focus on visible daily work and sales opportunity creation.

MVP includes:
1. Business onboarding
2. Product catalog
3. Website/landing page draft generator
4. Agent task board
5. Prospect database
6. Manual/semi-automated prospect discovery workflow
7. Outreach draft generator
8. CRM lead pipeline
9. Quotation draft
10. Live report dashboard
11. KPI tracking
12. Real-time visitor analytics
13. CTA and conversion event tracking

MVP excludes:
- Fully automated cold WhatsApp blasting
- Fully autonomous investor outreach
- Deep ERP/inventory
- Complex accounting
- Native mobile app
- Automated mass scraping without compliance review

## Acceptance Criteria

A pilot merchant is considered successfully onboarded when:

- Business profile completed
- At least 1 website/homepage draft created
- At least 3 valid landing/content pages created or drafted
- At least 20 prospect candidates generated or imported
- At least 10 prospects validated/scored
- At least 10 daily tasks created with reasons and expected impact
- At least 5 follow-up/outreach drafts created
- At least 1 quotation workflow tested
- Dashboard shows tasks, prospects, leads, pipeline, and live visitor activity

## Key Open Questions

- Which vertical should be the first pilot segment?
- What prospect sources are legally safe and practically valuable?
- What level of human validation is needed for prospect quality?
- What is the true cost per tenant per month?
- What pricing tiers are profitable and still ROI-positive for merchants?
- Which tasks should be automated vs owner-approved?
- Which integrations are required for MVP?
