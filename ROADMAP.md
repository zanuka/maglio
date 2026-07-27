# Maglio Roadmap

High-level phased plan. This is a living document — priorities will shift based on real usage and feedback as we build in public.

## Phase 0 — Foundation (Now)

- [x] Name and vision locked (Maglio)
- [x] README + roadmap
- [ ] Repository created and public
- [ ] Basic TypeScript CLI skeleton
- [ ] MIT license, contributing guidelines, CODE_OF_CONDUCT
- [ ] GitHub issue templates and project board for public development

**Goal:** Clean starting point that makes the “factory of factories” vision obvious and invites early feedback.

## Phase 1 — Core CLI + Declarative Blueprint

- [ ] `maglio init` — detect project root, scaffold `.maglio/` and a starter `factory.yaml`
- [ ] Declarative factory schema (stages, profiles, safety rails, model roles)
- [ ] Sensible defaults for a typical full-stack / web project
- [ ] `maglio doctor` — validate config and required files
- [ ] Dry-run support on all mutating commands

**Goal:** A developer can run `maglio init` and understand the shape of their future assembly line in under a minute.

## Phase 2 — Scaffold: Skills, Stages, and AGENTS.md

- [ ] Stage emitters for the core line: plan → tasks/tests → handoff → loop → review → explain
- [ ] Skill / slash-command generation compatible with common agent harnesses (Cursor, Claude Code, and similar)
- [ ] `AGENTS.md` generation or safe merge that describes the factory contract
- [ ] Circuit-breaker and stop-condition templates
- [ ] Light vs overnight profile support in the same blueprint

**Goal:** `maglio scaffold` produces a usable, local factory that an existing coding agent can already run against.

## Phase 3 — Recipes and Contribution Surface

- [ ] Recipe format (shareable stage sets + defaults)
- [ ] Built-in starter recipes (solo full-stack, small team, documentation-heavy, etc.)
- [ ] Documented extension points for custom stages
- [ ] Contribution guide focused on recipes and stage modules
- [ ] Example factory configs in the repo

**Goal:** Other developers can publish and reuse factory patterns without forking Maglio.

## Phase 4 — Comprehension & Evidence

- [ ] Owner’s manual generation / update stage
- [ ] Review-stage contract (fresh agent, plan re-check, test re-run)
- [ ] Evidence package hooks (what was proven, what failed, what was deferred)
- [ ] Optional proof / demo stage interface (browser or recorded walkthrough — pluggable)
- [ ] Simple metrics for comprehension debt (files touched vs explained)

**Goal:** Factory runs leave behind understanding and evidence, not only code.

## Phase 5 — Reliability, Integration, and DX

- [ ] Stronger schema validation and migration helpers
- [ ] Status / inspect commands for the current factory state
- [ ] MCP-friendly emission of factory tools or stage metadata
- [ ] Test coverage for scaffold and recipe logic
- [ ] Expanded documentation and real-project examples
- [ ] Optional deeper integration with Nocciolo (knowledge-aware planning defaults)

**Goal:** Maglio feels solid enough for daily use and for others to build on.

## Phase 6 — Advanced Autonomy (Later)

- [ ] Event-driven or scheduled factory triggers
- [ ] Multi-repo / multi-package factory profiles
- [ ] Self-improving meta-loop (factory that proposes improvements to its own blueprint)
- [ ] Richer model-routing policies (planning vs execution vs review)
- [ ] Lightweight inspection UI only if the CLI path is already excellent

**Goal:** Support high-autonomy local factories without abandoning the local-control and comprehension principles.

---

### Guiding Constraints

- Prefer local control and version-controlled factory configs
- Amplify existing engineering practices (tests, reviews, ADRs, clear architecture) rather than replace them
- Keep the CLI fast and the happy path short
- Treat recipes and stages as the primary contribution surface
- Stay complementary to knowledge systems (Nocciolo and others); do not become a second memory product
- Optimize for comprehension and safety rails, not only raw throughput

Feedback and real-world usage will reshape this plan. Open issues or discussions are the best way to influence direction.
