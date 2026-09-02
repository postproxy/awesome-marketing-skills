---
name: bulkpublish-publisher
description: Prepare, review, schedule, and publish approved social content through BulkPublish.
version: 1.0.0
---

# BulkPublish Publisher

Use this skill when an AI agent needs to move approved marketing content from a draft into a multi-platform social publishing workflow through BulkPublish.

## Before writing

Collect the source content, canonical URL, audience, brand voice, target platforms, channel IDs, media, timezone, and requested action. Distinguish clearly between creating a draft, scheduling, and publishing. Scheduling and publishing are external write actions.

Read the current [BulkPublish API documentation](https://app.bulkpublish.com/docs). The canonical [BulkPublish social-media-content-skills](https://github.com/azeemkafridi/bulkpublish-api/tree/main/skills/social-media-content-skills) collection provides related planning, adaptation, preflight, and review workflows.

## Workflow

1. Check channel health, quota, media constraints, platform limits, and required approvals.
2. Create a platform-specific variant for each selected channel. Keep claims traceable to the source and preserve required disclosures.
3. Show the final copy, destinations, media, and schedule to the user for explicit approval.
4. After approval, use the BulkPublish MCP server when available, or the REST API documented at `https://app.bulkpublish.com/docs`.
5. Use a stable idempotency key. If only some platforms fail, report per-platform results and retry failed items only.
6. Return post IDs, statuses, timestamps, and any required follow-up actions.

## Safety

- Never reveal API keys or place credentials in files, logs, or output.
- Never publish or schedule without explicit approval of the exact destinations and timing.
- Do not automate spam, fake engagement, unsolicited messaging, or deceptive reviews.
- Do not bypass CAPTCHAs, rate limits, platform restrictions, or interactive human-verification steps.
- Ask the user to complete CAPTCHA or login steps when required.
