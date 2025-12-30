# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This is a **GitHub Profile README** repository. The README.md file is automatically displayed on the GitHub profile page at github.com/BrunoCerberus.

## Key Files

- `README.md` - The profile content displayed on GitHub (Markdown with embedded SVGs and badges)
- `github-metrics.svg` - Auto-generated metrics visualization (do not edit manually)
- `profile-3d-contrib/` - Auto-generated 3D contribution calendar SVGs (do not edit manually)

## GitHub Actions Workflows

Two workflows run daily at midnight and on push to master:

**3D Contribution Calendar** (`.github/workflows/3d-contrib.yml`)
- Uses `yoshi389111/github-profile-3d-contrib@0.7.1`
- Generates 3D contribution visualizations in `profile-3d-contrib/`

**GitHub Metrics** (`.github/workflows/metrics.yml`)
- Uses `lowlighter/metrics@latest`
- Generates `github-metrics.svg` with activity stats, isocalendar, and language breakdown
- Timezone: America/Sao_Paulo

## Commands

Manually trigger workflow updates:
```bash
gh workflow run "Generate 3D Contribution Calendar"
gh workflow run "Generate GitHub Metrics"
```

## Self-Hosted Vercel Services

**github-readme-stats** (Analytics section)
- Deployed at: `github-readme-stats-one-lake-78.vercel.app`
- Forked from: `anuraghazra/github-readme-stats`
- Vercel project: `brunocerberus' projects` → `github-readme-stats`
- Required env variable: `PAT_1` (GitHub Personal Access Token, no scopes needed)

If stats stop working, check the Vercel deployment and ensure `PAT_1` is set.

## Notes

- Generated SVG files are committed automatically by GitHub Actions
- The README uses external badge services (shields.io, capsule-render, skillicons.dev) for dynamic content
- Profile displays iOS development focus with Swift, SwiftUI, UIKit, and Clean Architecture emphasis
