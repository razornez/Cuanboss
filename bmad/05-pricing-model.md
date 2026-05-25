# Pricing Model Framework

## Status

Draft. Pricing is intentionally not fixed.

## Principle

Do not set the subscription price based only on a nice round number.

Final pricing must consider:

1. Cost to serve each merchant.
2. Usage limits.
3. Support/onboarding cost.
4. Human validation/managed service cost.
5. AI/token cost.
6. Infrastructure cost.
7. Compliance and data quality cost.
8. Gross margin target.
9. Merchant ROI and willingness to pay.
10. Competitive alternatives.

## Pricing Must Answer

For the business:

```text
Can this merchant realistically get more value than the subscription cost?
```

For the SaaS company:

```text
Can we serve this merchant profitably at the selected price?
```

## Cost Components

### 1. Fixed Platform Cost

Examples:
- Application hosting
- Database server
- Redis/queue infrastructure
- Object storage
- Logging/monitoring
- CI/CD
- Domain/DNS/email infrastructure
- Security tools

### 2. Variable Cost Per Merchant

Examples:
- AI model/token usage
- Website generation and updates
- Search/prospect discovery runs
- Storage for product images/documents
- Email sending
- WhatsApp/API integration
- Analytics event volume
- Queue/job execution
- Support tickets
- Onboarding sessions
- Human validation/research labor

### 3. Feature-Specific Cost

Examples:
- Prospect discovery cost per run
- AI content generation cost per item
- AI strategy analysis cost per report
- Quotation PDF generation/storage
- Website bandwidth
- Capital readiness report generation
- CRM activity volume

## Unit Economics Formula

```text
monthly_price >= (fixed_cost_allocation + variable_cost_per_merchant + support_cost + risk_buffer) / target_cost_ratio
```

Alternative gross margin formula:

```text
price = total_cost_per_merchant / (1 - target_gross_margin)
```

Example:

```text
If total monthly cost per merchant = 250,000 IDR
Target gross margin = 70%
Required price = 250,000 / (1 - 0.70) = 833,333 IDR
```

This is only an example. Real data must be collected.

## Merchant ROI Formula

Break-even orders:

```text
break_even_orders = monthly_subscription_cost / average_gross_profit_per_order
```

Merchant ROI:

```text
merchant_roi = (agent_assisted_gross_profit - monthly_subscription_cost) / monthly_subscription_cost
```

Important:
- Use gross profit, not revenue.
- Pricing should be easier to justify when average gross profit per order is high.
- Low-margin merchants may need lower-tier plans or performance-based pricing.

## Pricing Research Inputs Needed

For each target segment:

```text
average_order_value
average_gross_margin
average_monthly_order_count
average_ad_spend
average_lead_volume
average_close_rate
owner willingness to pay
support intensity
AI/prospect usage intensity
```

## Possible Pricing Structure

Pricing tiers should be calculated later, but likely dimensions include:

### Starter

For businesses that need basic website, CRM, and guided tasks.

Possible limits:
- Limited products
- Limited landing pages
- Limited AI actions
- Manual prospect import
- Basic CRM
- Basic dashboard

### Growth

For businesses that want active prospect discovery and daily growth tasks.

Possible limits:
- More landing pages
- Prospect discovery quota
- More AI strategy reports
- Follow-up assistant
- Quotation builder
- Live report

### Managed / Assisted Growth

For businesses that need hands-on help.

Possible inclusions:
- Human-assisted onboarding
- Human prospect validation
- Campaign setup support
- Monthly/weekly growth review
- More advanced reporting
- Higher support SLA

### Performance Add-On

Potential model:

```text
base subscription + success fee for verified agent-assisted deals
```

Requires strong attribution logic and clear contract terms.

## Pricing Variables To Model

```text
number_of_products
number_of_websites
number_of_landing_pages
monthly_ai_actions
monthly_prospect_discovery_runs
monthly_validated_prospects
monthly_email_outreach_drafts
monthly_whatsapp_followup_drafts
monthly_quotations
monthly_storage_gb
monthly_page_views
support_level
human_validation_minutes
managed_service_minutes
```

## Guardrails

- Do not promise enterprise-level managed service at low self-service pricing.
- Do not include unlimited AI/prospect discovery without cost controls.
- Do not set price before understanding support and AI cost.
- Do not price below cost just to attract users unless it is an intentional pilot subsidy.
- Do not use one price for all UMKM verticals if cost-to-serve and ROI differ greatly.

## Pricing Validation Plan

1. Interview 10–20 UMKM owners across 3 verticals.
2. Ask current ad spend, lead volume, closing rate, gross margin, and software spend.
3. Estimate break-even orders per possible price tier.
4. Run pilot with manual cost tracking.
5. Calculate true cost per merchant.
6. Compare merchant value generated vs subscription cost.
7. Adjust tier limits and onboarding support.
8. Define guarantee only after pilot evidence exists.

## Output Needed Before Final Pricing

- Cost model spreadsheet
- Usage assumptions by tier
- Merchant ROI calculator
- Pilot cost report
- Support effort report
- Pricing page draft
- Terms for guarantee/performance claims
