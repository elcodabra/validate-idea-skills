---
name: validate-idea-orchestrator
description: Routes an indie hacker through an 8-step no-code idea validation workflow — picks the right step-skill, tracks the validation log, and enforces the go/no-go gate at the end. Use when the user says "validate my idea", "I have an idea for...", "should I build this", "is there a market for...", or mentions smoke tests, landing pages, or pre-sales for an unbuilt product. Use at the start of any indie hacker / SaaS / micro-product idea conversation before any code is written.
---

# Validate Idea Orchestrator

## Overview

An 8-step workflow that proves real demand for a product idea using competitor analysis, smoke tests, landing pages, and pre-sales — no code. This skill is the entry point; it routes the user to the correct step-skill based on where they are and enforces the rule that **no code gets written until the Step 8 decision says GO**.

Inspired by *Validate Your Indie Hacker Idea in 7 Days (Without Writing Code)* — Larry Qu, CalmOps.

## When to Use

Trigger on any of:

- "I have an idea for…", "should I build…", "validate my idea", "is there demand for…"
- The user wants to start coding an MVP they haven't proven anyone wants
- Mentions of: smoke test, landing page validation, pre-sale, waitlist, fake door, pre-order
- A new project directory with no users yet and no shipped product

**Do NOT use when:** the user already has paying customers, is asking purely technical questions about an existing product, or is in a CTF / pure-engineering task.

## The 8-Step Map

| Step | Skill | Outcome |
|-----|-------|---------|
| 1 | [step-1-problem-and-audience](../step-1-problem-and-audience/SKILL.md) | Written problem statement, 2–3 target segments, list of watering holes |
| 2 | [step-2-competitor-analysis](../step-2-competitor-analysis/SKILL.md) | Advantages/disadvantages table for each competitor & alternative; the gap to own |
| 3 | [step-3-value-proposition](../step-3-value-proposition/SKILL.md) | One headline + 3 benefit bullets that pass the "so what?" test |
| 4 | [step-4-landing-page](../step-4-landing-page/SKILL.md) | Live landing page on a no-code builder with a single primary CTA |
| 5 | [step-5-smoke-test](../step-5-smoke-test/SKILL.md) | Analytics, conversion event, and a fake-door / waitlist hooked up |
| 6 | [step-6-drive-traffic](../step-6-drive-traffic/SKILL.md) | 100–500 targeted visitors via communities, outreach, or "Show HN" |
| 7 | [step-7-pre-sell](../step-7-pre-sell/SKILL.md) | Stripe payment link or deposit page; first pre-orders (or rejections) |
| 8 | [step-8-decide](../step-8-decide/SKILL.md) | Validation log filled in; go / pivot / kill decision recorded |

Cross-cutting:

- [customer-interviews](../customer-interviews/SKILL.md) — used inside Steps 1, 6, and 7
- References: [validation-metrics.md](../../references/validation-metrics.md), [no-code-tools.md](../../references/no-code-tools.md), [validation-pitfalls.md](../../references/validation-pitfalls.md)

## Process

1. **Orient.** Ask the user where they are. Two questions only:
   - "One sentence: what's the idea and who is it for?"
   - "Which of Step 1–7 are you on (or have you done none yet)?"
2. **Create the validation log.** Write `validation-log.md` in the working directory with the template from [validation-metrics.md](../../references/validation-metrics.md#validation-log-template). Every step-skill updates it. The log is the single source of truth.
3. **Route to the step-skill.** Invoke the matching `step-N-*` skill. Do not do that step's work yourself — defer to the skill.
4. **Enforce the gate.** After each step, ask: "Did you complete the step's exit criteria? (y/n)" If no, do not advance. If the user wants to skip ahead to coding, refuse and quote the Step 8 decision rule from this file.
5. **Close the loop.** After Step 8, the decision is GO, PIVOT, or KILL. Only on GO does the agent switch to a build skill (e.g. `spec-driven-development`).

## The Gate (non-negotiable)

> No production code, no backend, no database schema, no MVP feature work until the Step 8 decision is **GO**.
>
> "Building the landing page" does not mean a custom React app — use a no-code builder (see [no-code-tools.md](../../references/no-code-tools.md)). Writing your own auth or DB at this stage *is* the failure mode this skill exists to prevent.

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "I'll validate by just shipping the MVP — that's faster" | Building takes 2–6 months on average. Validation takes 8 steps. [CB Insights' post-mortem study](https://www.cbinsights.com/research/startup-failure-reasons-top/) found 42% of startups fail because there was no market need. |
| "I already know my audience wants this" | Then proving it with a landing page + 10 pre-orders should be trivial. If it isn't, you didn't know. |
| "My idea is too novel for a landing page to test" | If you can't describe it on a landing page, your prospects can't understand it either. That's a signal. |
| "I'll skip Steps 1–3 and just build a landing page" | Without a problem statement, a competitor read, and a value prop, the page won't convert and you'll learn nothing. |
| "Pre-sales feel scammy — I shouldn't ask for money before building" | Pre-sales with clear delivery dates and refunds are the strongest signal of intent. Email signups are vanity; payments are validation. |
| "I'll skip to coding — the validation is just a formality" | Then you don't need this skill. Close it and own the risk. |

## Red Flags

- User wants to `npm init` or write any backend code in steps 1–8
- "Would you use this?" appears in any survey or message (leading question — see [validation-pitfalls.md](../../references/validation-pitfalls.md#pitfall-1-leading-questions))
- Tracking only signups, not conversion or revenue
- Driving traffic from sources where the audience does not actually hang out
- Step 8 decision based on "vibes" instead of the metrics in the validation log

## Verification

Orchestration is done when:

- [ ] `validation-log.md` exists in the working directory and is filled in for every completed step
- [ ] Each step's exit criteria from its SKILL.md have been met before advancing
- [ ] On Step 8, a written GO / PIVOT / KILL decision exists with cited metrics
- [ ] If the decision is anything other than GO, no production code has been written
