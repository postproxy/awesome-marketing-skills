---
name: email-flows
description: When the user wants to create email sequences, drip campaigns, automated email flows, or nurture campaigns. Also use when the user mentions "welcome email", "onboarding emails", "email sequence", "drip campaign", "email automation", "nurture sequence", "re-engagement emails", or "email flow."
version: 1.0.0
---

# Email Flow Builder

Design automated email sequences that onboard, nurture, convert, and re-engage — with specific copy and timing for each email.

## Before You Start

**Check for product marketing context first:**
If `.claude/product-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered.

## Phase 1: Information Gathering

Collect context by asking the user focused questions in batches of 2-3.

### Required Context

1. **What's this email flow for?** — Use `AskUserQuestion` with options:
   - Welcome sequence (new signups)
   - Onboarding sequence (new product users)
   - Lead nurture (pre-sale education)
   - Re-engagement (win back inactive users)
   - Upgrade / upsell sequence
   - Post-purchase follow-up
   - Event-triggered (abandoned cart, feature usage, etc.)

2. **Product/service context** — Ask: "What's your product or service? What problem does it solve and for whom?"

3. **Audience for this flow** — Ask: "Who enters this email flow? Describe them — what do they know, what do they want, what stage are they in?"

4. **Desired outcome** — Ask: "What's the #1 action you want people to take by the end of this sequence? (e.g., activate the product, book a demo, upgrade to paid, come back)"

5. **Aha moment** — Ask: "What's the 'aha moment' for your product — the point where users realize the value? (e.g., 'sent their first invoice', 'connected their first integration', 'saw their first analytics report')"

6. **Brand voice** — Use `AskUserQuestion` with options:
   - Professional and polished
   - Casual and friendly
   - Bold and direct
   - Warm and supportive
   - Technical and precise

7. **Current state** — Ask: "Do you have any existing emails or sequences? What's working or not working? What email tool do you use? (e.g., Mailchimp, Customer.io, ConvertKit, SendGrid)"

8. **Sequence length preference** — Use `AskUserQuestion` with options:
   - Short (3-4 emails)
   - Medium (5-7 emails)
   - Long (8+ emails)
   - Not sure — recommend based on the flow type

## Phase 2: Sequence Design

Based on the flow type and context, design the full email sequence.

### For Each Email, Specify:

1. **Email #** and **Subject line** (with 1 alternative subject)
2. **Send timing** — when it sends relative to trigger or previous email
3. **Goal** — the single purpose of this email
4. **Preview text** — the snippet shown in inbox
5. **Body copy** — full email content, written in the specified voice
6. **CTA** — primary call to action (button text + destination)
7. **Trigger/condition** — any behavioral conditions (e.g., "only send if user hasn't activated")

### Timing Guidelines

| Flow Type | Email 1 | Early Spacing | Later Spacing |
|-----------|---------|---------------|---------------|
| Welcome | Immediately | 1-2 days | 3-4 days |
| Onboarding | Immediately | 1 day | 2-3 days |
| Lead nurture | Immediately | 2-3 days | 4-7 days |
| Re-engagement | After inactivity trigger | 3-4 days | 7 days |
| Upgrade | After usage trigger | 2-3 days | 5-7 days |

### Copy Guidelines

- **One email, one job** — single purpose and CTA per email
- Short paragraphs (1-3 sentences) with white space
- Mobile-first formatting
- 50-125 words for transactional, 150-300 for educational, up to 500 for narrative
- Subject lines: 40-60 characters, clarity over cleverness

## Phase 3: Deliverables

Generate and save:

1. **`email-flow-[type].md`** — Complete sequence document with all emails, subject lines, body copy, timing, and conditions

Present a summary and suggest next steps (e.g., "Use /split-test to A/B test subject lines" or "Use /marketing-copy to create alternative versions").

## Guidelines

- Every email should deliver value, not just ask for something
- The first email sets expectations — tell people what's coming
- Use behavioral triggers where possible (action-based > time-based)
- Always include an unsubscribe path and respect email preferences
- Test subject lines — they're the highest-leverage element

## User Request

$ARGUMENTS
