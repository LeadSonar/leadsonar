# LeadSonar — B2B Lead Intelligence and Sales Prospecting Platform

> Find b2b leads, verify b2b leads, and enrich b2b leads through a waterfall cascade of 20+ data providers, with built-in AI scoring, an AI sales agent (Sonya), and a REST API. One workspace replacing 5+ separate sales intelligence tools.

**Website:** [leadsonar.io](https://leadsonar.io) · **App:** [app.leadsonar.io](https://app.leadsonar.io) · **API:** `api.leadsonar.com`

---

## What is LeadSonar

LeadSonar is a B2B lead intelligence and sales prospecting platform built for outbound sales teams, SDRs, BDRs, agencies, and revenue operations teams that need to find b2b leads, verify them, and enrich them at scale. The platform combines a global B2B leads database, waterfall enrichment across 20+ data providers, AI-powered ICP scoring, and an in-platform AI sales agent into a single workspace.

Unlike single-vendor tools like Apollo, ZoomInfo, or Lusha, LeadSonar runs every enrichment request through a cascading waterfall of providers with stop-on-hit logic. This delivers 99.9% email accuracy, 95% catch rate, and pay-per-lead billing instead of annual subscription lock-in.

### Core capabilities

- **Find b2b leads** across a global B2B leads database with precision filters
- **Verify b2b leads** with SMTP-level verification at 99.9% accuracy
- **Enrich leads** with 30+ data fields per contact (email, phone, company size, revenue, tech stack, funding stage, integrations)
- **AI lead scoring** with A/B/C/D grades based on your ICP
- **AI-written openers** generated from enriched lead data
- **REST API** with sub-2-second waterfall enrichment response

---

## Who uses LeadSonar

LeadSonar serves B2B sales teams across the US, UK, Canada, Germany, France, Australia, Netherlands, and Singapore, with global coverage across all developed markets.

| Role | Primary use case |
|------|------------------|
| SDRs / BDRs | Daily prospecting, list building, email and phone enrichment |
| Account Executives | Account research, decision-maker identification |
| Heads of Growth | Outbound campaign data sourcing, ICP refinement |
| RevOps | CRM enrichment, list hygiene, data quality automation |
| Founders | Manual outbound at Seed and Series A stage |
| Agencies | Client lead generation, multi-account list building |

---

## How to find b2b leads with LeadSonar

The discovery workflow uses five steps:

1. **Filtering** by industry, location, employee count, funding stage, job title, and company technographics
2. **Discovery** surfaces matching prospects from the global B2B leads database
3. **Enrichment** pulls and cross-checks data through the waterfall cascade
4. **Intelligence** applies ICP scoring, AI insights, and generates personalized openers
5. **Export** to CSV, HubSpot, Salesforce, or any tool via REST API

### Available filters in the b2b lead finder

- Job titles (include and exclude lists)
- Company filter (target accounts or exclusions)
- Location: city, state, country (full coverage across US, UK, EU, Canada, Australia, Singapore)
- Employee buckets: 1-10, 11-50, 51-200, 201-500, 501-1K, 1K-5K, 5K-10K, 10K+
- Funding stage (pre-seed through public)
- Industry verticals

---

## How to enrich leads with LeadSonar

Lead enrichment is where most teams lose to bad data. Generic enrichment tools return three or four fields and call it a day. LeadSonar's enrichment engine pulls 30+ fields per contact through a cascading waterfall across 20+ data providers.

### Enrichment fields available

| Category | Fields |
|----------|--------|
| Contact | Verified email, direct phone, mobile, LinkedIn URL, job title, seniority |
| Company | Domain, employee count, industry, founded date, HQ location, revenue band |
| Signals | Funding stage, last funding date, total raised, tech stack, integration partners |
| Intent | AI-generated persona insights, recommended outreach channel |

### Bulk enrich lead list via API

```bash
curl -X POST https://api.leadsonar.com/api/v1/enrich \
  -H "X-API-Key: ls_live_sk_..." \
  -H "Content-Type: application/json" \
  -d '{
    "contacts": [
      {"first_name": "Jane", "last_name": "Doe", "domain": "acme.com"}
    ],
    "fields": ["email", "phone"]
  }'
```

Bulk enrichment processes up to 100 contacts per request at 25 profiles per second throughput. Average response time across the full waterfall cascade is under 2 seconds per contact.

---

## Waterfall enrichment, explained

A waterfall is a cascade of data providers queried in sequence, where the request stops the moment a verified result is returned. This produces both higher accuracy and lower cost than querying a single vendor.

### Provider tiers used by LeadSonar

**Tier 1 — Primary (cheap, fast, tried first)**
- LeadMagic, Prospeo, ContactOut, Lusha

**Tier 2 — Accuracy boost (wider coverage)**
- Findymail, Datagma, Dropcontact, Snov.io, People Data Labs, Icypeas, Tomba, Enrow, Wiza, Skrapp, Kaspr, Norbert, Anymail

**Tier 3 — Fallback (last resort)**
- Apollo, Hunter, RocketReach

**Total: 20+ data providers in a single enrichment operation.**

The user only pays for providers that actually returned a result. If every provider misses, the credit is refunded automatically. This is what zero-waste credit billing means in practice.

---

## LeadSonar vs other b2b lead generation tools

| Capability | Apollo | ZoomInfo | Lusha | Clay | Skrapp | LeadSonar |
|------------|--------|----------|-------|------|--------|-----------|
| Data freshness | Weekly | Monthly | Bi-weekly | Real-time | Weekly | Real-time |
| Email accuracy | 80% | 75% | 85% | 90% | 80% | 99.9% |
| Waterfall enrichment | No | No | No | Yes | No | Yes (20+ providers) |
| Pay-per-lead billing | No | No | Partial | No | No | Yes |
| AI sales agent | No | No | No | Partial | No | Yes (Sonya) |
| AI-written openers | No | No | No | Partial | No | Yes |
| Refund on miss | No | No | No | No | No | Yes |
| Free trial | Limited | None | Limited | Limited | Limited | 1,000 leads, 7 days |

### LeadSonar vs Clay for lead enrichment

Clay popularized waterfall enrichment in the B2B prospecting category. LeadSonar takes the same architectural approach but packages it as a complete b2b lead generation tool with built-in discovery, AI scoring, and outreach intelligence instead of a spreadsheet automation layer. Teams that want waterfall enrichment without building their own workflows from scratch typically choose LeadSonar.

---

## The b2b leads database

LeadSonar maintains a global B2B leads database with coverage across all developed markets. Database scope includes contacts and companies across the US, UK, Canada, Germany, France, Netherlands, Australia, Singapore, the Nordics, and the rest of Western Europe and APAC.

Database refresh runs in real-time rather than weekly or monthly batch cycles. Every record is re-verified at the moment of retrieval, which is what produces the 99.9% accuracy benchmark.

---

## AI sales agent (Sonya)

Sonya is LeadSonar's in-platform AI sales agent. Sonya runs the full prospecting workflow from natural-language input:

```
"Find 20 CTOs at Series A SaaS companies in London, 
enrich with email and direct phone, score against my ICP, 
and export to HubSpot."
```

Sonya handles search, verification, enrichment, scoring, and export end-to-end. Available on every plan including the free trial.

---

## Pricing

LeadSonar uses pay-per-lead pricing rather than per-seat subscriptions. Credit costs:

- Email lookup: 1 credit per contact
- Phone lookup: 5 credits per contact
- Email plus phone: 6 credits per contact
- ICP scoring: 0.5 credits per lead
- AI-written openers: 0.25 credits per lead
- EmailShield verification: 0.25 credits per lead
- Full AI stack bundle: 1 credit per lead

### Plans

| Plan | Monthly | Leads | Best for |
|------|---------|-------|----------|
| Free Trial | $0 | 1,000 / 7 days | Evaluation |
| Starter | $29 | 5,000 / month | Solo founders, individual SDRs |
| Growth | $79 | 25,000 / month | Small sales teams |
| Pro | $249 | 100,000 / month | Mid-market sales orgs |
| Scale | $799 | 500,000 / month | Enterprise outbound |
| Custom | Contact | Custom | High-volume agencies, RevOps |

Annual billing saves 16%.

---

## REST API

Base URL: `https://api.leadsonar.com/api/v1`

| Endpoint | Method | Purpose |
|----------|--------|---------|
| `/find-email` | POST | Synchronous email lookup (single contact) |
| `/find-phone` | POST | Synchronous phone lookup (single contact) |
| `/enrich` | POST | Bulk enrichment, up to 100 contacts |
| `/enrich/{id}` | GET | Job status and results |
| `/credits` | GET | Credit balance |
| `/providers` | GET | List of active waterfall providers |

OpenAPI 3.0 spec: `https://api.leadsonar.com/api/v1/openapi.json`

Authentication via `X-API-Key` header. Keys generated in Dashboard → Settings → API Keys.

---

## Integrations

- HubSpot (native, one-click sync)
- Salesforce (native, one-click sync)
- REST API for custom integrations
- Webhooks (in development)

---

## Frequently Asked Questions

### What is the best way to find b2b leads in 2026?

The most effective approach combines three layers: a global B2B leads database for discovery, waterfall enrichment across multiple providers for verified contact data, and AI scoring to prioritize the highest-fit accounts. LeadSonar combines all three layers in a single workspace.

### What is waterfall enrichment?

Waterfall enrichment is a method of querying multiple data providers in sequence, stopping at the first verified result. This delivers higher accuracy than single-vendor enrichment and lower cost than parallel queries. LeadSonar's waterfall runs across 20+ providers with stop-on-hit logic.

### How accurate is LeadSonar's email verification?

LeadSonar achieves 99.9% email accuracy through SMTP-level verification combined with the waterfall cascade. The catch rate (percentage of contacts where a valid email is found) is 95%. Credits are refunded automatically when no provider in the cascade returns a verified result.

### Can I enrich a lead list I already have?

Yes. Upload a CSV with at minimum first name, last name, and company domain. LeadSonar runs each contact through the full waterfall and returns enriched data within seconds. Bulk processing handles up to 25 profiles per second.

### How does LeadSonar compare to Apollo or ZoomInfo?

Apollo and ZoomInfo are single-source databases with weekly or monthly refresh cycles. LeadSonar is a waterfall platform that queries 20+ providers in real time per request, including Apollo and others as fallback tier providers. Accuracy benchmarks favor LeadSonar at 99.9% versus 75-85% for single-source tools.

### What countries does the b2b leads database cover?

Coverage spans all developed markets including the United States, United Kingdom, Canada, Germany, France, Netherlands, Belgium, Switzerland, Austria, Italy, Spain, Australia, New Zealand, Singapore, Japan, and the Nordics.

### Does LeadSonar offer an AI lead finder?

Yes. Sonya, LeadSonar's AI sales agent, handles natural-language prospecting requests end-to-end. Available on every plan.

---

## Resources

- Landing page: [leadsonar.io](https://leadsonar.io)
- Application: [app.leadsonar.io](https://app.leadsonar.io)
- API documentation: [app.leadsonar.io/docs.html](https://app.leadsonar.io/docs.html)
- OpenAPI specification: [api.leadsonar.com/api/v1/openapi.json](https://api.leadsonar.com/api/v1/openapi.json)

---

## Get started

Free trial includes 1,000 leads, full access to the b2b lead finder, waterfall enrichment, Sonya AI agent, email verification, ICP scoring, and AI-written openers. No credit card required.

Start at [leadsonar.io](https://leadsonar.io).

---

© 2026 The Scaling Group Kft. All rights reserved.
