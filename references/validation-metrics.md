# Validation Metrics & Log Template

Reference loaded by the `validate-idea-orchestrator` and `step-7-decide` skills.

## Validation Log Template

Create as `validation-log.md` in the project working directory. Keep all days in one file — the goal on Step 7 is to read the whole thing in one sitting.

```markdown
# Validation Log — [Idea name]

Cycle: 1 / N (this is the Nth attempt for this idea)
Owner: [you]
Started: [YYYY-MM-DD]

## Step 1 — Problem & Audience
**Problem statement:**
> [Specific person] struggles to [outcome] because [obstacle] which costs [time/money/status]. Today they cope by [workaround] which is bad because [gap].

**Segments:**
1. ...
2. ...

**Watering holes:**
| Segment | Channel | URL | Self-promo rules | Verbatim quote |
|---------|---------|-----|------------------|----------------|

## Step 2 — Value Proposition
- Chosen segment + why:
- Headline:
- Subhead:
- Bullet 1 / 2 / 3:
- Proof element:
- Rejected drafts:

## Step 3 — Landing Page
- URL:
- Builder + template:
- Primary CTA + why:
- Stated price + model:
- Screenshot: ![](path or link)

## Step 4 — Smoke Test
- Pattern: waitlist / fake door / pre-order
- Analytics tool + URL:
- Conversion event name + last verified at:
- UTM scheme:
- Auto-reply copy:

## Step 5 — Drive Traffic
- Channels:
- Posts / messages (timestamped):
- Visits by UTM source:
- Conversion by UTM source:
- Interview slots booked:

## Step 6 — Pre-Sell
- Model: deposit / lifetime / founding seat / LOI
- Price + refund terms:
- Stripe link:
- Outreach: N sent, M replies
- Pre-orders: N totaling $M
- Declines (quoted reasons):

## Step 7 — Decision
- Verdict: **GO | PIVOT | KILL**
- Evidence: ...
- Reasoning: ...
- Next action (dated):
```

## Reference Thresholds

Tighter for B2C / consumer, looser for niche B2B / enterprise.

| Signal | KILL | PIVOT | GO |
|--------|------|-------|----|
| Qualified visitors | <50 | 50–200 | >200 |
| CTA conversion (visitor → click) | <5% | 5–15% | >15% |
| Waitlist conversion (visitor → email) | <2% | 2–5% | >5% |
| Pre-order intent rate | <1% | 1–3% | >3% |
| **Pre-orders (paying)** | 0 | 1–4 | ≥5 OR ≥$500 collected |
| Qualified interviews | <2 | 2–4 | ≥5 |

A clean **GO** requires both: ≥5 paying pre-orders *and* ≥5 qualified interviews. Either alone is insufficient.

## What does NOT count

- "Likes" or impressions on a tweet
- Page views from your own / team's traffic
- "Yes" answers to "would you use this?" (leading)
- Signups from a giveaway or contest (extrinsic motivation)
- Friends, family, or current colleagues

## Source

Larry Qu, *Validate Your Indie Hacker Idea in 7 Days (Without Writing Code)*, CalmOps, 2025.
