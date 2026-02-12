# Awesome Marketing Skills

A collection of Claude Code skills for marketing content creation, powered by [PostProxy](https://postproxy.dev).

## Getting Started

**Start with Product Context.** Before using any other skill, run `/product-context` to create your foundational product marketing document (`.claude/product-context.md`). This captures your product's positioning, audience, messaging, and voice so every other skill can reference it automatically — you only describe your product once.

```
> /product-context
```

## Skills

| Skill | Description |
|-------|-------------|
| **product-context** | Create your foundational product marketing document — positioning, audience, messaging, and brand voice. **Use this first.** |
| **campaign-brief** | Build structured campaign briefs and generate master prompts for AI image generation and copywriting. |
| **marketing-copy** | Write, rewrite, or improve marketing copy for landing pages, headlines, CTAs, and more. |
| **social-creator** | Create social media posts, plan content calendars, and optimize social strategy. |
| **email-flows** | Design email sequences, drip campaigns, and automated nurture flows. |
| **ad-campaigns** | Create and optimize paid advertising campaigns across Google, Meta, LinkedIn, and more. |
| **seo-at-scale** | Build programmatic SEO pages at scale using templates and data. |
| **competitor-pages** | Create competitor comparison pages, alternative pages, and vs pages. |
| **go-to-market** | Plan product launches and go-to-market strategies. |
| **pricing-plan** | Design, evaluate, and optimize pricing strategies and tiers. |
| **conversion-audit** | Audit landing pages and optimize for conversions. |
| **ab-test** | Plan and design A/B tests and experiments. |

## Installation

Clone this repo and add it as a skill source in your Claude Code project:

```bash
git clone https://github.com/postproxy/awesome-marketing-skills.git
```

Copy any skill directory into your project's `.claude/skills/` folder, or reference them directly.

## Structure

```
awesome-marketing-skills/
  product-context/          # Start here — foundational product document
  campaign-brief/
  marketing-copy/
  social-creator/
  email-flows/
  ad-campaigns/
  seo-at-scale/
  competitor-pages/
  go-to-market/
  pricing-plan/
  conversion-audit/
  ab-test/
```

Each skill directory contains:
- `SKILL.md` — Skill definition and workflow
- `references/` — Templates and reference files (where applicable)

## Usage

From Claude Code, invoke any skill naturally:

```
> create a campaign brief for my new product launch
```

Or use slash commands:

```
> /campaign-brief
> /social-creator
> /email-flows
```

## Contributing

To add a new skill:

1. Create a new directory with a descriptive name (e.g., `social-calendar/`)
2. Add a `SKILL.md` with frontmatter (`name`, `description`, `version`) and workflow instructions
3. Include any reference files in a `references/` subdirectory
4. Submit a pull request

## License

MIT
