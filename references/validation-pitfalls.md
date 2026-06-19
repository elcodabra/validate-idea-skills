# Common Validation Pitfalls

Reference loaded by every step-skill in this pack.

## Pitfall 1 — Leading questions

> "Would you use a tool that does X?"

People say yes to be polite. Replace with past-behavior questions (see [customer-interviews](../skills/customer-interviews/SKILL.md)).

## Pitfall 2 — Vanity metrics

- Impressions
- Likes / hearts
- Page views without conversion denominator
- Email signups when payment was the question

If the metric goes up but the business doesn't, it's vanity.

## Pitfall 3 — Ignoring negative feedback

The structured "no" tells you why and what to change. Filing it as "not the right person" is confirmation bias. Log every decline with a quoted reason (Step 7).

## Pitfall 4 — Building too soon

Symptoms:
- "I'll just throw up a quick MVP" before Step 8 evidence exists
- Refactoring the landing page into a custom React app
- Setting up a Postgres schema "for when signups arrive"

The orchestrator's gate exists to block this. See `validate-idea-orchestrator → The Gate (non-negotiable)`.

## Pitfall 5 — No pricing test

"Free during beta" hides the only question that matters: would they pay? At minimum, state a price on the landing page. Step 7 turns it into a real charge.

## Pitfall 6 — Wrong audience

Symptoms:
- Step 6 traffic mostly from your existing followers, not the Step 1 segment
- Friends and family signing up
- Generic-platform traffic (homepage Reddit, broad Twitter) with no segment-specific channel

Re-read Step 1 watering holes. If the channels don't match the segment, no amount of headline tweaking saves it.

## Pitfall 7 — Sunk cost fallacy

After 6 months of building, "validation" becomes rationalization. Run this 8-step pack *before* the 6 months, not after.

## Pitfall 8 — The "if I build it, they will come" myth

A live product without distribution gets the same traffic as a landing page without distribution — zero. Step 6 (driving traffic) is not optional; it is the test.

## Source

Larry Qu, [*Validate Your Indie Hacker Idea in 7 Days (Without Writing Code)*](https://calmops.com/indie-hackers/validate-idea-in-7-days-without-code/), CalmOps, 2025 (Common Pitfalls + Real Talk sections).
