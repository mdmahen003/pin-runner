# pin-runner

Public repository that only contains GitHub Actions workflows and the secrets/variables they use.
All application code lives in the private `pin-core` repository, which every workflow checks out into `core/` with `CORE_PAT`.

- Secrets are passed to steps only through `env:` and are never echoed.
- Required repository **variables**: `CORE_REPO` (`owner/pin-core`), `CF_PAGES_PROJECT`.
- Full list of secrets/variables and where to get them: `pin-core/docs/SECRETS.md`.
- Phone-friendly setup (Bengali): `pin-core/docs/SETUP_BN.md`; daily/weekly routine: `pin-core/docs/RUNBOOK_BN.md`.

Workflows: `ci`, `daily-factory`, `schedule-feed`, `weekly-learn`, `weekly-products`, `export-csv`, `generate-topics`, `seed-bg-lib`, `db-migrate`, `deploy-site`, `deploy-image-worker`, `set-pages-secrets`, `set-telegram-webhook`, `heartbeat`.

> GitHub pauses scheduled workflows in a public repository after 60 days without repository activity.
> To resume: Actions → choose the workflow → **Enable workflow** (or push any small commit).
> Nothing in this repo commits automatically.
