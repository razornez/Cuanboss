# Compliance & Risk Plan

## Status

Draft. Must be reviewed before implementation.

## Principle

The product must help UMKM create opportunities without becoming a spam engine or violating platform/data rules.

## Core Risks

### 1. Scraping Risk

Risk:
- Automated scraping can violate website/platform terms.
- Search engine automated queries can be restricted.
- Social platforms may ban accounts or block access.
- Data quality can be poor or outdated.

Mitigation:
- Prefer official APIs, public directories with allowed usage, partner datasets, user-provided data, inbound leads, and manually validated sources.
- Store source URL and collection method.
- Add data provenance to every prospect.
- Avoid high-volume scraping without legal review.
- Apply rate limits.
- Use human validation for higher-risk sources.

### 2. Personal Data Risk

Risk:
- Collecting names, phone numbers, emails, and business contact data may create personal data obligations.
- Detailed visitor/session tracking may create privacy concerns.

Mitigation:
- Collect minimum required data.
- Store consent/contact status.
- Store source and purpose.
- Support opt-out/delete request workflows.
- Avoid sensitive personal data.
- Create data retention policies.
- Separate business/organization data from personal data when possible.
- Default analytics tracking to anonymous/pseudonymous identifiers.
- Avoid invasive fingerprinting.
- Avoid surveillance-style monitoring.

### 3. Outreach Spam Risk

Risk:
- Cold WhatsApp blasting can violate platform rules and damage merchant reputation.
- Irrelevant outreach reduces trust and may trigger complaints.

Mitigation:
- Default cold outreach to `draft_for_approval` or `guide_only`.
- Prioritize inbound, customer lama, referral, and opt-in contacts.
- For outbound cold B2B email, require contextual relevance, identity clarity, and opt-out.
- Track message frequency.
- Store opt-out status.
- Never hide sender identity.

### 4. False Promise Risk

Risk:
- Claiming guaranteed sales may create trust, legal, and refund issues.

Mitigation:
- Do not promise guaranteed orders for all merchants.
- Define success through measurable activity, pipeline, and ROI progress.
- Use qualification gates before any performance guarantee.
- Clearly separate pipeline estimate from confirmed revenue.
- Use transparent attribution.

### 5. Prospect Quality Risk

Risk:
- Agent may generate irrelevant prospects.
- Owner may waste time on low-quality leads.

Mitigation:
- Require relevance reason.
- Require source and buying signal.
- Allow owner feedback to train/re-rank prospect scoring.
- Use validation stage before outreach.
- Track conversion by source.

### 6. AI Hallucination Risk

Risk:
- AI may invent facts, prices, guarantees, business claims, or prospect details.

Mitigation:
- Separate facts from generated suggestions.
- Require source-backed prospect data.
- Require owner approval for outbound messages.
- Use templates with allowed claims.
- Restrict AI from inventing prices without business rules.

### 7. Pricing/Cost Risk

Risk:
- The product may become expensive to operate due to AI, prospect discovery, support, hosting, or real-time analytics cost.

Mitigation:
- Track usage cost per tenant from day one.
- Set plan limits.
- Add fair usage policies.
- Separate self-service from managed service.
- Recalculate pricing after pilot data.
- Track analytics event ingestion/storage cost.

### 8. Support/Onboarding Risk

Risk:
- UMKM may need heavy onboarding, making low-cost pricing unprofitable.

Mitigation:
- Create onboarding templates by industry.
- Use guided setup.
- Offer managed onboarding as separate tier/add-on.
- Track support minutes per merchant.

## Compliance Features Required

### Prospect Data Provenance

Every prospect must store:

```text
source_type
source_url
collection_method
created_at
relevance_reason
consent_status
```

### Consent & Outreach Status

Recommended statuses:

```text
unknown
public_business_contact
inbound_opt_in
existing_customer
referral
opted_out
do_not_contact
```

### Outreach Approval Gate

Cold or semi-cold outreach must require:

```text
owner approval
message preview
contact source
reason for relevance
frequency check
opt-out handling
```

### Message Safety Checklist

Every outbound message draft should:

- Identify the business clearly.
- Explain why the recipient is being contacted.
- Be relevant to the recipient context.
- Avoid misleading claims.
- Avoid pressure/manipulation.
- Include a polite way to stop receiving messages when appropriate.

### Analytics & Visitor Tracking Rules

Real-time analytics and visitor intelligence features must:

- Focus on business intelligence and conversion visibility.
- Avoid invasive surveillance behavior.
- Avoid aggressive browser/device fingerprinting.
- Avoid storing sensitive personal information without consent.
- Use anonymous or pseudonymous identifiers by default.
- Clearly separate analytics events from personal lead/customer data.
- Respect applicable privacy and retention requirements.

## Allowed/Preferred Prospect Sources

Preferred:
- Inbound website leads
- Existing customers
- Customer referrals
- Public business directories with allowed use
- Official event/tender/RFQ pages
- Business websites with public contact details
- User-uploaded customer/prospect lists with permission
- Partner data sources with legal agreement

Use caution:
- Social media public pages
- Search engine results
- Community/group data
- Marketplace data
- Contact enrichment providers

Avoid:
- Mass cold WhatsApp blasting
- Sensitive personal data collection
- Hidden identity outreach
- Automated collection from sites that prohibit it
- Scraping behind login or access controls

## Guarantee Risk Control

Any guarantee must be conditional.

Possible conditions:

- Merchant passes business readiness audit.
- Merchant provides accurate product/pricing data.
- Merchant responds within agreed SLA.
- Merchant approves and executes required tasks.
- Merchant tracks outcomes honestly.
- Product/service quality and capacity are sufficient.
- Pricing is not far outside market reality.

Guarantee should be based on:

- Measurable activity
- Pipeline progress
- Quotation/follow-up execution
- Break-even progress

Not unconditional revenue promises.

## Open Legal/Compliance Research

- Indonesian personal data protection obligations for B2B prospect data.
- Platform-specific rules for WhatsApp, Instagram, Facebook, TikTok, Google, LinkedIn.
- Email outreach rules and opt-out standards in target markets.
- Data retention and deletion requirements.
- Liability language for AI-generated business recommendations.
- Analytics/privacy obligations for visitor tracking and live activity monitoring.
