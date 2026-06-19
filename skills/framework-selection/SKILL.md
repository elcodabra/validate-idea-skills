---
name: framework-selection
description: Step 0 of the idea validation workflow — classifies the idea (B2B/B2C, price point, sales cycle, audience reachability, hardware/software, regulatory) and picks the validation framework that fits, then says which of the 8 steps to keep, skip, or extend. Defaults to this pack's 8-step smoke-test + pre-sell framework. Use at the very start, before Step 1, whenever a new idea arrives. Use also when the user asks "how should I validate this?", "which validation method fits?", or when the standard 8 steps feel wrong for the idea (enterprise sales, free consumer, a manual service, deep tech).
---

# Step 0: Framework Selection

## Overview

Not every idea is validated the same way. A $5/mo consumer app, a $50k enterprise platform, and a hand-delivered service all produce demand signal differently. Step 0 runs **before** Step 1: it classifies the idea, recommends the validation framework, and tunes which of the 8 steps to keep, skip, or extend — so the rest of the workflow is aimed at the right signal.

The default is this pack's **8-step smoke-test + pre-sell framework**. Most indie / pro-sumer / paid-tool ideas with a reachable audience should run it as-is. Step 0 exists to catch the ideas that shouldn't.

## When to Use

- The very first action on any new idea, before [step-1-problem-and-audience](../step-1-problem-and-audience/SKILL.md)
- The user asks "how should I validate this?" / "which method fits?" / "is a landing page even the right test here?"
- The standard 8 steps feel wrong: long enterprise cycles, a free/ad-supported consumer product, a manual service, hardware, or a regulated market
- A previous cycle produced no signal and you suspect the *method* was wrong, not the idea

## Process

### 1. Classify the idea

Ask only what you can't infer. Capture:

| Axis | Options |
|------|---------|
| Buyer | B2C / pro-sumer / B2B SMB / B2B enterprise |
| Price / ACV | free / <$20/mo / $20–200/mo / $200+/mo / $5k+ ACV |
| Sales cycle | impulse / days / weeks / months (procurement, security review) |
| How money is made | direct paid / freemium / ad-supported / marketplace take-rate |
| Audience reachability | easy (named watering holes) / hard (diffuse, offline, gated) |
| Delivery | pure software / human-in-the-loop service / hardware / regulated |
| Newness | better mousetrap / new behavior / network-effect (needs both sides) |

### 2. Pick the framework

Match the profile to a primary framework. These are **adaptations of**, not replacements for, the 8 steps unless noted.

| If the idea is… | Primary framework | What changes vs. the default 8 steps |
|---|---|---|
| Paid SaaS / pro-sumer tool, reachable audience | **8-step smoke-test + pre-sell** (default) | Run as-is |
| B2B enterprise, $5k+ ACV, months-long cycle | **Design-partner / LOI route** | Step 7 pre-sell becomes a signed LOI or paid pilot, not a Stripe link; extend Steps 6–7 to 30–90 days; weight qualified interviews over conversion rate |
| Manual service or "AI does X for you" where the value is the outcome | **Concierge / Wizard-of-Oz MVP** | Deliver the outcome by hand for the first N customers before any code; Step 7 charges for the manual service; landing page advertises the outcome, not a product |
| Free / ad-supported consumer, monetized by scale | **Engagement + retention test** | Pre-sell (Step 7) is N/A — substitute waitlist→activation and a retention/return-visit signal; raise the Step 6 traffic bar |
| Fuzzy problem, hard-to-reach audience, no clear segment | **Interview-led (The Mom Test)** | Lead with [customer-interviews](../customer-interviews/SKILL.md) before building any page; treat Steps 4–5 as optional until the problem is confirmed |
| Two-sided marketplace / network effect | **Single-side concierge + supply seeding** | Validate the harder side first by hand; a landing page alone can't test liquidity |
| Hardware / physical product / high unit cost | **Crowdfunding pre-sell (Kickstarter / Indiegogo)** | Step 7 becomes a public campaign with a funding goal + tiered rewards; the Step 4 page drives to the campaign; GO = campaign funds (or hits a pre-set % of goal) |
| Headline / price / offer genuinely uncertain, with traffic to spare | **Fake-door A/B test** | Ship 2 landing variants in Steps 4–5 (headline *or* price — one variable), split-route the Step 6 traffic by UTM, and let conversion pick the winner before Step 7 |
| Many untested assumptions, unclear which is riskiest | **Lean Canvas + riskiest-assumption mapping** | Run *before* Step 1: fill a one-page Lean Canvas, rank assumptions by (impact × uncertainty), and design Steps 4–7 to test the single riskiest one first |
| You already have some users | **Sean Ellis PMF survey** | Run the "how disappointed if this went away" survey alongside Step 8 instead of cold pre-sells |

If two fit, pick the one that tests the **riskiest assumption** first (does anyone want it? can I reach them? will they pay? can I deliver it?). When the riskiest assumption itself is unclear, start with the Lean Canvas mapping row above, then route to the matching framework.

### 3. Recommend to the user (and confirm)

Don't just present the table — **make one clear call.** State it in plain language and tie it to the classification, then let the user confirm or override. You own the reasoning; the user owns the final choice.

```
For "[idea]" ([buyer] · [price] · [cycle]), I recommend **[framework]**.
Why: [1–2 sentences citing the specific axes — e.g. "$8k ACV + a 2-month
     procurement cycle means a Stripe pre-order can't fire, but a signed
     LOI can"].
Runner-up: [framework] — switch to it if [condition].
Confidence: [high / medium / low] — would change if [the one fact that flips it].
```

Rules for a good recommendation:

- **One primary pick.** "It depends" is a non-answer; name the call and the condition that would change it.
- **Cite the classification, not generic advice.** The reason must reference the axes you filled in, not "this is best practice."
- **Default with a reason.** When the idea is an ordinary paid tool with a reachable audience, recommend the 8-step default *and say why nothing more exotic is needed* — don't reach for a fancier framework to look thorough.
- **Flag low confidence.** If the classification is thin (e.g. price or audience still unknown), say so and name what to learn first.

Wait for the user's confirm/override before tailoring the steps.

### 4. Tailor the 8 steps

Write the concrete plan: for each of Steps 1–8, mark **keep / skip / extend / replace**, with one line of why. Example for an enterprise idea:

- Steps 1–3: keep
- Step 4 (landing page): keep, but target design partners not self-serve
- Step 5 (smoke test): keep
- Step 6 (traffic): extend to 30 days, outreach-led
- Step 7 (pre-sell): **replace** Stripe link with signed LOI / paid pilot
- Step 8 (decide): keep, but GO threshold = N signed LOIs, not pre-orders

### 5. Name the kill-switch up front

State the single signal that, if absent, means KILL regardless of enthusiasm (e.g. "no design partner will sign an LOI", "0% return visits in week 2"). Naming it now prevents goal-post-moving at Step 8.

## Update the Validation Log

Add a `Step 0 — Framework` section to `validation-log.md`:

- Idea classification (the axes table, filled in)
- Recommended framework + runner-up + confidence + one-paragraph why
- The user's confirm or override
- Per-step keep / skip / extend / replace plan
- The named kill-switch signal

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "Just run the 8 steps, why pick a framework?" | For ~70% of ideas you will pick the default — and that's the point: a 2-minute check that confirms the method before you spend a week on it. |
| "My enterprise idea fits the landing-page + pre-order flow" | A $50k platform is not bought with a Stripe link from a Reddit post. Signed LOIs and design partners are the real signal; forcing pre-orders here produces a false KILL. |
| "It's a free consumer app, so there's nothing to validate" | Then the signal is retention and activation, not payment. Pick the engagement framework — don't skip validation, change what you measure. |
| "I'll figure out the method as I go" | Method drift mid-cycle means you can't trust any of the numbers. Choose once, up front, in writing. |
| "Concierge feels like cheating — I should build the real thing" | Delivering the outcome by hand is the fastest, highest-fidelity demand test there is. Automate only what the manual version proves people pay for. |

## Red Flags

- Defaulting to the 8 steps for an enterprise / hardware / regulated idea without reading this table
- No named kill-switch — guarantees a vibes-based Step 8
- Picking a framework that tests an easy assumption while the riskiest one goes untested
- "All of the above" — more than one primary framework means none is the focus

## Verification

- [ ] Idea classified across the axes in section 1
- [ ] One primary framework recommended to the user with reasoning, a runner-up, and a confidence level; user confirmed or overrode
- [ ] Per-step keep / skip / extend / replace plan recorded
- [ ] Kill-switch signal named before Step 1 begins
- [ ] Validation log `Step 0 — Framework` section committed before invoking [step-1-problem-and-audience](../step-1-problem-and-audience/SKILL.md)
