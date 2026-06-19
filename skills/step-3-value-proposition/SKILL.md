---
name: step-3-value-proposition
description: Step 3 of the 8-step idea validation workflow — turns the Step 1 problem statement and the Step 2 competitor gap into a one-line headline, three benefit bullets, and one proof element that passes the "so what?" test. Use after Steps 1–2 are complete and before building the landing page. Use also when rewriting copy for a landing page that isn't converting.
---

# Step 3: Value Proposition

## Overview

A value proposition is one sentence that tells one segment what they get and why it beats what they do today. Step 3 turns the Step 1 problem statement and the Step 2 competitor gap into copy you can put on a page tomorrow.

## When to Use

- Step 3 of the validation cycle, after [step-2-competitor-analysis](../step-2-competitor-analysis/SKILL.md) is signed off
- Rewriting copy on a landing page with <5% CTA conversion (below the KILL threshold in [validation-metrics.md](../../references/validation-metrics.md#reference-thresholds))
- The user can't describe the product in one sentence without using the word "platform"

## Process

### 1. Pick ONE segment

Step 1 produced 2–3 segments. Pick the segment with (a) the most acute pain, (b) the easiest channel, and (c) existing paid tools. You can run Step 4–8 again for a second segment later.

### 2. Draft the headline

Template:

```
[Verb the desired outcome] for [specific segment]
— without [the painful workaround they hate].
```

The "without" half should attack the gap you found in [step-2-competitor-analysis](../step-2-competitor-analysis/SKILL.md) — the axis every alternative gets wrong.

Examples (the form, not the content):

- "Ship indie hacker landing pages in an hour — without writing HTML."
- "Get studio-quality headshots for your LinkedIn — without booking a photographer."

The headline must pass three tests:

1. **Specificity** — segment is named or unmistakably implied
2. **Outcome over feature** — promises a result, not a tool
3. **"So what?" defeated** — a tired buyer reading it does not need a second sentence to understand the payoff

### 3. Three benefit bullets

Each bullet = `Benefit → How you deliver it → Proof or specificity`.

Bad: "Fast and easy."
Good: "Live landing page in 60 minutes — drag-and-drop blocks, 12 templates tested for indie hacker conversion."

### 4. One proof element

Pick one (in priority order):

1. **A real metric** ("147 indie hackers shipped pages with this in beta")
2. **A real quote** from the Step 1 watering-hole research, attributed
3. **A specific demo** ("watch a 30-second build", linked to a Loom)
4. **A credible competitor comparison** built from the Step 2 table ("Same output as Webflow, 1/10 the setup")

Never invent a metric, quote, or logo. Faked social proof is a credibility cliff later and a Pitfall (see [validation-pitfalls.md](../../references/validation-pitfalls.md)).

### 5. The Mom test

Run the draft past the "would my mom understand this?" test, then the harder one: would someone in the Step 1 watering hole *quote it back at someone else with the same problem*? If not, rewrite.

## Update the Validation Log

Add a `Step 3` section to `validation-log.md`:

- Chosen segment (and why over the others)
- Final headline + 3 bullets + proof element
- 2 rejected headline drafts and why they failed

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "I'll write five headlines and A/B test on the page" | You will not have enough traffic in the cycle to A/B test. Pick one well-reasoned headline now; test variants after Step 6. |
| "My product does many things, I need to mention them all" | The page that mentions everything sells nothing. Pick one outcome for one segment. |
| "Feature words are fine — my audience is technical" | Technical buyers still buy outcomes. "Postgres-backed event queue" works only if the outcome ("never lose a webhook") is also there. |
| "I'll write the copy after the page is built" | The copy *is* the page. Layout is a wrapper. |

## Red Flags

- Headline contains "platform", "solution", "powered by AI", "next-gen", "revolutionary"
- More than one audience addressed
- Benefits are adjectives ("fast", "easy", "powerful") with no proof
- Inventing testimonials, logos, or numbers
- Trying to write copy without a chosen segment

## Verification

- [ ] One segment chosen, one paragraph explains why
- [ ] Headline passes specificity / outcome / "so what?" tests and attacks the Step 2 gap
- [ ] 3 benefit bullets each cite a real mechanism + proof
- [ ] One concrete proof element with a source link (or marked "TODO: capture before Step 6")
- [ ] Validation log `Step 3` section committed before invoking [step-4-landing-page](../step-4-landing-page/SKILL.md)
