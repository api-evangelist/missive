# Missive (missive)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Missive is a team inbox and collaboration platform that brings email, SMS, WhatsApp, Instagram, Facebook Messenger, and live chat into one unified workspace. It provides a REST API for managing conversations, messages, contacts, labels, drafts, analytics, and automation rules, enabling teams to integrate Missive into business workflows. The API supports webhooks for real-time event notifications, custom channels for integrating external communication sources, and UI/iFrame integrations via JavaScript.

APIs.json: https://raw.githubusercontent.com/api-evangelist/missive/refs/heads/main/apis.yml

Naftiko: https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=missive-api-evangelist&utm_content=repo

## Tags

- Team Inbox
- Collaboration
- Email
- Messaging
- Conversations
- Contacts
- Webhooks
- Automation
- REST API

## APIs

### Missive REST API

The Missive REST API allows developers to manage conversations, messages, contacts, drafts, labels, and analytics programmatically. Authentication uses Bearer tokens (personal access tokens with `missive_pat-` prefix) generated in Missive preferences under the API tab. The base URL is `https://public.missiveapp.com/v1/` and API access requires a Productive plan or higher subscription.

- Documentation: https://missiveapp.com/docs/developers/rest-api
- Endpoints: https://missiveapp.com/docs/developers/rest-api/endpoints
- Base URL: https://public.missiveapp.com/v1/

**Available Endpoints:**
- Analytics: POST/GET `/v1/analytics/reports`
- Contacts: POST/PATCH/GET `/v1/contacts`, GET `/v1/contact_books`, GET `/v1/contact_groups`
- Conversations: GET/PATCH `/v1/conversations/:id`, POST `/v1/conversations/:id/merge`
- Conversation content: GET messages, comments, drafts, posts per conversation
- Drafts: POST/DELETE `/v1/drafts`
- Messages: POST `/v1/messages` (custom channels)

## Plans, Rate Limits, and FinOps

### Plans

Missive offers three paid plans with a 20% discount for annual billing. API access requires the Productive plan or above. All plans include a 30-day free trial with no credit card required.

| Plan | Monthly Price | Annual Price | Users | API Access |
|------|--------------|--------------|-------|------------|
| Starter | $14/user/mo | $11.20/user/mo | Up to 5 | No |
| Productive | $24/user/mo | $19.20/user/mo | Up to 50 | Yes |
| Business | $36/user/mo | $28.80/user/mo | Unlimited | Yes |

Full plans detail: [plans/missive-plans-pricing.yml](plans/missive-plans-pricing.yml)

### Rate Limits

The Missive API enforces the following rate limits per API token:

| Limit Type | Limit |
|-----------|-------|
| Concurrent requests | 5 simultaneous |
| Requests per minute | 300 |
| Requests per 15 minutes | 900 |

HTTP 429 Too Many Requests is returned when any limit is exceeded.

Full rate limits detail: [rate-limits/missive-rate-limits.yml](rate-limits/missive-rate-limits.yml)

### FinOps

Cost optimization opportunities include:
- Annual billing saves 20% across all plan tiers
- Teams not requiring API access can use Starter ($14) instead of Productive ($24), saving $10/user/month
- Regular audit of API token holders to right-size plan assignments

Full FinOps detail: [finops/missive-finops.yml](finops/missive-finops.yml)

## Timestamps

- Created: 2026-06-12
- Modified: 2026-06-12

## Common

| Type | URL |
|------|-----|
| Website | https://missiveapp.com |
| Documentation | https://missiveapp.com/docs/developers/ |
| GitHub Org | https://github.com/missive |
| LinkedIn | https://www.linkedin.com/company/missive-app |
| Blog | https://missiveapp.com/blog |
| Pricing | https://missiveapp.com/pricing |
| Status Page | https://status.missiveapp.com/ |
| X (Twitter) | https://twitter.com/missiveapp |

## Maintainers

- Kin Lane (kin@apievangelist.com)
