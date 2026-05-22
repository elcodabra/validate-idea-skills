---
name: step-4-smoke-test
description: Step 4 of the 7-step idea validation workflow — instruments the landing page with analytics, a conversion event on the primary CTA, and a fake-door experience that captures intent without delivering a product. Use after Step 3 is live. Use also when an existing page is getting traffic but no measurable signal — the smoke test gear is missing.
---

# Step 4: Smoke Test

## Overview

A smoke test is a landing page that **acts like the product exists** so you can measure real intent, then handles the "click" honestly (no product yet, you tell them so). Step 4 wires up the instrumentation so Step 5's traffic produces evidence, not vibes.

## When to Use

- Step 4 of the validation cycle, after [step-3-landing-page](../step-3-landing-page/SKILL.md)
- Existing landing page has traffic but you can't say what % click the CTA
- "Our signups look fine" with no numerator/denominator — that's vanity. Run this skill.

## Process

### 1. Pick the smoke-test pattern

| Pattern | What the user sees | What you measure | Strength of signal |
|---------|--------------------|------------------|--------------------|
| **Waitlist** | "We're not live yet — leave your email" | Email signups | Low |
| **Fake door** | A "Get early access" / "Join the private beta" CTA opens a modal: "Thanks — we're shipping in N weeks. Tell us your use case and we'll prioritize early-access invites." | Click + qualified reply | Medium |
| **Pre-order** | Real Stripe payment link (see [step-6-pre-sell](../step-6-pre-sell/SKILL.md)) | Charges | High |

Default to **fake door** on Step 4 — it's honest (you tell them after the click), gives a stronger signal than email-only, and feeds the Step 5 interviews.

> Ethics rule: the CTA copy itself must signal pre-launch ("Get early access", "Join the private beta", "Pre-order"). CTAs that read "Start now", "Sign up", or "Buy" imply a working product and become deceptive when there isn't one. Never charge cards or claim a feature exists if it doesn't. "Coming soon" + honest modal after the click is the line — but the line starts at the button copy.

### 2. Analytics

Minimum kit (no enterprise tools):

- **Plausible**, **Fathom**, or **Umami** — privacy-friendly, ~5 minutes to install, GDPR-safe defaults
- Or **Google Analytics 4** if you must (more setup, ad-blocker noise)
- Plus the no-code builder's built-in stats as a sanity check

Set up at minimum:

- Page views by source (UTM)
- Outbound link clicks (some builders need a manual setting)
- One **custom conversion event** on the primary CTA

### 3. The conversion event

Define ONE primary conversion event. Examples:

- `cta_click` — fired the moment the primary CTA is clicked
- `signup_submit` — fired on form submission
- `pre_order_intent` — fired on click of the "Pre-order" button (separate from the actual Stripe success — track both)

Test it: open an incognito window, do the action, confirm the event lands in the analytics dashboard within 60 seconds. If it doesn't, fix it now — Step 5 traffic without this is wasted.

### 4. UTM scheme

Set up your URL conventions before sharing any link on Step 5:

```
https://yoursite.com/?utm_source=<channel>&utm_medium=<post|comment|dm>&utm_campaign=launch-week
```

Examples:

- `utm_source=reddit&utm_medium=comment&utm_campaign=launch-week`
- `utm_source=ih&utm_medium=post&utm_campaign=launch-week`
- `utm_source=cold-email&utm_medium=dm&utm_campaign=launch-week`

Document the scheme in the validation log so every link you ship tomorrow is taggable.

### 5. Test messaging variations (optional, lightweight)

If the builder supports it cheaply, create 2 versions of the headline (the only thing worth testing at this volume). Otherwise, plan to swap copy mid-week after the first 100 visitors and re-measure — that's enough at indie-hacker traffic levels.

### 6. The post-click experience

When a visitor converts, what do they get? Write this **today**, not after they sign up:

- Auto-reply email (set up in the form tool or via a simple ESP — ConvertKit, Beehiiv, MailerLite, Buttondown)
- The email asks 1–2 questions ("What pushed you to sign up today?") — these answers feed [customer-interviews](../customer-interviews/SKILL.md) on Step 5
- A calendar link for a 15-min call (Cal.com, SavvyCal) — optional but high-signal for B2B

## Update the Validation Log

Add a `Step 4` section to `validation-log.md`:

- Smoke-test pattern chosen + why
- Analytics tool + dashboard URL
- Conversion event name + verified test run timestamp
- UTM scheme
- Auto-reply email copy

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "I'll just count signups in the form tool" | Without page-view denominator you can't compute conversion. A 10% conversion on 50 visits is great; a 10% conversion on 5,000 is a disaster. |
| "I'll add analytics after I see if there's traffic" | Then you'll lose the first cohort, who matter most. Wire it up before Step 5. |
| "Fake door is dishonest — I should wait until I have a product" | Fake door with a clear post-click message is standard practice. Charging without a refund or hiding the "not built yet" message is what's wrong. |
| "UTMs are overkill for indie hacker traffic" | At 100 visitors, UTMs are the only way to tell which channel converted. Without them, Step 7 becomes a guess. |

## Red Flags

- No conversion event defined
- Same URL shared everywhere with no UTM
- Auto-reply email is the builder's default "Thanks for subscribing"
- "Buy now" or "Get it" CTAs on a fake-door — must clearly indicate intent, not purchase
- User wants to launch a Product Hunt before the analytics work

## Verification

- [ ] Analytics installed and showing real-time data
- [ ] One conversion event verified end-to-end in incognito
- [ ] UTM scheme documented and applied to at least one share link
- [ ] Auto-reply email live and tested
- [ ] Post-click experience is honest (no product where there is no product)
- [ ] Validation log `Step 4` section committed before invoking [step-5-drive-traffic](../step-5-drive-traffic/SKILL.md)
