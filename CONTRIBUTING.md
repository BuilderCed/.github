# Contributing

## Branch Strategy

- `main` — production (protected by rulesets)
- `feat/*` — new features
- `fix/*` — bug fixes

## Commit Convention

```
<type>(<scope>): <description>

Types: feat | fix | docs | style | refactor | perf | test | chore | ci | build
```

## Pull Request Requirements

- [ ] Meaningful description (min 20 chars)
- [ ] Conventional Commits title
- [ ] Size < 1000 lines (split if larger)
- [ ] Tests passing
- [ ] No secrets in code
- [ ] CodeRabbit review addressed (T1 repos)

## Code Standards

- **TypeScript**: strict mode, no `any`, Zod at boundaries, error handling
- **Python**: type hints, ruff lint, pytest, pip-audit clean
- **All**: no TODOs in production code, self-documenting naming
