---
name: step-4-landing-page
description: Step 4 of the 8-step idea validation workflow — ships a live landing page on a no-code builder (Carrd, Framer, Webflow, etc.) using the Step 3 copy. Use after Step 3 is complete. Use also when the user is about to write a custom React/Next.js app to validate an idea — redirect them to a no-code builder first.
---

# Step 4: Landing Page

## Overview

A live one-page site that turns Step 3's value proposition into something a stranger can find, read in 30 seconds, and act on. The page is built on a no-code platform — not custom code — because the goal is to ship today, not in two weeks.

## When to Use

- Step 4 of the validation cycle, after [step-3-value-proposition](../step-3-value-proposition/SKILL.md)
- User is reaching for `npx create-next-app` or a React boilerplate to "just throw something up". Stop them and run this skill instead.
- Rebuilding a landing page that isn't converting (combine with `step-3-value-proposition` rewrite first)

## Process

### 1. Pick a builder

Default recommendations by speed-to-live:

| Need | Pick | Why |
|------|------|-----|
| Fastest, simplest | **Carrd** | Single-page, $19/yr, live in an hour |
| Slightly richer design | **Framer** or **Typedream** | Free tier, good templates, fast |
| Existing brand site / want to scale this | **Webflow** | Heavier but production-ready |
| Already using a stack | **Vercel + a single static HTML file** | Only if you can ship in <2 hours |

See [no-code-tools.md](../../references/no-code-tools.md) for the full list.

**Do not build a custom app.** If the user insists, ask: "What signal will the custom app give that a Carrd page won't?" There usually isn't one.

### 2. The 7-block structure

A validation landing page has exactly these blocks, in order:

1. **Headline** (from Step 3)
2. **Subhead** — one line, the "for whom" + "without what"
3. **Primary CTA** — one button, above the fold ("Get early access", "Join the waitlist", "Pre-order for $X")
4. **3 benefit bullets** (from Step 3)
5. **Visual mock-up** — a screenshot, hand-drawn sketch, or short Loom. Real. Not a stock image.
6. **Proof element** (from Step 3)
7. **Secondary CTA** — same action as primary, at the bottom

No nav menu, no footer links, no "About us", no blog, no live chat widget. Every link off the page is a leak.

### 3. One primary action

Pick exactly one (Step 5 and Step 7 will iterate this):

- **Email waitlist** — lowest commitment, weakest signal
- **"Reserve your spot" form** — asks for use-case details, medium signal
- **Pre-order at a real price** — strongest signal (covered in [step-7-pre-sell](../step-7-pre-sell/SKILL.md))

If undecided, start with the form (medium signal) — Step 5 layers analytics, Step 7 swaps in payments.

### 4. Pricing clarity

Even if you're not collecting money yet, **state a price**. "Free during beta" hides the most important question: "would they pay?" Position it inside the Step 2 competitor price band. Use one of:

- "$X/month at launch — early adopters get 50% off"
- "$X one-time, refundable until launch"
- "Free during beta — usage capped at N/day"

### 5. Mockup or visual

People convert on what they can picture. Use, in order of preference:

1. A real screenshot of a prototype (Figma frame, even hand-sketched on paper and photographed)
2. A 30-60s Loom showing the *outcome* (not the UI)
3. A clean wireframe — never a generic SaaS dashboard stock image

### 6. Ship it

- Custom domain (cheap — Namecheap/Cloudflare). Bare subdomain on the builder is a credibility hit.
- HTTPS on (every builder does this by default; verify)
- Loads in <3 seconds on mobile
- Open the page on your phone. If you wouldn't tap the CTA, neither will visitors.

## Update the Validation Log

Add a `Step 4` section to `validation-log.md`:

- Live URL
- Builder + template used
- Primary CTA chosen + why
- Stated price + model
- Screenshot of the page as shipped

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "I want full control, I'll build with Next.js" | You're optimizing for craft when the task is learning. Ship on Carrd today; rebuild later if validated. |
| "I'll add a nav, footer, and about page so it looks legit" | Looking like a real SaaS site reduces conversion vs. a focused one-pager. Every link is a leak. |
| "I'll hide the price until they sign up" | Then you're only learning whether people are curious, not whether they'd pay. Pricing IS the validation. |
| "Stock dashboard image is fine for now" | Visitors detect this instantly and bounce. Use real screenshots, a Loom, or hand-sketched wireframes. |
| "The page can wait until I have a logo / brand" | A clean text-only Carrd page with the right headline outperforms a beautifully branded page with weak copy. |

## Red Flags

- Repo contains `package.json` for the landing page on Step 4
- Page has a nav with 4+ links
- No price visible anywhere
- CTA copy is "Learn more" or "Sign up" (vague)
- Page is on `something.framer.app` instead of a real domain

## Verification

- [ ] Live URL reachable on a real custom domain
- [ ] 7 blocks present, in order, with no extras
- [ ] One primary CTA visible above the fold
- [ ] Price stated somewhere on the page
- [ ] Mobile load <3s, HTTPS on
- [ ] Validation log `Step 4` section committed before invoking [step-5-smoke-test](../step-5-smoke-test/SKILL.md)
