# Contributing to Maglio

Thanks for your interest in contributing. Maglio is being developed in public and we welcome thoughtful collaboration.

## Getting Started

1. Read the [README](./README.md) and [ROADMAP](./ROADMAP.md) to understand the current focus.
2. Review [AGENTS.md](./AGENTS.md) — it contains the project principles that apply to both human and AI contributors.
3. Look at open issues. Early-stage issues are the best place to start.

## Development Setup

Once the TypeScript CLI scaffold lands:

```bash
git clone <repo-url>
cd maglio
npm install
npm run build   # or the equivalent once defined
```

Exact scripts will be documented as the project structure stabilizes.

## How to Contribute

### Issues

- Search existing issues before opening a new one.
- Use clear titles and include reproduction steps or concrete examples when reporting bugs.
- For feature ideas, explain the problem you’re trying to solve and how it fits the current roadmap.

### Pull Requests

- Keep PRs focused. Small, reviewable changes are preferred over large ones.
- Update documentation (README, ROADMAP, AGENTS.md) when behavior or public surface changes.
- Prefer adding tests for core domain logic (factory schema, stage emitters, recipe loading) when practical.
- Follow the coding standards outlined in `AGENTS.md` and the Cursor rules.

### High-leverage contribution areas

While the foundation is forming, the most useful contributions are:

- Feedback on the declarative factory schema and stage model
- Starter recipes for common project shapes
- Clear examples of stop conditions and circuit breakers
- Documentation that helps someone scaffold their first factory

### Commit Messages

Use clear, conventional messages:

```
feat: add factory.yaml schema validation
fix: make scaffold idempotent when AGENTS.md already exists
docs: clarify light vs overnight profiles
chore: update dependencies
```

## Code of Conduct

Please read and follow our [Code of Conduct](./CODE_OF_CONDUCT.md).

## Questions

Open a discussion or issue. Early feedback on architecture and DX is especially valuable while the foundation is still forming.
