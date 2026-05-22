---
name: step-6-pre-sell
description: Step 6 of the 7-step idea validation workflow — converts the smoke test into a real pre-sale by adding a Stripe payment link (or deposit) and direct outreach to the most engaged Step 5 visitors. Use after Step 5 has produced traffic and at least 5 interview slots. Use when the user only has email signups and wants the strongest possible demand signal before deciding.
---

# Step 6: Pre-Sell

## Overview

Email signups are interest. A charged card — even refundable — is intent. Step 6 swaps the fake-door CTA for a real payment link, communicates honestly with the people who've already raised their hand, and converts as many of them as possible into paying pre-orders before Step 7's decision.

This step is **optional but powerful**: a single paying pre-order at a real price is worth more than 100 email signups.

## When to Use

- Step 6 of the validation cycle, after [step-5-drive-traffic](../step-5-drive-traffic/SKILL.md)
- The user has signups but no payment evidence and is leaning toward "GO" — force a real price test
- Pre-sale is the natural next step in product categories where pre-orders are normal (B2B SaaS, courses, hardware, niche tools)

**Skip when:** the product is free-to-consumer / ad-supported / B2C with no clear pricing — for those, qualified interviews + waitlist conversion is the strongest available signal. Document the skip in the validation log.

## Process

### Step 1 — Choose the pre-sell model

| Model | What you collect | When to use |
|-------|------------------|-------------|
| **Refundable deposit** ($X, fully refunded if you don't ship) | Real charge, real intent, lowest risk to buyer | Default — works for most B2B / pro-sumer |
| **Lifetime deal** (one-time, big discount, refundable until launch) | Real charge, captures highest-intent users | Indie / dev tools, design tools |
| **Founding-customer slot** (annual upfront, limited to N seats) | Larger ticket, big intent signal | High-touch B2B, consultancies |
| **"Reserve at the launch price"** ($1 hold or signed letter of intent) | Soft signal | Enterprise; long sales cycles |

Refunds must be unconditional and clearly stated. This is the ethical floor and also the trust mechanic that makes pre-sales work.

### Step 2 — Set up in 30 minutes

Minimum stack:

- **Stripe Payment Link** (no code, ~5 min to create — `dashboard.stripe.com → Payment Links`)
- Set the description to the exact pre-sell offer + delivery date + refund policy
- Replace the Step 4 fake-door CTA on the landing page with the Stripe link (or keep both — "Pre-order for $X" primary, "Join waitlist" secondary)
- Auto-receipt email through Stripe with manual personalization within 24h

See [no-code-tools.md](../../references/no-code-tools.md#payment--pre-order) for alternatives (Gumroad, Lemon Squeezy, Polar.sh).

### Step 3 — Pre-sell communication

Write a short message and send personally to (a) every Step 5 signup, (b) every interview reply that said "interesting":

```
Subject: I'm opening a few pre-order slots — $X refundable

Hey [Name],

You signed up for [Product] last week. I'm opening N
pre-order slots before deciding whether to build it full-time.

  • Price: $X (50% off the launch price)
  • Delivery: by [date]
  • Refundable any time before launch — no questions

The slots exist so I commit to building this for the
people who actually need it. If that's you, here's the link:
  [Stripe payment link with UTM]

If not — I'd still love to know what's holding you back.

— [Name]
```

Personalize at least the first sentence per recipient. Do not bcc a list.

### Step 4 — Handle objections, learn from no's

The most valuable Step 6 output is not the yes — it's the structured no. For every reply that declines, ask one of:

- "What would have to be true for this to be a yes?"
- "What's your current workaround, and what would it take to replace it?"
- "Wrong price, wrong time, or wrong product?"

Log every reply in the validation log. The no-pattern decides Step 7's pivot direction.

### Step 5 — Track separately

Set up two metrics — do not collapse them:

- **Pre-order intent** — clicks on the Stripe button (Step 4 conversion event)
- **Pre-orders** — successful Stripe charges

The ratio (intent → charge) tells you how much friction the price is creating. The volume of either tells you about demand.

## Update the Validation Log

Add a `Step 6` section to `validation-log.md`:

- Pre-sell model chosen + price + refund terms
- Stripe link URL
- Outreach: number sent, by segment
- Responses: pre-orders, declines (with quoted reasons)
- Intent → charge ratio

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "Pre-sales without a built product feels dishonest" | A clear delivery date + unconditional refund is the opposite of dishonest. Hiding the price until after signup is what's dishonest. |
| "I'll charge after I build the MVP" | Then "validation" is just hope. The whole point is to test willingness-to-pay before you sink the time. |
| "I'll skip Stripe and use a payment form on my site" | Stripe Payment Links take 5 minutes and handle SCA, receipts, refunds, tax. Do not roll your own. |
| "Bulk-email my whole list with the offer" | Conversion plummets vs. personalized 1-1s on a list this small. Spend the 90 minutes; send 30 personal notes. |
| "I'll only count yeses; no's don't matter" | The structured no's are the most actionable data of the entire week. They tell you why and how to pivot. |

## Red Flags

- Refund policy is conditional or hidden
- Pre-sell price is "TBD" or "contact us"
- Charging without delivery date in writing
- Selling a feature you have not designed (over-promising — see [validation-pitfalls.md](../../references/validation-pitfalls.md))
- "I'll talk to objections later" — they evaporate within 48 hours

## Verification

- [ ] Pre-sell model chosen and documented, with written refund terms
- [ ] Stripe (or equivalent) payment link live and test-charged successfully
- [ ] Landing-page CTA updated; both intent and charge events tracked separately
- [ ] Personal outreach sent to ≥80% of Step 5 signups + warm interview leads
- [ ] At least 3 explicit declines logged with quoted reasons (these matter as much as the yeses)
- [ ] Validation log `Step 6` section committed before invoking [step-7-decide](../step-7-decide/SKILL.md)
