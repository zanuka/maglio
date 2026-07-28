# AGENTS.md — Maglio

This file is the primary source of truth for any AI agent working on Maglio.

## Project Identity

Maglio is a **factory of factories** CLI.

It helps developers scaffold local agentic software factories — declarative blueprints that emit skills, stage harnesses, AGENTS.md contracts, circuit breakers, and handoff packages so coding agents can run structured plan → test → loop → review → explain workflows without constant human babysitting.

We are building this in public as open source.

Maglio complements Nocciolo (company-brain / durable knowledge). Nocciolo supplies context; Maglio shapes production systems that use it.

## Core Principles (non-negotiable)

1. **Local control first**  
   Factory configs, skills, and artifacts live in the user’s repo. Prefer self-hostable, version-controlled, offline-capable designs. Avoid forced cloud runtimes.

2. **Amplify existing craft**  
   Maglio does not replace tests, reviews, ADRs, or coding standards. It scaffolds agent workflows that run *inside* those standards.

3. **Comprehension-first**  
   Every meaningful factory design should reduce (or at least not increase) comprehension debt. Owner’s manuals, review stages, and evidence packages are first-class, not optional polish.

4. **Declarative over prompt theater**  
   Prefer explicit `factory.yaml` (or equivalent), stage files, and skills over fragile chat history or hidden prompt chains.

5. **Progressive autonomy**  
   Support light (human-in-the-loop) and overnight profiles from the same blueprint. Autonomy expands only when stop conditions and review gates are trusted.

6. **Recipes and stages as the contribution surface**  
   Prefer pluggable stages and shareable recipes over a monolithic closed pipeline. Make it easy for others to publish patterns without forking the core.

7. **Clear boundaries**  
   Maglio scaffolds and configures factories. It is not a general multi-agent runtime, not a memory product, and not a hosted “run everything for you” platform.

## Architecture Expectations

- TypeScript CLI (Node.js)
- Clean separation: schema / config → stage emitters → skill generators → validation / doctor
- Config lives in `.maglio/` (or equivalent) and is version-controlled
- Prefer explicit configuration over magic
- Scaffold output must be reviewable by a human before any agent runs it at scale
- Idempotent scaffold where practical (re-running should not thrash user edits without intent)

## Coding Standards

- Prefer small, composable functions and clear module boundaries
- Strong typing — avoid `any` unless there is a documented reason
- CLI commands should be idempotent where practical and support `--dry-run`
- Errors should be actionable (tell the user what to do next)
- No silent failures when generating stages, skills, or safety rails

## When Working on Factory / Stage Features

- Treat the declarative blueprint as the source of truth for what gets generated
- Stages should have clear inputs, outputs, and stop conditions
- Separate planning capability from execution capability in defaults when it matters (handoff model)
- Review stages should assume a fresh agent that did not build the work
- Prefer standards that existing tools already speak (`AGENTS.md`, common skill formats, MCP-friendly configs)

## Documentation & Public Development

- Keep the README and ROADMAP accurate
- Prefer updating living docs over leaving stale comments
- When adding a major capability, update the roadmap status
- Recipe and stage docs are part of the product

## What Agents Should Not Do

- Do not invent architecture patterns that contradict local-control or comprehension-first principles
- Do not expand scope into hosted multi-agent platforms, general agent marketplaces, or memory backends unless explicitly requested
- Do not make cloud-only or vendor-locked paths the default
- Do not generate factory configs that encourage agents to run without stop conditions or review gates
- Do not treat Maglio as a replacement for good engineering process — only as an amplifier of it

## Current Focus

See `ROADMAP.md`. At the time of writing we are in early foundation (Phase 0 → Phase 1: Core CLI + declarative blueprint).
