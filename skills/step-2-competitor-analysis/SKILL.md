---
name: step-2-competitor-analysis
description: Step 2 of the 8-step idea validation workflow — analyzes the existing competitors and alternatives for the Step 1 segments, building a head-to-head table of each one's advantages and disadvantages from links the user supplies. Use after Step 1 is signed off and before writing the value proposition. Use also when the user says "look at these competitors", "analyze this product", or pastes competitor URLs and wants to know where the gap is.
---

# Step 2: Competitor Analysis

## Overview

Before you can claim a value proposition, you need to know what the segment already uses and where those tools fall short. Step 2 takes the competitor and alternative links the user provides, analyzes each one's **advantages and disadvantages** for the Step 1 segment, and finds the gap your idea can own. The output directly feeds the Step 3 headline and its proof element.

"No competitors" is almost never true and is itself a red flag — if nobody is solving this, either the segment copes with a manual workaround (that *is* the competitor) or there is no demand. Name the alternative either way.

## When to Use

- Step 2 of the validation cycle, after [step-1-problem-and-audience](../step-1-problem-and-audience/SKILL.md) is signed off
- The user pastes competitor URLs and asks "what do you think of these?" / "where's the gap?"
- The Step 3 value proposition can't articulate "…without [the painful workaround]" because the alternatives haven't been mapped
- A landing page isn't converting and you suspect the offer isn't differentiated from what the segment already pays for

**Do NOT use when:** the user has already produced a competitor matrix with named advantages, disadvantages, and pricing per alternative, and an identified gap. Skip to [step-3-value-proposition](../step-3-value-proposition/SKILL.md).

## Process

### 1. Gather the links

Ask the user for the competitors and alternatives to analyze. Aim for **3–7**:

- Direct competitors (same job, same segment)
- Indirect alternatives (a different tool category that solves the same pain)
- The "do nothing" / manual workaround from the Step 1 problem statement (spreadsheet, email, agency, ignoring it)

If the user has fewer than 3, find the rest from the Step 1 watering holes — search the subreddits/forums for "alternative to", "vs", and "how do you currently handle".

> Send me the links (or names) of the competitors and alternatives you want analyzed — direct products, adjacent tools, and the manual workaround people use today.

### 2. Analyze each link

For each URL, fetch and read the landing page, pricing page, and (if quick) a few public reviews (G2, Capterra, Reddit, Trustpilot). Capture, per competitor:

| Field | What to capture |
|-------|-----------------|
| Name + URL | The link |
| Who they target | Their stated segment — is it your Step 1 segment or adjacent? |
| Price + model | Real numbers from the pricing page (free tier, $/mo, one-time, enterprise-only) |
| Advantages | 2–4 things they genuinely do well for the segment (be honest, not dismissive) |
| Disadvantages | 2–4 real weaknesses, ideally backed by a verbatim user complaint |
| Positioning quote | Their own one-line headline, copied verbatim |

Use real fetched content and cited reviews. **Do not invent weaknesses** to make your idea look better — wishful disadvantages are how founders talk themselves into a non-existent gap.

### 3. Build the comparison table

Collapse the per-competitor notes into one head-to-head table in the segment's terms:

| Capability / Axis | You (intended) | Competitor A | Competitor B | Workaround |
|-------------------|----------------|--------------|--------------|------------|
| Price | | | | |
| Time-to-value | | | | |
| [Axis that matters to the segment] | | | | |

Pick the axes the Step 1 segment actually cares about (from their verbatim quotes), not generic feature checkboxes.

### 4. Find the gap

From the disadvantages columns, name the **one underserved axis** you can own:

- A real disadvantage shared by the leaders that your idea removes
- Backed by at least one verbatim user complaint from a review or watering hole
- Narrow enough to fit in a headline ("…without [the thing they all get wrong]")

If you can't find a defensible gap — every competitor is cheaper, better, and loved — that is a **kill-or-pivot signal now**, not after you build. Surface it honestly.

### 5. Pricing reality check

Record the price band the segment already pays. Your Step 3 stated price and Step 7 pre-sell price must sit in a defensible position relative to this band — you can't price 10× the incumbents on a weaker product, and "free vs. their paid" tells you nothing about willingness to pay.

## Update the Validation Log

Add a `Step 2` section to `validation-log.md`:

- Per-competitor cards (name, URL, target, price, advantages, disadvantages, verbatim complaint)
- The head-to-head comparison table
- The named gap + the one axis you'll own, with its supporting quote
- The competitor price band

## Common Rationalizations

| Rationalization | Reality |
|---|---|
| "I have no competitors — this is totally new" | Then the segment copes some other way. The spreadsheet, the agency, or "doing nothing" is your competitor. Name it. |
| "I already know the competitors, I don't need to read their sites" | Their pricing and positioning change; your memory is months stale. Read the live page. |
| "Their reviews are all glowing, so there's no gap" | Then there may genuinely be no opening. That's the most valuable thing Step 2 can tell you — before you build. |
| "I'll just list their features" | Features aren't advantages. Frame every point as a benefit or pain *for the Step 1 segment*. |
| "I'll invent some weaknesses they probably have" | Wishful disadvantages produce a fake gap and a value prop that collapses on contact. Cite a real complaint or drop it. |

## Red Flags

- "No competitors" with no named manual workaround
- Advantages/disadvantages with no link or quote behind them
- Comparison axes are generic feature checkboxes, not what the Step 1 segment cares about
- The "gap" is a feature you want to build, not a pain the segment has voiced
- Pricing column left blank — you can't position on price you didn't read

## Verification

- [ ] 3–7 competitors/alternatives analyzed, including the manual workaround
- [ ] Each has real advantages, disadvantages, and a price from the live page (or marked N/A with reason)
- [ ] At least one disadvantage backed by a verbatim user complaint
- [ ] One defensible gap named on an axis the Step 1 segment cares about — or an honest "no clear gap" flagged
- [ ] Competitor price band recorded
- [ ] Validation log `Step 2` section committed before invoking [step-3-value-proposition](../step-3-value-proposition/SKILL.md)
