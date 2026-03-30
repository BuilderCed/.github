# BuilderCed CI/CD Infrastructure

Reusable workflows, templates, and community health files for 63+ repos.

## Reusable Workflows

| Workflow | Type | Description |
|----------|------|-------------|
| `reusable-ci-typescript.yml` | TypeScript/React/Next.js | lint + typecheck + test + build |
| `reusable-ci-python.yml` | Python | ruff + pytest + pip-audit |
| `reusable-ci-expo.yml` | React Native/Expo | lint + typecheck + test + expo-doctor |
| `reusable-ci-dart.yml` | Flutter/Dart | analyze + test |
| `reusable-ci-static.yml` | HTML/PWA | validate + size check + CSP |
| `reusable-security-scan.yml` | All | adaptive gitleaks + TruffleHog + Semgrep |
| `reusable-dependabot-auto-merge.yml` | All | patch/minor auto, major HITL |
| `reusable-pr-gate.yml` | All | description + size + conventional commits |
| `reusable-deploy-gh-pages.yml` | Static | full auto deploy |

## Usage

```yaml
# In your repo's .github/workflows/ci.yml
name: CI
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  ci:
    uses: BuilderCed/.github/.github/workflows/reusable-ci-typescript.yml@main
    with:
      node-version: '22'
      pnpm-version: '9'

  security:
    uses: BuilderCed/.github/.github/workflows/reusable-security-scan.yml@main

  pr-gate:
    if: github.event_name == 'pull_request'
    uses: BuilderCed/.github/.github/workflows/reusable-pr-gate.yml@main
```

## Templates

- `templates/coderabbit-template.yaml` — CodeRabbit FR config
- `templates/dependabot-template.yml` — Dependabot with grouping
- `templates/.gitattributes-template` — Line endings + binaries
- `templates/.editorconfig-template` — Formatting consistency
