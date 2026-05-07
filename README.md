# template-base

Base template to bootstrap a standardized repository.

## Included standards

This template includes baseline files and automations for:

* Repository governance (`CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `LICENSE`)
* Release management with Semantic Versioning (SemVer) and changelog automation
* CI/CD with GitHub Actions
* `pre-commit` checks
* Dev Container setup
* Dependency automation with Dependabot and Renovate
* Backstage catalog metadata (`catalog-info.yaml`)
* Markdown-first linting and validation

## Release management

Releases are managed with [Release Please](https://github.com/googleapis/release-please):

1. Use Conventional Commits in merged pull requests.
2. Release Please opens/updates a release PR.
3. Merging the release PR updates `CHANGELOG.md`, creates a SemVer tag (`vX.Y.Z`), and publishes a GitHub release.

## CI/CD overview

* **CI** (`.github/workflows/ci.yml`): runs markdown and pre-commit validations on push/PR.
* **CD** (`.github/workflows/release-please.yml`): automates changelog + release publication.

## Quick start

```bash
pre-commit install
pre-commit run --all-files
```

If using VS Code, open the repo in the dev container for a ready-to-use environment.
