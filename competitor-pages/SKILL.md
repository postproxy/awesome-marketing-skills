---
name: competitor-pages
description: When the user wants to create competitor comparison pages, alternative pages, or vs pages. Also use when the user mentions "vs page", "competitor comparison", "alternatives page", "comparison landing page", "competitor content", or "[product] vs [product]."
version: 1.0.0
---

# Competitor & Comparison Page Builder

Create SEO-optimized competitor comparison and alternative pages that build trust through honest positioning.

## Before You Start

**Check for product marketing context first:**
If `.claude/product-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered.

## Phase 1: Information Gathering

Collect context by asking the user focused questions in batches of 2-3.

### Required Context

1. **Your product** — Ask: "What's your product? Describe what it does, who it's for, and what makes it different."

2. **Page type** — Use `AskUserQuestion` with options:
   - "Alternative to [Competitor]" page (targeting users switching away)
   - "[Competitor] Alternatives" page (roundup for evaluators)
   - "You vs [Competitor]" direct comparison page
   - "[Competitor A] vs [Competitor B]" third-party comparison (positioning yourself as the better option)

3. **Target competitor(s)** — Ask: "Which competitor(s) are you comparing against? List 1-5 names."

4. **Your key advantages** — Ask: "What are your top 3 advantages over this competitor? Be specific — features, pricing, support, ease of use, etc."

5. **Their key advantages** — Ask: "Be honest — where is the competitor genuinely better or more established? (This builds credibility with readers.)"

6. **Target searcher** — Ask: "Who is searching for this comparison? What stage are they in — actively looking to switch, early research, or comparing before a first purchase?"

7. **Proof points** — Ask: "What evidence do you have? (e.g., customer switching stories, benchmark data, review site ratings, feature comparisons, pricing differences)"

8. **SEO context** — Ask: "Do you know if people search for '[your product] vs [competitor]' or '[competitor] alternatives'? Any keyword data you can share?"

## Phase 2: Page Strategy

Based on the page type selected, design the page structure:

### Page Format: Alternative To [Competitor]
**URL:** `/alternative/[competitor]` or `/[competitor]-alternative`
- TL;DR summary at top
- Why people look for alternatives (acknowledge competitor strengths first)
- Where [competitor] falls short (honest, specific, verified)
- How your product solves those gaps
- Feature comparison table
- Customer switching stories
- Migration/switching guide
- CTA

### Page Format: [Competitor] Alternatives (Roundup)
**URL:** `/[competitor]-alternatives`
- Include 4-7 real alternatives (including yourself)
- Be genuinely helpful — don't trash competitors
- Position yourself as best for a specific use case
- Include pricing comparison
- "Best for" labels on each alternative

### Page Format: You vs [Competitor]
**URL:** `/vs/[competitor]` or `/compare/[competitor]`
- Side-by-side comparison (honest both ways)
- Feature-by-feature breakdown
- Pricing comparison
- "Choose [competitor] if..." and "Choose [you] if..." sections
- Real customer quotes

### Page Format: [Competitor A] vs [Competitor B]
- Objective comparison of both
- Position your product as "the third option" at the end
- Capture search traffic for competitor-vs-competitor terms

## Phase 3: Deliverables

Generate and save:

1. **`competitor-page-[competitor-name].md`** — Full page copy ready for publishing, including headline, sections, comparison table, and CTAs

Present a summary and suggest next steps (e.g., "Use /conversion-audit to optimize the page" or "Use /marketing-copy to refine the copy").

## Guidelines

- **Honesty builds trust** — acknowledge competitor strengths, be accurate about limitations, don't misrepresent features
- Readers comparing tools will verify claims — accuracy is non-negotiable
- Update competitor pages quarterly (pricing and features change)
- "Different tools fit different needs" framing beats "we're better at everything"
- Include schema markup recommendations for rich snippets
- Deep research: recommend signing up for competitor products, mining G2/Capterra reviews, gathering real switching stories

## User Request

$ARGUMENTS
