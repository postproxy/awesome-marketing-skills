---
name: seo-at-scale
description: When the user wants to build SEO pages at scale using templates and data, create programmatic content, or plan a scalable SEO strategy. Also use when the user mentions "programmatic SEO", "pSEO", "template pages", "SEO at scale", "scalable content", "landing page templates", or "automated pages."
version: 1.0.0
---

# SEO at Scale (Programmatic SEO)

Plan and design scalable SEO page strategies that generate organic traffic through templatized, data-driven pages.

## Before You Start

**Check for product marketing context first:**
If `.claude/product-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered.

## Phase 1: Information Gathering

Collect context by asking the user focused questions in batches of 2-3.

### Required Context

1. **What does your product/service do?** Ask: "Describe your product in 1-2 sentences — what problem does it solve and for whom?"

2. **Current SEO state** — Use `AskUserQuestion` with options:
   - No SEO pages yet, starting from scratch
   - Have a blog but no programmatic pages
   - Already have some template pages, want to scale
   - Existing pSEO that needs improvement

3. **Data assets** — Ask: "What data do you have access to that could power template pages? (e.g., product catalog, location data, integrations list, user-generated content, industry benchmarks, competitor info)"

4. **Playbook direction** — Use `AskUserQuestion` with options:
   - Templates (e.g., "Invoice Template for [Industry]")
   - Comparisons (e.g., "[Product] vs [Competitor]")
   - Directories / Listings
   - Location pages (e.g., "[Service] in [City]")
   - Integration pages (e.g., "[Product] + [Integration]")
   - Glossary / educational terms
   - Use cases by persona or industry

5. **Target audience** — Ask: "Who are you trying to attract with these pages? What would they be searching for?"

6. **Content uniqueness** — Ask: "What unique value can each page provide beyond just swapping a variable? (e.g., proprietary data, curated recommendations, dynamic stats, real examples)"

7. **Technical setup** — Use `AskUserQuestion` with options:
   - Static site (Next.js, Astro, Hugo, etc.)
   - CMS-based (WordPress, Webflow, etc.)
   - Custom app with dynamic rendering
   - Not sure yet

8. **Scale target** — Ask: "Roughly how many pages are you thinking? (10s, 100s, 1000s?)"

## Phase 2: Strategy Design

Based on gathered context, design the programmatic SEO strategy:

### URL Structure
- Always use subfolders, not subdomains (subdomains dilute authority)
- Pattern: `yoursite.com/[category]/[variable]/`
- Keep URLs clean, readable, and keyword-rich

### Page Template Design
For each page, ensure:
- **Unique value per page** — not just variable swapping
- **Structured data** — schema markup for rich snippets
- **Internal linking** — connect related pages into clusters
- **User intent match** — the page answers what the searcher actually wants

### Content Layers (from strongest to weakest)
1. Proprietary / first-party data
2. Curated expert content
3. Aggregated public data with analysis
4. AI-generated content with human review

### Quality Gates
Every page must pass:
- [ ] Provides value specific to that page's topic
- [ ] Would not be considered "thin content" by Google
- [ ] Has proper title, meta description, H1 unique to the page
- [ ] Internal links to and from related pages
- [ ] Loads fast and works on mobile

## Phase 3: Deliverables

Generate and save:

1. **`seo-at-scale-plan.md`** — Complete strategy document with URL patterns, template design, data sources, and implementation steps
2. **`page-template.md`** — A sample page template showing all sections and where dynamic data goes

Present a summary and suggest next steps (e.g., "Use /marketing-copy to write the template copy" or "Use /conversion-audit to optimize the page template for conversions").

## Guidelines

- Quality over quantity — 100 great pages beat 10,000 thin ones
- Every page must earn its existence with unique value
- Start with one playbook, prove it works, then expand
- Monitor for Google thin content penalties after launch
- Plan for ongoing data updates — stale programmatic pages lose rankings

## User Request

$ARGUMENTS
