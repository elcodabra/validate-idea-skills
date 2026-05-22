---
name: step-2-value-proposition
description: Step 2 of the 7-step idea validation workflow — turns the Step 1 problem statement into a one-line headline, three benefit bullets, and one proof element that passes the "so what?" test. Use after Step 1 is complete and before building the landing page. Use also when rewriting copy for a landing page that isn't converting.
---

# Step 2: Value Proposition

## Overview

A value proposition is one sentence that tells one segment what they get and why it beats what they do today. Step 2 turns the Step 1 problem statement into copy you can put on a page tomorrow.

## When to Use

- Step 2 of the validation cycle, after [step-1-problem-and-audience](../step-1-problem-and-audience/SKILL.md) is signed off
- Rewriting copy on a landing page with <2% CTA conversion
- The user can't describe the product in one sentence without using the word "platform"

## Process

### Step 1 — Pick ONE segment

Step 1 produced 2–3 segments. Pick the segment with (a) the most acute pain, (b) the easiest channel, and (c) existing paid tools. You can run Step 3–7 again for a second segment later.

### Step 2 — Draft the headline

Template:

```
[Verb the desired outcome] for [specific segment]
— without [the painful workaround they hate].
```

Examples (the form, not the content):

- "Ship indie hacker landing pages in an hour — without writing HTML."
- "Get studio-quality headshots for your LinkedIn — without booking a photographer."

The headline must pass three tests:

1. **Specificity** — segment is named or unmistakably implied
2. **Outcome over feature** — promises a result, not a tool
3. **"So what?" defeated** — a tired buyer reading it does not need a second sentence to understand the payoff

### Step 3 — Three benefit bullets

Each bullet = `Benefit → How you deliver it → Proof or specificity`.

Bad: "Fast and easy."
Good: "Live landing page in 60 minutes — drag-and-drop blocks, 12 templates tested for indie hacker conversion."

### Step 4 — One proof element

Pick one (in priority order):

1. **A real metric** ("147 indie hackers shipped pages with this in beta")
2. **A real quote** from the Step 1 watering-hole research, attributed
3. **A specific demo** ("watch a 30-second build", linked to a Loom)
4. **A credible competitor comparison** ("Same output as Webflow, 1/10 the setup")

Never invent a metric, quote, or logo. Faked social proof is a credibility cliff later and a Pitfall (see [validation-pitfalls.md](../../references/validation-pitfalls.md)).

### Step 5 — The Mom test

Run the draft past the "would my mom understand this?" test, then the harder one: would someone in the Step 1 watering hole *quote it back at someone else with the same problem*? If not, rewrite.

## Update the Validation Log

Add a `Step 2` section to `validation-log.md`:

- Chosen segment (and why over the others)
- Final headline + 3 bullets + proof element
- 2 rejected headline drafts and why they failed

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "I'll write five headlines and A/B test on the page" | You will not have enough traffic in 7 steps to A/B test. Pick one well-reasoned headline now; test variants after Step 5. |
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
- [ ] Headline passes specificity / outcome / "so what?" tests
- [ ] 3 benefit bullets each cite a real mechanism + proof
- [ ] One concrete proof element with a source link (or marked "TODO: capture before Step 5")
- [ ] Validation log `Step 2` section committed before invoking [step-3-landing-page](../step-3-landing-page/SKILL.md)
