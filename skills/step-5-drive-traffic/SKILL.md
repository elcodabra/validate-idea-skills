---
name: step-5-drive-traffic
description: Step 5 of the 7-step idea validation workflow — drives 100–500 targeted visitors to the smoke-test page via communities, direct outreach, and one launch surface (Show HN, Product Hunt upcoming, niche newsletter). No ad budget required. Use after Step 4 is instrumented. Use also when an existing page has zero traffic and the user is unsure where to share it.
---

# Step 5: Drive Traffic

## Overview

The page is live and instrumented. Step 5 puts qualified eyeballs in front of it — not the most eyeballs, the most *qualified* eyeballs from the Step 1 watering holes. The target is 100–500 visitors from real segments, not 10,000 from generic Twitter.

## When to Use

- Step 5 of the validation cycle, after [step-4-smoke-test](../step-4-smoke-test/SKILL.md)
- The page is live but has had no real visitors yet
- Conversion data is missing because the traffic mix is wrong (e.g., friends-and-family only)

## Process

### 1. Set the target

- **Floor:** 100 unique visitors from the Step 1 segments — below this, conversion numbers are not statistically meaningful
- **Goal:** 200–500 in 48 hours
- **Channel diversity:** at least 3 sources so you can tell which segment / channel converts best (Step 7 input)

### 2. Channel strategy (in priority order, no ads required)

#### 2a. Community engagement (best ROI)

Take the watering-hole list from Step 1. For each:

- Read the community rules — most ban promotion. The ones that don't usually have a "Showcase Saturday" / "Self-promo Thursday" thread.
- **Contribute first.** Spend 60 minutes answering questions and commenting before posting anything about your project. Lurkers smell ads in the first sentence.
- Write the post in the community's voice. Lead with the problem (Step 1's verbatim quote), not the product.

Template (adapt for tone):

```
I keep seeing [problem quote] in this community.
I've been chewing on it for a while and put up a one-pager
describing what I think the fix looks like: [link with UTM].
If you've felt this pain, I'd love your reaction — especially
"this is wrong because…" replies.
```

Asking for criticism dramatically out-performs asking for signups.

#### 2b. Direct outreach (most effective)

- Find 20–50 people in the segment by name (LinkedIn, GitHub, Twitter bios, podcast guest lists)
- Send a short personalized message — 3–4 sentences, no pitch deck
- Ask for **15 minutes**, not a signup. You're really running [customer-interviews](../customer-interviews/SKILL.md) here.
- Include the landing page link as a footer (UTM tagged `cold-email`), not the ask
- Expect 10–20% reply rate when truly personalized; 1–2% if it's a template

#### 2c. "Show HN" (Hacker News)

One shot. Post once. Title format: `Show HN: [Tool name] – [outcome in 5–7 words]`. Be present in the comments for the first 4 hours. Strong fit for dev / infra / productivity tools, weak for consumer.

#### 2d. Product Hunt — upcoming page

Set up a "Coming soon" page on Product Hunt (separate from your launch). This collects intent emails over days/weeks without burning your one PH launch shot. Save the actual PH launch for after validation.

#### 2e. Niche newsletter / Slack / Discord

If your segment reads a particular newsletter, the cheapest play is a sponsored classified (often <$100) or a guest contribution. Save for after channels 2a–2c are exhausted.

### 3. Tag every share

Every link you post or send today must use the [Step 4 UTM scheme](../step-4-smoke-test/SKILL.md). One untagged link in a high-traffic thread can wreck the Step 7 attribution.

### 4. Set traffic expectations

Realistic 48-hour outcomes by channel (indie hacker scale):

| Channel | Typical visitors | Typical conversion |
|---------|-----------------:|-------------------:|
| 2 well-written subreddit posts | 50–200 | 2–8% |
| Show HN (front page) | 1,000–10,000 | 1–3% for dev/infra tools, 0.3–1% for consumer/non-dev |
| 30 personalized cold emails | 30–60 visits, 5–10 calls | 20–40% to conversion |
| Indie Hackers post | 50–300 | 3–10% |
| Twitter post from <1k account | 5–30 | <1% |
| Twitter post from >10k account | 200–1,000 | 1–3% |

If you're at 5 visitors after Step 5, the channels are wrong, not the page.

### 5. Capture interview slots

The point of cold outreach is conversations, not signups. Every reply that says "interesting" → invite to a 15-min call. Step 6/7 logic depends on having had ~5 real conversations.

## Update the Validation Log

Add a `Step 5` section to `validation-log.md`:

- Channels actually used
- Posts / messages sent (with timestamps and URLs)
- Visits per channel (from analytics, by UTM)
- Conversion per channel
- Interview slots booked

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "I'll just tweet it and see what happens" | Untargeted tweets from small accounts get <30 visits. You'll learn nothing. |
| "I'll spam every subreddit" | One ban kills a channel permanently. Read rules, contribute first, post once. |
| "Cold outreach feels icky" | A 4-sentence personalized email asking for 15 minutes is not spam. A 12-paragraph pitch deck is. |
| "I'll wait until I have more traffic before talking to people" | The 5 conversations you have on Step 5 are worth more than the next 500 visitors. |
| "Product Hunt now will be my launch" | PH should be saved for after validation — burning it now without product is a waste of your one shot. |

## Red Flags

- All visitors from one source
- No conversations booked
- Posting verbatim copies of the same message to 10 subreddits
- Tracking only "page views" with no UTM split
- Skipping interviews because "the data will tell me everything"

## Verification

- [ ] ≥100 unique visitors logged in analytics by end of day, tagged by UTM
- [ ] ≥3 distinct channels in the UTM split
- [ ] ≥5 customer interview slots booked or completed (see [customer-interviews](../customer-interviews/SKILL.md))
- [ ] No untagged share links
- [ ] Validation log `Step 5` section committed before invoking [step-6-pre-sell](../step-6-pre-sell/SKILL.md)
