# Control‑M + GitHub Actions + Codespaces starter

This repo demonstrates a starter integration pattern between Control‑M Automation API (ctm-cli / REST) and GitHub Actions, with a Codespaces devcontainer for local development.

What’s included
- Codespaces devcontainer that installs `ctm` CLI, `jq`, `curl`, Python 3.12 and Java 21.
- Example GitHub Actions workflows:
  - `ci-cd-with-controlm.yml` — uses Automation API REST (token + polling).
  - `ctm-cli-deploy.yml` — installs `ctm` CLI and runs `ctm login`, `ctm deploy`, `ctm run`.
- `scripts/install-ctm-cli.sh` — helper to install ctm-cli (edit the download URL).
- `controlm/jobs/example-job.json` — example jobs-as-code payload.

Secrets required (add to GitHub repo secrets):
- CTM_HOST — Control‑M Automation API host (no https prefix)
- CTM_USER — CI user
- CTM_PASS — CI password
- (Optional) CTM_TOKEN — if you prefer static token auth
