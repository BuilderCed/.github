# Security Policy

## Reporting a Vulnerability

If you discover a security vulnerability, please report it responsibly:

1. **Do NOT** open a public issue
2. Use [GitHub Security Advisories](https://github.com/BuilderCed/.github/security/advisories/new) (preferred)
3. Include: description, steps to reproduce, impact assessment

## Response Timeline

- Acknowledgment: 48 hours
- Assessment: 5 business days
- Fix: depends on severity (critical: 24h, high: 7 days)

## Supported Versions

Only the latest version on `main` branch is supported with security updates.

## Security Measures

- All dependencies scanned by Dependabot (weekly, grouped)
- Secret scanning with push protection enabled (39+ secret types)
- Gitleaks + TruffleHog + Semgrep in CI (adaptive by risk level)
- GitHub Actions pinned to commit SHAs (not version tags)
- GITHUB_TOKEN least-privilege permissions per workflow
- Dependabot security updates auto-merged (patch/minor)
