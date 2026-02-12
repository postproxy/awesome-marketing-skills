# Master Prompt Templates

Reference templates for generating image and text master prompts from a campaign brief.

## Image Generation Master Prompt Template

Structure the image prompt as follows:

```markdown
# Image Generation Master Prompt

## Campaign Context
- **Product/Service:** [from brief]
- **Target Audience:** [from brief]
- **Main Message:** [from brief]
- **Mood/Tone:** [derived from brief]

## Visual Direction

### Style
[Photography / Illustration / 3D render / Flat design / Mixed media — choose based on what fits the product and audience]

### Color Palette
[3-5 colors derived from brand context, audience preferences, and campaign mood. Include hex codes if brand colors are known.]

### Lighting & Atmosphere
[Describe lighting direction: natural/studio/dramatic/soft. Describe atmosphere: warm/cool/energetic/calm]

### Composition Notes
[Where the product sits in frame, rule of thirds, negative space for text overlay, focal point]

## Prompt Variations

### 1. Hero Image (16:9 landscape)
> [Full prompt — describe scene, subject, environment, lighting, style, mood. Be specific: "A [style] photograph of [subject] in [setting], [lighting description], [color mood], [composition detail]. [Technical: camera angle, depth of field, texture]"]

### 2. Social Media Square (1:1)
> [Full prompt — tighter composition, product-focused, bold visual impact, space for overlaid text]

### 3. Story / Vertical (9:16)
> [Full prompt — vertical composition, immersive feel, works for Instagram/TikTok stories, product in upper or lower third leaving space for text]

## Negative Prompt Suggestions
[What to avoid: cluttered backgrounds, wrong demographic, off-brand elements, specific visual artifacts]

## Technical Notes
- Recommended generation tools: [based on style — photorealistic → Flux/Midjourney, illustration → DALL-E/Midjourney]
- Seed/style consistency tip: Use the same style keywords across variations for visual cohesion
```

## Text Generation Master Prompt Template

Structure the text prompt as follows:

```markdown
# Text Generation Master Prompt

## Campaign Context
- **Product/Service:** [from brief]
- **Target Audience:** [from brief]
- **Main Message:** [from brief]
- **Communication Goal:** [from brief]

## Voice & Tone

### Brand Voice
[Describe the voice: authoritative, friendly, playful, minimal, bold, sophisticated — derived from brief and product type]

### Tone for This Campaign
[The specific emotional register: urgent, inspiring, reassuring, exciting, educational]

### Language Guidelines
- Vocabulary level: [Simple/Moderate/Sophisticated — match audience]
- Sentence structure: [Short & punchy / Flowing & descriptive / Mix]
- Avoid: [Jargon, clichés, specific words that don't fit]
- Lean into: [Power words, sensory language, social proof, specific benefits]

## Copy Formats

### Headlines (3 variations)

**A — Benefit-driven (direct)**
> [Headline that leads with the primary benefit. Clear, specific, no fluff.]

**B — Emotional / Storytelling**
> [Headline that creates curiosity or emotional resonance. Paints a picture.]

**C — Urgency / Action-oriented**
> [Headline with time pressure or strong call to action. Creates FOMO or momentum.]

### Body Copy (3 variations, 2-3 sentences each)

**A — Benefit-driven**
> [Expand on the main benefit. Include a supporting detail. End with CTA.]

**B — Storytelling**
> [Mini narrative or scenario. Show the transformation. End with CTA.]

**C — Problem-solution**
> [Name the pain point. Present the product as the solution. End with CTA.]

### CTAs (3 variations)
> - [Direct: "Shop now", "Get started", "Book your spot"]
> - [Soft: "Learn more", "See how it works", "Explore"]
> - [Urgent: "Don't miss out", "Limited time", "Last chance"]

### Social Media Captions (3 variations)

**A — Informative**
> [Caption that educates or informs. Include relevant hashtags.]

**B — Engaging / Conversational**
> [Caption that asks a question or invites interaction. Include relevant hashtags.]

**C — Promotional**
> [Caption that drives action. Include offer details if applicable. Include relevant hashtags.]

### Short-Form Ad Copy (3 variations, 1-2 lines each)

**A — Benefit-first**
> [Primary line + description for paid ads]

**B — Question hook**
> [Open with a question that resonates with target audience]

**C — Social proof / Authority**
> [Lead with credibility, numbers, or social proof]

## Platform Adaptation Notes
- **Instagram:** Visual-first, shorter captions, emoji-friendly, hashtag strategy
- **LinkedIn:** Professional tone, longer form acceptable, industry context
- **Facebook:** Conversational, community-oriented, can be longer
- **Twitter/X:** Concise, punchy, thread-friendly for longer content
- **TikTok:** Ultra-casual, trend-aware, hook in first line
```

## Example: Completed Image Prompt (Coffee Brand)

```
A warm-toned lifestyle photograph of a ceramic mug of freshly brewed artisan coffee
on a sunlit wooden table, morning light streaming through a window creating soft shadows,
steam rising gently, shallow depth of field with a blurred bookshelf and plant in background.
Earthy color palette: warm brown, cream, forest green, golden light.
Shot from 45-degree angle above, rule of thirds with mug in lower right.
Natural, cozy, inviting atmosphere. High resolution, editorial photography style.
```

## Example: Completed Text Prompt (Coffee Brand)

**Headline A (Benefit):** "Start Every Morning Right — Artisan Coffee Delivered to Your Door"

**Headline B (Emotional):** "That First Sip That Makes the Whole Day Possible"

**Headline C (Urgency):** "Your Morning Upgrade Ships Free — This Week Only"

**Body A:** "Freshly roasted, single-origin beans delivered on your schedule. No more settling for stale supermarket coffee. Subscribe today and taste the difference."

**Caption A:** "Mornings are better when your coffee is brewed from beans roasted just days ago. Single-origin. Freshly roasted. Delivered. ☕ #ArtisanCoffee #MorningRitual #CoffeeLovers"
