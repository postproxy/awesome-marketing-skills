---
name: product-context
description: When the user wants to create or update their product marketing context document. Also use when the user mentions "product context", "marketing context", "positioning", "messaging foundation", "who is my audience", "brand voice", "ideal customer profile", or "product marketing." This skill creates the foundational document that all other marketing skills reference.
version: 1.0.0
---

# Product Context Builder

Create and maintain `.claude/product-context.md` — the foundational document that captures your product's positioning, audience, messaging, and voice. All other marketing skills reference this file automatically, so you only describe your product once.

## Before You Start

Check if `.claude/product-context.md` already exists.

- **If it exists:** Read it, present a summary, and ask which sections the user wants to update or expand. Don't redo what's already solid.
- **If it doesn't exist:** Offer two paths using `AskUserQuestion`:
  - **Auto-draft from codebase (Recommended)** — Scan README, landing pages, package.json, marketing copy, and any docs to draft a V1 the user refines
  - **Build from scratch** — Walk through each section conversationally

## Phase 1: Information Gathering

Gather information across 12 sections. Ask questions in batches of 2-3 to avoid overwhelming the user. Use `AskUserQuestion` for structured choices and open-ended questions for descriptive fields.

**Important:** Push for specificity and exact customer language. When answers are vague, ask "Can you give me a specific example?" or "How would your customer describe this?" Polished marketing language is less useful here than real words customers use.

Skip sections that don't apply (e.g., Personas for a B2C product, Switching Dynamics for a brand-new category).

---

### Section 1: Product Overview

1. **One-liner** — Ask: "Describe your product in one sentence — what it does, for whom, and the key benefit. (e.g., 'Notion is an all-in-one workspace for notes, tasks, and docs aimed at teams who want to consolidate tools')"

2. **Category** — Use `AskUserQuestion` with options:
   - SaaS / Software tool
   - API / Developer tool
   - Marketplace / Platform
   - Agency / Service
   - Physical product
   - Content / Media / Education

3. **Pricing model** — Use `AskUserQuestion` with options:
   - Free
   - Freemium (free tier + paid)
   - Free trial → paid
   - Paid only
   - Usage-based
   - Enterprise / custom pricing

4. **Current stage** — Use `AskUserQuestion` with options:
   - Pre-launch / building
   - Just launched (< 6 months)
   - Growing (6 months - 2 years)
   - Established (2+ years)

---

### Section 2: Target Audience

1. **Ideal customer** — Ask: "Describe your ideal customer. If B2B: company size, industry, stage. If B2C: demographics, lifestyle, situation."

2. **Primary use case** — Ask: "What's the #1 thing your best customers use your product for? What job does it do for them?"

3. **How they find you** — Ask: "How do your best customers typically discover your product? (e.g., Google search, word of mouth, social media, communities, ads)"

4. **Decision process** — Ask: "What does the buying/signup process look like? Is it a quick individual decision or a team/approval process?"

---

### Section 3: Personas (B2B — skip for B2C)

Ask: "In your buyer's organization, who are the key people involved? Describe as many as apply:"

1. **End user** — Who uses the product day-to-day? What's their role and what do they care about?
2. **Champion** — Who advocates internally for buying your product? What motivates them?
3. **Decision maker** — Who has final say? What do they need to approve?
4. **Financial buyer** — Who controls the budget? What metrics matter to them?
5. **Technical influencer** — Who evaluates the technical fit? What concerns do they have?

---

### Section 4: Problems & Pain Points

1. **Core problem** — Ask: "What's the #1 problem your product solves? Describe it the way your customers would describe it — in their words, not marketing language."

2. **Current alternatives** — Ask: "What are people doing today instead of using your product? (e.g., spreadsheets, a competitor, manual process, nothing)"

3. **Why alternatives fail** — Ask: "What's broken or frustrating about those alternatives? Why aren't they good enough?"

4. **Cost of the problem** — Ask: "What does this problem cost people? (time, money, missed opportunities, frustration — be specific if you can)"

5. **Emotional tension** — Ask: "How do people feel about this problem? (e.g., frustrated, overwhelmed, embarrassed, anxious, stuck)"

---

### Section 5: Competitive Landscape

1. **Direct competitors** — Ask: "Who are your top 2-3 direct competitors — products that solve the same problem for the same audience?"

2. **How they position** — Ask: "How do these competitors position themselves? What do they emphasize?"

3. **Where they fall short** — Ask: "Where do competitors fall short? What do their customers complain about? (Check G2, Capterra, Reddit, Twitter if unsure)"

4. **Indirect competitors** — Ask: "What indirect alternatives exist? (e.g., hiring someone, building in-house, using a general-purpose tool like Excel/Notion)"

---

### Section 6: Differentiation

1. **Key differentiators** — Ask: "What are your top 3 things that make you different from alternatives? Be specific — not 'better UX' but 'set up in 5 minutes without engineering help.'"

2. **Why it matters** — Ask: "For each differentiator, why does your customer care? What does it enable them to do?"

3. **Unfair advantage** — Ask: "Do you have anything that's genuinely hard to copy? (e.g., proprietary data, network effects, unique expertise, integrations, community)"

---

### Section 7: Objections & Anti-Personas

1. **Top objections** — Ask: "What are the top 3 reasons people say no or hesitate? (e.g., 'too expensive', 'we already have a tool', 'seems complicated', 'not sure it'll work for us')"

2. **Objection responses** — For each objection, ask: "How do you typically respond to this objection? What evidence or argument works?"

3. **Anti-personas** — Ask: "Who is NOT a good fit for your product? Who should you not waste time marketing to?"

---

### Section 8: Switching Dynamics (JTBD Four Forces)

Explain: "Think about what drives someone to switch from their current solution to yours. There are four forces at play:"

1. **Push** — Ask: "What's pushing people away from their current solution? What's the breaking point?"

2. **Pull** — Ask: "What's pulling them toward your product? What's the attractive vision of the future?"

3. **Habit** — Ask: "What habits keep them stuck on their current solution? (e.g., 'we've always done it this way', sunk cost, team familiarity)"

4. **Anxiety** — Ask: "What anxieties make them hesitate to switch? (e.g., migration pain, learning curve, 'what if it doesn't work?')"

---

### Section 9: Customer Language

This section is critical — it powers all copy across other skills.

1. **Problem language** — Ask: "How do your customers describe the problem in their own words? Share exact quotes from calls, support tickets, reviews, or surveys if you have them."

2. **Solution language** — Ask: "How do customers describe the value they get from your product? What words do they use? (e.g., 'it just works', 'saves me hours every week', 'finally I can see everything in one place')"

3. **Words to use** — Ask: "Are there specific words or phrases that resonate with your audience? Industry terms they use?"

4. **Words to avoid** — Ask: "Any words or phrases that don't land well, feel too corporate, or don't match your audience? (e.g., 'synergy', 'leverage', 'disrupt')"

---

### Section 10: Brand Voice

1. **Voice attributes** — Use `AskUserQuestion` with multiSelect:
   - Professional
   - Casual
   - Bold / Confident
   - Warm / Friendly
   - Witty / Playful
   - Technical / Precise
   - Minimalist / Clean
   - Provocative / Edgy

2. **Voice description** — Ask: "If your brand were a person, how would they talk? Give an example of how you'd explain your product at a dinner party."

3. **Brands you admire** — Ask: "Name 2-3 brands whose tone or communication style you admire (they don't have to be in your industry)."

---

### Section 11: Proof Points

1. **Key metrics** — Ask: "What numbers tell your product's story? (e.g., users, revenue saved, time saved, uptime, NPS, growth rate)"

2. **Notable customers** — Ask: "Any recognizable companies or people using your product? Logos you can display?"

3. **Testimonials** — Ask: "Share your best 2-3 customer quotes — the ones that make prospects say 'that's exactly what I need.'"

4. **Case studies** — Ask: "Do you have any before/after stories? (e.g., 'Company X reduced churn by 30% in 3 months')"

---

### Section 12: Goals & Metrics

1. **Business goal** — Use `AskUserQuestion` with options:
   - Grow revenue
   - Increase signups / users
   - Reduce churn
   - Enter a new market
   - Launch a new product
   - Build brand awareness

2. **Primary conversion action** — Ask: "What's the main action you want marketing to drive? (e.g., free trial signup, demo request, purchase, waitlist)"

3. **Current metrics** — Ask: "Share what you know: monthly traffic, conversion rate, MRR/ARR, churn rate, CAC, LTV. (Skip what you don't track yet)"

---

## Phase 2: Document Assembly

After gathering information, assemble everything into a structured markdown document. Use this format:

```markdown
# Product Context

> Last updated: [date]

## Product Overview
- **One-liner:** [one-liner]
- **Category:** [category]
- **Pricing:** [pricing model]
- **Stage:** [stage]

## Target Audience
- **Ideal customer:** [description]
- **Primary use case:** [use case]
- **Discovery:** [how they find you]
- **Decision process:** [description]

## Personas
[If B2B — list each role with their priorities]

## Problems & Pain Points
- **Core problem:** [in customer words]
- **Current alternatives:** [what they do today]
- **Why alternatives fail:** [shortcomings]
- **Cost of problem:** [specific costs]
- **Emotional tension:** [how it feels]

## Competitive Landscape
- **Direct competitors:** [list with positioning]
- **Where they fall short:** [weaknesses]
- **Indirect alternatives:** [list]

## Differentiation
- **Key differentiators:** [list with "why it matters"]
- **Unfair advantage:** [if any]

## Objections & Responses
| Objection | Response |
|-----------|----------|
| [objection 1] | [response] |
| [objection 2] | [response] |
| [objection 3] | [response] |

**Anti-personas:** [who is NOT a fit]

## Switching Dynamics
- **Push (away from current):** [what's broken]
- **Pull (toward you):** [what's attractive]
- **Habit (keeps them stuck):** [inertia]
- **Anxiety (hesitation):** [fears]

## Customer Language
- **Problem language:** [exact quotes]
- **Solution language:** [exact quotes]
- **Words to use:** [list]
- **Words to avoid:** [list]

## Brand Voice
- **Attributes:** [selected attributes]
- **Description:** [how the brand talks]
- **Brands we admire:** [list]

## Proof Points
- **Key metrics:** [numbers]
- **Notable customers:** [logos/names]
- **Testimonials:** [best quotes]
- **Case studies:** [before/after stories]

## Goals & Metrics
- **Business goal:** [goal]
- **Primary conversion:** [action]
- **Current metrics:** [what's known]
```

Present the assembled document to the user for review. Ask them to confirm or request changes.

## Phase 3: Save

Save the confirmed document to `.claude/product-context.md`.

Let the user know: "All other marketing skills (campaign briefs, landing page copy, ad campaigns, etc.) will now automatically read this file so you don't have to repeat this information."

## Guidelines

- Real customer language > polished marketing copy — always push for specifics and quotes
- It's okay to have gaps — a partial context doc is far better than none
- Recommend updating this document quarterly or after major product changes
- If auto-drafting from codebase, present the draft and explicitly ask the user to correct anything that's wrong or outdated

## User Request

$ARGUMENTS
