# Maglio

**The forge hammer for agentic software factories.**

Scaffold local production lines of skills, loops, harnesses, and handoff packages so coding agents can run structured work overnight — without babysitting prompts all day.

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![Status: Early](https://img.shields.io/badge/Status-Early%20%2F%20Public-orange)]()

---

## The Problem

Coding agents made writing code easier. The harder problem is building a system that can context-engineer, plan, execute, test, review, and explain itself.

Most “software factory” approaches today are either:

- One person’s private skill stack that is hard to reuse
- Cloud platforms that own the loop and the data
- Naive backlog loops ("slop cannons") that pump out unverified PRs nobody trusts or reads
- Prompt-chasing sessions that collapse the moment the human steps away

Developers who want **local control**, durable standards, and progressive autonomy still have to reinvent the assembly line every time.
Git and `.maglio/` can centralize team factory knowledge without locking you into a proprietary cloud runtime.

## The Vision

Maglio is a **factory of factories**.

It is a CLI that turns a declarative factory blueprint into the concrete files your agents already understand:

- Skills and slash commands
- `AGENTS.md` and project rules
- Stage harnesses with conditional routing (triage -> spec -> plan -> tasks -> tests -> handoff -> loop -> review -> explain)
- Circuit breakers, human judgment gates, and stop conditions
- Work orders that separate high-capability planning from lower-cost execution
- Merge risk assessments, owner’s manuals, and evidence packages so you know what to trust and still understand what was built

Maglio does not run your factory for you. It gives you the tools to stand one up that fits *your* repo, *your* standards, and *your* tolerance for autonomy.

It is designed to sit next to [Nocciolo](https://github.com/) — the company-brain / knowledge layer. Nocciolo supplies durable context; Maglio shapes that context into a production system.

## How Maglio Helps Developers

### A) Give developers a real starting point
Instead of copying someone else’s private `/factory` skill and hoping it fits, you get a configurable scaffold:

```bash
maglio init          # detect project, create factory config
maglio scaffold      # emit skills, AGENTS.md, stage files, stop conditions
maglio doctor        # validate the assembly line
maglio graph         # visualize the blueprint as a Mermaid or ASCII diagram
```

You choose the stages, the models for planning vs execution, the safety rails, and how far autonomy is allowed to go. Daytime “light factory” and overnight “full loop” can be different profiles of the same system.

### B) Encourage open-source contributions
Maglio is built as a **recipe and stage system**, not a closed product:

- Pluggable stages (plan, tests, handoff, loop, review, explain, proof…)
- Community recipes for common stacks and team shapes
- Standards-first artifacts (`AGENTS.md`, skill formats, MCP-friendly configs)
- Clear extension points so others can publish stages without forking the core

The goal is a shared library of factory patterns that any developer can adopt, adapt, and improve.

### C) Innovate on software-factory practice
Existing factories often optimize for “ship more code while I sleep.” Maglio optimizes for four additional properties:

1. **Human judgment gates before code** - triage ambiguous work into an interactive spec step instead of letting agents vibe out product decisions
2. **Risk-scored, evidence-backed PRs** - assess merge risk (alignment, blast radius, verification, rollback cost, error detection) pre-PR so reviewers know what needs close scrutiny
3. **Comprehension-first** - every factory run should leave behind plain-language explanation and verification proof, not just diffs
4. **Declarative, local, and progressive** - the factory is version-controlled config + files in the repo, starting human-in-the-loop and expanding autonomy only when stop conditions and review gates are trusted

Circuit breakers, separate planning vs execution models, independent review agents, merge risk rubrics, and owner’s manuals are first-class, not afterthoughts.

## What Maglio Produces

Typical scaffold output (exact layout will evolve):

```
.maglio/
  factory.yaml          # declarative blueprint
  stages/               # plan, tests, handoff, loop, review, explain…
  recipes/              # optional shared or local recipes
skills/                 # generated or linked skills for Cursor / Claude Code / etc.
AGENTS.md               # updated or generated agent instructions
docs/
  factory-owner-manual.md
```

The concrete skill names and stage set are configurable. Maglio’s job is to make the *structure* repeatable and reviewable.

## Core Principles

- **Local control** — no forced cloud runtime; the factory lives in your repo and your tools
- **Amplify craft** — clear architecture, tests, reviews, and ADRs remain the source of truth; agents run inside those standards
- **Progressive autonomy** — light daytime profiles and full overnight profiles from the same blueprint
- **Comprehension debt is real** — every meaningful run should reduce (or at least not increase) the gap between what the agent built and what you understand
- **Standards over magic** — prefer `AGENTS.md`, skills, and MCP surfaces that other tools already speak
- **Complement, don’t compete** — Maglio scaffolds factories; it does not try to be the only agent runtime or the only memory system

## Status

Maglio is in the earliest public stage. We are building in the open.

See [ROADMAP.md](./ROADMAP.md) for the phased plan.

## Relationship to Nocciolo

| Layer        | Project   | Role                                      |
|--------------|-----------|-------------------------------------------|
| Knowledge    | Nocciolo  | Durable company brain / memory config    |
| Production   | Maglio    | Factory scaffold and assembly-line config |

Use them together or independently. Maglio assumes good project knowledge exists; Nocciolo helps make that knowledge agent-usable.

## Contributing

Issues, ideas, and early design feedback are welcome. Once the CLI skeleton lands, small focused PRs on stages, recipes, and docs will be the highest-leverage contributions.

## License

MIT
