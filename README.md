# Missive (missive)

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
