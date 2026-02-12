---
name: ab-test
description: When the user wants to plan, design, or set up an A/B test or experiment. Also use when the user mentions "A/B test", "split test", "experiment", "test this change", "hypothesis", "multivariate test", "conversion test", or "which version is better."
version: 1.0.0
---

# A/B Test Designer

Design statistically valid A/B tests with clear hypotheses, proper sample sizing, and actionable analysis plans.

## Before You Start

**Check for product marketing context first:**
If `.claude/product-context.md` exists, read it before asking questions. Use that context and only ask for information not already covered.

## Phase 1: Information Gathering

Collect test context by asking the user focused questions in batches of 2-3.

### Required Context

1. **What do you want to test?** Ask: "What change are you considering? Describe the current version and what you want to try differently."

2. **Why this test?** Ask: "What made you want to test this? Is it based on data, user feedback, a hunch, or something else?"

3. **Where does this live?** — Use `AskUserQuestion` with options:
   - Landing page / marketing page
   - Pricing page
   - Signup / onboarding flow
   - Email (subject line, copy, CTA)
   - In-product feature
   - Ad creative or copy

4. **Current performance** — Ask: "What's the current conversion rate (or best estimate) for what you're testing? And roughly how much traffic or volume does this page/flow get per week?"

5. **Success metric** — Ask: "What's the primary metric you'll use to judge the winner? (e.g., click-through rate, signup rate, revenue per visitor, activation rate)"

6. **Secondary metrics** — Ask: "Any secondary metrics to watch? And are there any guardrail metrics that should NOT get worse? (e.g., support tickets, refund rate, bounce rate)"

7. **Minimum detectable effect** — Use `AskUserQuestion` with options:
   - Small improvement is worth it (5-10% lift)
   - Need a moderate improvement (10-20% lift)
   - Only care about big wins (20%+ lift)
   - Not sure — help me decide

8. **Testing tools** — Use `AskUserQuestion` with options:
   - PostHog
   - Optimizely / VWO
   - Google Optimize (or successor)
   - LaunchDarkly / feature flags
   - Custom / built in-house
   - No tool yet — need recommendation

9. **Constraints** — Ask: "Any constraints? (e.g., limited dev resources, can't change certain elements, seasonal traffic patterns, stakeholder opinions)"

## Phase 2: Test Design

Based on gathered context, design the complete experiment.

### Hypothesis

Structure as:
```
Because [observation/data],
we believe [specific change]
will cause [expected outcome]
for [audience segment].
We'll know this is true when [primary metric] improves by [threshold].
```

### Sample Size & Duration

Use this reference for planning:

| Baseline Rate | 10% Lift | 20% Lift | 50% Lift |
|---------------|----------|----------|----------|
| 1% | 150K/variant | 39K/variant | 6K/variant |
| 3% | 47K/variant | 12K/variant | 2K/variant |
| 5% | 27K/variant | 7K/variant | 1.2K/variant |
| 10% | 12K/variant | 3K/variant | 550/variant |

Calculate estimated test duration based on the user's traffic volume.

### Variant Design
- Describe control (A) and variant (B) in specific detail
- Single variable change — isolate what you're testing
- Bold enough to produce a measurable difference

### Traffic Allocation
- Default: 50/50 split
- If risk is high: start 90/10 or 80/20 and ramp up
- Ensure user consistency (same visitor sees same variant)

### Analysis Plan
- Pre-commit to sample size — no peeking and stopping early
- 95% confidence threshold (p < 0.05)
- Plan for: significant winner, significant loser, and inconclusive scenarios

## Phase 3: Deliverables

Generate and save:

1. **`split-test-plan.md`** — Complete test plan with hypothesis, variants, sample size, duration estimate, metrics, and analysis plan

Present a summary and suggest next steps.

## Guidelines

- The #1 mistake is stopping tests early because results "look good" — pre-commit to sample size
- If traffic is too low for statistical significance, recommend bigger/bolder changes or qualitative testing instead
- One test at a time per page/flow unless traffic supports concurrent tests
- Document every test — even losers teach you something
- Always ask "what will we do with the results?" before starting

## User Request

$ARGUMENTS
