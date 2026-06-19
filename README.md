# validate-idea-skills

A pack of [Claude Code agent skills](https://github.com/addyosmani/agent-skills) that walks an indie hacker through validating a product idea in **8 steps, without writing any code** — competitor analysis, smoke tests, landing pages, pre-sales, and a hard go/no-go gate at the end.

Based on Larry Qu, [*Validate Your Indie Hacker Idea in 7 Days (Without Writing Code)*](https://calmops.com/indie-hackers/validate-idea-in-7-days-without-code/), CalmOps.

## What's inside

```
validate-idea-skills/
├── skills/
│   ├── validate-idea-orchestrator/   # Routes to the right step-skill, enforces the gate
│   ├── step-1-problem-and-audience/   # Problem statement, segments, watering holes
│   ├── step-2-competitor-analysis/    # Advantages/disadvantages of competitors, the gap
│   ├── step-3-value-proposition/      # Headline + 3 bullets + proof
│   ├── step-4-landing-page/           # No-code page, live on a custom domain
│   ├── step-5-smoke-test/             # Analytics + conversion event + fake door
│   ├── step-6-drive-traffic/          # Communities, outreach, Show HN
│   ├── step-7-pre-sell/               # Stripe payment links, real intent signal
│   ├── step-8-decide/                 # GO / PIVOT / KILL on quantitative thresholds
│   └── customer-interviews/          # 15-min Mom Test discovery script
├── references/
│   ├── validation-metrics.md         # Thresholds + validation log template
│   ├── no-code-tools.md              # Landing page / payment / analytics stack
│   └── validation-pitfalls.md        # Leading questions, vanity, sunk cost, etc.
├── agents/
│   └── validation-coach.md           # Spawnable coach persona
├── .claude/commands/
│   └── validate.md                   # /validate slash command
├── .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── LICENSE
└── README.md
```

## Install

### Claude Code (recommended)

Local / development:

```bash
git clone https://github.com/elcodabra/validate-idea-skills.git
claude --plugin-dir /path/to/validate-idea-skills
```

Marketplace (once published):

```
/plugin marketplace add elcodabra/validate-idea-skills
/plugin install validate-idea-skills@validate-idea-skills
```

### Other agents (Cursor, Gemini CLI, Windsurf, Codex, …)

Skills are plain Markdown — copy any `SKILL.md` into your agent's rules / skills directory, or reference the whole `skills/` folder. See [addyosmani/agent-skills](https://github.com/addyosmani/agent-skills) for per-tool setup notes.

## Use it

```
/validate
```

Or just say "validate my idea: [one sentence]" — the `validate-idea-orchestrator` skill auto-triggers.

The orchestrator:

1. Creates a `validation-log.md` in the working directory.
2. Routes you through Steps 1 → 8 using the matching skill at each step.
3. Enforces the rule that **no product code is written until the Step 8 decision is GO**.
4. Writes a quantitative GO / PIVOT / KILL verdict at the end.

## The 8-step map

| Step | Skill | Exit criteria |
|-----|-------|---------------|
| 1 | `step-1-problem-and-audience` | Problem statement + 2–3 segments + watering holes with verbatim quotes |
| 2 | `step-2-competitor-analysis` | Advantages/disadvantages per competitor + named gap + price band |
| 3 | `step-3-value-proposition` | Headline + 3 bullets + 1 real proof element |
| 4 | `step-4-landing-page` | Live page on a no-code builder + custom domain + stated price |
| 5 | `step-5-smoke-test` | Analytics + conversion event + UTM scheme + fake-door post-click |
| 6 | `step-6-drive-traffic` | ≥100 qualified visitors from ≥3 channels + 5 interview slots |
| 7 | `step-7-pre-sell` | Stripe link live + personal outreach + ≥3 declines logged |
| 8 | `step-8-decide` | Written GO / PIVOT / KILL backed by the validation log |

## The gate

> No production code, no backend, no schema, no MVP feature work until Step 8 says **GO**.

`spec-driven-development` (or whatever build skill you prefer) takes over only after a GO — and even then, scope is constrained to fulfilling the people who paid.

## Credits

- Larry Qu — original 7-step framework at CalmOps
- Addy Osmani — [agent-skills](https://github.com/addyosmani/agent-skills) structure and conventions this pack follows
- Rob Fitzpatrick — *The Mom Test* (basis of the `customer-interviews` skill)

## License

MIT — see [LICENSE](LICENSE).
