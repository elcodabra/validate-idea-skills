---
name: step-8-decide
description: Step 8 of the 8-step idea validation workflow — analyzes the validation log against quantitative thresholds and produces a written GO / PIVOT / KILL decision. This is the gate that controls whether any production code gets written. Use after Step 7 is complete. Use also when re-evaluating after a week-2 iteration cycle.
---

# Step 8: Analyze and Decide

## Overview

Step 8 is the decision gate. The validation log is now full of evidence; this skill turns it into one of three written verdicts:

- **GO** — strong evidence of demand and willingness-to-pay. Proceed to build.
- **PIVOT** — interesting signal but the segment, price, or shape is wrong. Re-run a focused 8-step cycle.
- **KILL** — no meaningful signal. Free yourself for the next idea.

No verdict, no code. Half-deciding ("I'll build a little and see") is how 6 months disappear.

## When to Use

- Step 8 of the validation cycle, after [step-7-pre-sell](../step-7-pre-sell/SKILL.md)
- Re-evaluating after a pivoted second cycle
- A founder is "about to start building" and you suspect they haven't actually decided based on data

## Process

### 1. Key metrics to analyze

Pull from the validation log and compute, do not estimate:

| Metric | How to compute | Source |
|--------|----------------|--------|
| Unique visitors | Analytics, unique by source | Step 5–6 |
| Visitors per qualified channel | UTM split, segment-aligned channels only | Step 6 |
| Landing page conversion to CTA | `cta_click` / `unique visitors` | Step 5 |
| Conversion to email/waitlist | `signup_submit` / unique visitors | Step 5 |
| Pre-order intent rate | `pre_order_intent` / unique visitors | Step 7 |
| Pre-orders | Stripe success count | Step 7 |
| Pre-order $ collected | Stripe revenue (gross) | Step 7 |
| Qualified interviews | 15+ min conversations with Step 1 segment | Step 6–7 |
| Decline reasons | Categorized (price / fit / time / scope) | Step 7 |

### 2. Apply the decision framework

Use the canonical threshold table in [validation-metrics.md → Reference Thresholds](../../references/validation-metrics.md#reference-thresholds). Do not redefine the numbers here.

The decision rule on top of those thresholds:

- **GO** — *both* the pre-order column AND the qualified-interviews column hit the GO row. Either alone is insufficient. (A single $500 enterprise deposit clears the pre-order threshold, but you still need ≥5 qualified conversations.)
- **KILL** — near-zero on every row, no coherent decline pattern.
- **PIVOT** — anything in between, with at least one specific changed variable identifiable from the decline reasons.

### 3. Write the decision

Add a `Step 8 — Decision` section to `validation-log.md`:

```markdown
## Step 8 — Decision

Verdict: **GO | PIVOT | KILL**

### Evidence
- Visitors: N (M qualified, by channel ...)
- Conversion: X% CTA, Y% waitlist
- Pre-orders: N totaling $M
- Interviews: N qualified, top 3 quotes
- Decline reasons (top 3): ...

### Reasoning
Two paragraphs in plain English. The verdict must follow the evidence, not the other way around.

### Next action (specific, dated)
- GO → next step: [which build skill, what scope, by when]
- PIVOT → next step: [what changes for the next cycle, which segment, restart Step 1 with ...]
- KILL → next step: [what was learned, what was sunk, what to try next]
```

### 4. On GO, scope the build narrowly

The Step 8 GO does **not** unlock building the full product. It unlocks building the smallest thing that fulfills the pre-orders. Hand off to `spec-driven-development` / `planning-and-task-breakdown` (or whatever your stack uses) with a scope no larger than: deliver the promised pre-sell offer to the N customers who paid.

### 5. On PIVOT, run another cycle

Restart from [step-1-problem-and-audience](../step-1-problem-and-audience/SKILL.md) with the changed variable made explicit: different segment, different price, different shape. Carry forward the Step 1–3 work that's still valid; redo what changes.

### 6. On KILL, log the lessons and move on

Capture: what was the wrong assumption, what could you not change (market, channel, price), and what you'd try differently in the next idea. This is the most valuable artifact for the next round.

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "The signals are mixed but I really believe in this — I'll build a little" | "A little" becomes 6 months. Either the data supports GO or it doesn't. PIVOT is also a valid answer; "build anyway" is not. |
| "My category needs more time — 8 steps isn't enough" | True for some categories (enterprise sales cycles, regulated industries). Then extend Step 6–7 explicitly to 21 or 30 days — don't blur the gate. |
| "Pre-orders are unfair — my product isn't built yet" | The whole framework is built around this constraint. Refundable pre-orders are the standard. |
| "I'll build the MVP because I want to use it myself" | That's a hobby project, not a validation outcome. Label it as such; the rest of the framework doesn't apply. |
| "I'll combine multiple weak signals into a strong one" | Weak signals don't compound; they reveal what people will say without commitment. Don't average vanity metrics into a GO. |

## Red Flags

- Verdict written before evidence is filled in
- "GO" with zero pre-orders and no qualified interviews
- "PIVOT" with no specified changed variable
- Skipping straight to a build skill without writing the decision section
- Re-defining the metric thresholds mid-decision to justify a desired outcome

## Verification

- [ ] Every metric row in section 1 (Key metrics) has a real number (or an explicit N/A with reason)
- [ ] Verdict written in the log with evidence and reasoning
- [ ] Next action is dated and concrete
- [ ] If GO: the build scope is constrained to fulfilling the pre-orders, not the whole product
- [ ] If PIVOT: the changed variable is named and Step 1 is restarted under it
- [ ] If KILL: lessons captured and the working directory is closed out
