# CLAUDE.md: DevOps / SRE / Platform Engineer

<!-- For: people managing infrastructure, CI/CD, cloud, containers, and production reliability. -->

## Principles
- **Safety first.** Production changes are risky by default. Always show what a command or plan will change before running it.
- **Everything as code.** Use infrastructure as code, config in version control, and no manual console changes. If a manual step is unavoidable, document it.
- **Reversible changes.** Every change needs a rollback plan. Prefer gradual rollouts (canary, feature flags) to big-bang changes.

## Commands
- Never run destructive or production-affecting commands without explicit confirmation. That includes `terraform apply`, `kubectl delete`, `DROP`, `rm -rf`, force pushes, and scaling to zero.
- Use dry-run, plan, or diff modes first (`terraform plan`, `kubectl diff`, `--dry-run`).
- Name the target environment explicitly in every command. Never rely on the default context or profile.

## Configuration
- Pin versions: images by tag or digest, providers, actions, packages.
- Use least-privilege IAM. No wildcard permissions without a written reason.
- Secrets live in a secret manager. Never put them in code, logs, CI output, or Terraform state outputs.
- Add resource requests and limits, health checks, and readiness probes for every service.

## Observability
- New services ship with structured logs, key metrics (the RED or USE method), and alerts that are actionable. Every alert needs a runbook link.

## Incidents
- When debugging production, gather evidence first (logs, metrics, recent deploys). Form a hypothesis, then test it. Mitigate first, find the root cause later.
- Write blameless postmortems: a timeline, the impact, the root cause, and action items with owners.

## Project specifics
<!-- Cloud provider, IaC tool, CI system, cluster/environments, on-call docs. -->
