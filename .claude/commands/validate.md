---
description: Start (or resume) the 8-step idea validation workflow for an indie hacker product idea — no code required.
---

Invoke the `validate-idea-orchestrator` skill.

If `validation-log.md` already exists in the working directory, resume from the latest completed step. Otherwise, start with Step 1.

Always:

- Maintain `validation-log.md` as the single source of truth.
- Route each step to its `step-N-*` skill — do not improvise.
- Refuse to write product code until the Step 8 verdict is **GO**.
- Use `customer-interviews` whenever talking to real users (Step 1, 6, 7).

Arguments after `/validate` (optional): treat as a one-sentence idea pitch and seed Step 1 with it.
