# KPI & Success Metrics

## Status

Draft. Metrics must be validated with pilot merchants.

## Success Philosophy

The product should not only report vanity metrics such as website views, likes, or number of generated posts.

The main goal is to help UMKM create measurable sales opportunities and move those opportunities toward revenue.

## KPI Layers

### 1. Agent Activity Metrics

Purpose: prove that the agent is working.

Metrics:
- Tasks created
- Tasks completed
- Tasks in progress
- Tasks waiting for owner approval
- Tasks blocked
- Agent runs completed
- Recommendations generated
- Owner actions completed

Example dashboard:

```text
Today:
- 12 tasks created
- 7 completed
- 3 in progress
- 2 waiting owner approval
```

### 2. Prospect & Lead Metrics

Purpose: measure opportunity creation.

Metrics:
- Prospect candidates discovered
- Qualified prospects
- Prospect relevance score average
- Prospects by source
- Prospects by segment
- Leads captured
- Leads by source
- Leads waiting response
- Qualified leads

Important:
- Prospect discovered is not equal to lead.
- Qualified prospect must have a clear reason and source.

### 3. Website & Growth Metrics

Purpose: measure whether digital assets generate attention and action.

Metrics:
- Website visitors
- Landing page visitors
- Search impressions
- Search clicks
- Keyword movement
- CTA WhatsApp clicks
- Form submissions
- Conversion rate: visitor to CTA click
- Conversion rate: CTA click to lead
- Page speed/technical health
- Active visitors now
- Repeat visitors
- Live sessions
- Top landing pages
- Traffic by campaign/source
- Real-time CTA clicks
- Real-time conversion events

### 4. Real-Time Visitor Intelligence Metrics

Purpose: help owner see live business activity and conversion behavior.

Metrics:
- Current active visitors
- Current live sessions
- Most viewed pages today
- Most clicked CTA today
- Visitor path before conversion
- Returning visitor activity
- Device/browser distribution
- Campaign traffic spikes
- Traffic changes after optimization
- Visitor-to-lead conversion path

Example live feed:

```text
10:42 WIB
Visitor opened:
Paket Jersey Sekolah

10:43 WIB
Visitor clicked:
WhatsApp CTA

10:44 WIB
Visitor opened:
Contact Page

10:45 WIB
Lead submitted:
Quotation Request
```

Important:
- Focus on conversion visibility and growth monitoring.
- Avoid invasive personal tracking.
- Anonymous/pseudonymous analytics should be default.

### 5. Sales Funnel Metrics

Purpose: measure movement toward closing.

Metrics:
- New leads
- Leads contacted
- Follow-ups completed
- Response rate
- Quotation requests
- Quotations sent
- Quotation follow-ups completed
- Deals won
- Deals lost
- Lost reason
- Closing rate
- Average order value
- Pipeline value
- Revenue won
- Gross profit estimate

### 6. ROI & Break-Even Metrics

Purpose: answer owner question: is the subscription worth it?

Metrics:
- Monthly subscription cost
- Estimated gross profit from agent-assisted orders
- Agent-assisted pipeline value
- Break-even progress
- Cost per qualified lead
- Cost per quotation
- Cost per won deal
- ROI estimate

Break-even formula:

```text
break_even_orders = monthly_subscription_cost / average_gross_profit_per_order
```

ROI formula:

```text
roi = (agent_assisted_gross_profit - monthly_subscription_cost) / monthly_subscription_cost
```

Important:
- Use gross profit, not revenue, for break-even analysis.
- Separate confirmed revenue from estimated pipeline.
- Do not count all business revenue as agent-assisted revenue.

### 7. Capital Readiness Metrics

Purpose: help business become more credible for financing/investment.

Metrics:
- Business profile completeness
- Product catalog completeness
- Transaction record completeness
- Invoice/payment data availability
- Repeat customer evidence
- Legal document checklist
- Cashflow summary availability
- Profitability evidence
- Financing/investor one-pager completeness

## Suggested 90-Day Pilot Success Definition

For merchants that pass onboarding qualification and execute required playbook actions, a successful pilot may be defined as achieving measurable progress in at least two categories:

1. Sales opportunity creation
2. Follow-up/quotation execution
3. Pipeline/order growth
4. Break-even/ROI progress
5. Capital readiness improvement

Example 90-day targets for pilot validation:

```text
- Website/landing page live and tracked
- Minimum 3 valid landing/content pages created
- Minimum 100 prospect candidates discovered or imported
- Minimum 40 prospects validated/scored
- Minimum 25 outreach/follow-up tasks completed
- Minimum 10 quotations sent
- Pipeline value reaches a target multiple of subscription cost
- Gross profit from agent-assisted orders approaches or exceeds subscription cost
```

These numbers are placeholders and must be validated by vertical and merchant maturity.

## Dashboard Principles

Dashboard should answer:

1. What did the agent do today?
2. What opportunities were created?
3. What needs owner action?
4. What is closest to closing?
5. What sales value is in pipeline?
6. What revenue/gross profit is confirmed?
7. Is the merchant moving toward break-even?
8. What strategy should be changed next?
9. Which pages and campaigns are driving engagement?
10. What are visitors doing right now?

## Success Risk

The product cannot claim success only because tasks are completed.

A healthy system must connect:

```text
Agent Activity → Prospect/Lead Creation → Follow-up → Quotation → Order → Gross Profit → ROI
```

## Vanity Metrics to Avoid as Primary Success

- Number of AI posts generated
- Number of website pages created
- Number of tasks created without completion
- Number of raw scraped records
- Social likes without lead attribution
- Website visits without CTA/action tracking

## Primary North Star Candidates

Candidate 1:

```text
Agent-assisted gross profit per merchant per month
```

Candidate 2:

```text
Qualified sales opportunities created per merchant per month
```

Candidate 3:

```text
Merchant break-even achievement rate within 90 days
```

Recommended early-stage North Star:

```text
Qualified sales opportunities created and advanced per merchant per month
```

Reason:
- More controllable than final sales.
- Still closer to revenue than website/content metrics.
- Useful before large enough revenue data exists.
