# Workflows

Drop-in GitHub Actions workflows for any project.

## What's included

| Workflow | Trigger | What it does |
|----------|---------|--------------|
| `auto-tag.yml` | Push to `main` | Scans commits (Conventional Commits), creates semver tag |
| `release.yml` | Release created | Builds + uploads assets to GitHub release |
| `pr-lint.yml` | PR opened/edited | Validates PR title follows Conventional Commits |

## Install

```bash
# From your project root
mkdir -p .github/workflows
curl -sL https://raw.githubusercontent.com/dvos-tools/workflows/main/.github/workflows/auto-tag.yml -o .github/workflows/auto-tag.yml
curl -sL https://raw.githubusercontent.com/dvos-tools/workflows/main/.github/workflows/release.yml -o .github/workflows/release.yml
curl -sL https://raw.githubusercontent.com/dvos-tools/workflows/main/.github/workflows/pr-lint.yml -o .github/workflows/pr-lint.yml
```

Or just copy the files from `.github/workflows/` into your project.

## Setup

- **auto-tag** and **pr-lint** work out of the box
- **release.yml** needs your build steps — look for the `YOUR BUILD STEPS HERE` placeholder and replace it
