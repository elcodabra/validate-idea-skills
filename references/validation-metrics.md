# Validation Metrics & Log Template

Reference loaded by the `validate-idea-orchestrator` and `step-8-decide` skills.

## Validation Log Template

Create as `validation-log.md` in the project working directory. Keep all steps in one file — the goal on Step 8 is to read the whole thing in one sitting.

```markdown
# Validation Log — [Idea name]

Cycle: 1 / N (this is the Nth attempt for this idea)
Owner: [you]
Started: [YYYY-MM-DD]

## Step 0 — Framework
- Idea classification (buyer / price / cycle / monetization / reachability / delivery / newness):
- Recommended framework + runner-up + confidence + why:
- User confirm / override:
- Per-step plan (keep / skip / extend / replace):
- Kill-switch signal:

## Step 1 — Problem & Audience
**Problem statement:**
> [Specific person] struggles to [outcome] because [obstacle] which costs [time/money/status]. Today they cope by [workaround] which is bad because [gap].

**Segments:**
1. ...
2. ...

**Watering holes:**
| Segment | Channel | URL | Self-promo rules | Verbatim quote |
|---------|---------|-----|------------------|----------------|

## Step 2 — Competitor Analysis
| Competitor / Alternative | URL | Targets | Price | Advantages | Disadvantages | Verbatim complaint |
|--------------------------|-----|---------|-------|------------|---------------|--------------------|
- Head-to-head table (axes the segment cares about):
- The gap you'll own + supporting quote:
- Competitor price band:

## Step 3 — Value Proposition
- Chosen segment + why:
- Headline:
- Subhead:
- Bullet 1 / 2 / 3:
- Proof element:
- Rejected drafts:

## Step 4 — Landing Page
- URL:
- Builder + template:
- Primary CTA + why:
- Stated price + model:
- Screenshot: ![](path or link)

## Step 5 — Smoke Test
- Pattern: waitlist / fake door / pre-order
- Analytics tool + URL:
- Conversion event name + last verified at:
- UTM scheme:
- Auto-reply copy:

## Step 6 — Drive Traffic
- Channels:
- Posts / messages (timestamped):
- Visits by UTM source:
- Conversion by UTM source:
- Interview slots booked:

## Step 7 — Pre-Sell
- Model: deposit / lifetime / founding seat / LOI
- Price + refund terms:
- Stripe link:
- Outreach: N sent, M replies
- Pre-orders: N totaling $M
- Declines (quoted reasons):

## Step 8 — Decision
- Verdict: **GO | PIVOT | KILL**
- Evidence: ...
- Reasoning: ...
- Next action (dated):
```

## Reference Thresholds

Canonical for this pack. Step 8 reads these — do not duplicate them elsewhere.

| Signal | KILL | PIVOT | GO |
|--------|------|-------|----|
| Qualified visitors | <50 | 50–200 | >200 |
| CTA conversion (visitor → click) | <5% | 5–15% | >15% |
| Waitlist conversion (visitor → email) | <2% | 2–5% | >5% |
| Pre-order intent rate (B2C floor 1–2%, B2B floor 5%) | <1% | 1–3% | >3% |
| **Pre-orders (paying)** | 0 | 1–4 | ≥5 OR ≥$500 collected |
| Qualified interviews | <2 | 2–4 | ≥5 |

**Decision rule** (applied at Step 8): a clean **GO** requires the pre-order row AND the qualified-interviews row to *both* be at GO level. Either alone is insufficient. A single $500 enterprise deposit clears the pre-order threshold but still needs ≥5 conversations.

Tighten thresholds for B2C (consumer scale, easier conversion), loosen for niche B2B / enterprise (smaller list, longer cycle, higher deal size).

## What does NOT count

- "Likes" or impressions on a tweet
- Page views from your own / team's traffic
- "Yes" answers to "would you use this?" (leading)
- Signups from a giveaway or contest (extrinsic motivation)
- Friends, family, or current colleagues

## Source

Larry Qu, [*Validate Your Indie Hacker Idea in 7 Days (Without Writing Code)*](https://calmops.com/indie-hackers/validate-idea-in-7-days-without-code/), CalmOps, 2025.
