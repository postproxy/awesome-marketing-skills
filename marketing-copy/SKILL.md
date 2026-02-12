---
name: marketing-copy
description: When the user wants to write, rewrite, or improve marketing copy for any page or asset. Also use when the user mentions "write copy", "copywriting", "headline", "landing page copy", "improve this copy", "rewrite this", "CTA copy", "value proposition", or "tagline."
version: 1.0.0
---

# Marketing Copywriter

Write, rewrite, or improve marketing copy for any page type — from headlines and CTAs to full landing page copy.

## Before You Start

**Check for product marketing context first:**
If `.claude/product-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered.

## Phase 1: Information Gathering

Collect context by asking the user focused questions in batches of 2-3.

### Required Context

1. **What do you need?** — Use `AskUserQuestion` with options:
   - Write copy from scratch (new page or asset)
   - Rewrite / improve existing copy
   - Write a specific element (headline, CTA, tagline, etc.)
   - Adapt copy for a different audience or platform

2. **What is this for?** — Use `AskUserQuestion` with options:
   - Homepage
   - Landing page
   - Pricing page
   - Feature / product page
   - About page
   - Email
   - Ad copy
   - Social media
   - Other

3. **What are you selling?** — Ask: "Describe the product or service in 2-3 sentences. What does it do, who is it for, and what makes it different from alternatives?"

4. **Target audience** — Ask: "Who will read this copy? Describe them: what's their role, what problem are they trying to solve, what do they already know about your product?"

5. **Desired action** — Ask: "What's the #1 thing you want the reader to do after reading this? (e.g., sign up, request demo, buy, learn more)"

6. **Tone and voice** — Use `AskUserQuestion` with options:
   - Professional and polished
   - Casual and conversational
   - Bold and confident
   - Warm and empathetic
   - Technical and precise
   - Playful and witty

7. **Existing copy** — Ask: "Paste your current copy if you have any. If starting from scratch, share any notes, bullet points, or rough ideas you have."

8. **Proof points** — Ask: "What evidence supports your claims? (e.g., customer results, stats, testimonials, awards, logos, case studies)"

9. **Constraints** — Ask: "Any constraints? (e.g., character limits, brand guidelines, words to avoid, regulatory requirements, must-include elements)"

## Phase 2: Copy Creation

### Core Principles

1. **Clarity over cleverness** — if it's not instantly understood, it fails
2. **Benefits over features** — "what it does for you" beats "what it does"
3. **Specificity over vagueness** — "saves 3 hours/week" beats "saves time"
4. **Customer language over company language** — use the words they use

### Writing Rules

- Simple vocabulary (8th grade reading level unless audience demands more)
- Active voice, confident tone
- Short paragraphs (1-3 sentences)
- No jargon, buzzwords, or filler ("innovative", "cutting-edge", "seamlessly")
- No exclamation points (the copy should be exciting without them)
- Every sentence earns its place — if removing it changes nothing, remove it

### Page Structure (for full pages)

**Above the fold:**
- Headline (core value proposition)
- Subheadline (supporting detail or how)
- Primary CTA
- Social proof hint (logos, "trusted by X")

**Core sections:**
- Problem / pain point acknowledgment
- Solution / how it works
- Key benefits (3-5, with specifics)
- Social proof (testimonials, case studies, numbers)
- Objection handling (FAQ or dedicated section)
- Final CTA with urgency or incentive

### CTA Formula
**[Action Verb] + [What They Get]**
- "Start Free Trial" not "Submit"
- "Get the Report" not "Download"
- "See Pricing" not "Learn More"

### Headline Patterns

**Outcome-focused:** "Get [desired outcome] without [pain point]"
**Specific:** Include numbers, timeframes, or concrete details
**Social proof:** "Join [X] teams who [outcome]"
**Question:** "Still [doing painful thing]?"
**How-to:** "How [audience] [achieves outcome] with [product]"

## Phase 3: Deliverables

For every copy request, provide:

1. **3 headline variations** (benefit-driven, emotional, urgency)
2. **Full copy** in the requested format
3. **CTA options** (3 variations)
4. **Brief rationale** for key copy decisions

Save to:
- **`copy-[page-type].md`** — Complete copy document

Present the copy and suggest next steps (e.g., "Use /conversion-audit to evaluate the full page" or "Use /split-test to test headline variations").

## Guidelines

- Write copy that's ready to use — no brackets, no placeholder text, no "insert X here"
- Always provide multiple options for headlines and CTAs — the user should choose
- If rewriting existing copy, explain what you changed and why
- Match the complexity and formality to the audience — B2B enterprise copy is different from B2C consumer copy
- Don't oversell — good copy makes realistic promises and delivers on them

## User Request

$ARGUMENTS
