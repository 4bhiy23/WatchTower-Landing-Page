# Product

<!-- impeccable:product-schema 1 -->

## Platform

web

## Stack

Astro / Tailwind

## Users

Node.js and JavaScript/TypeScript developers, engineering leads, and open-source maintainers who manage npm/pnpm dependencies across repos and monorepos, needing calm, continuous dependency intelligence without noisy PR bots or third-party SaaS subscriptions.

## Product Purpose

Watchtower is a read-only dependency monitoring system for Node.js projects. It checks dependencies for stable updates, OSV security advisories, npm deprecations, monorepo workspace version mismatches, and daily changes—reporting exact facts without modifying source files or opening unsolicited pull requests.

## Positioning

Zero hosting cost, zero third-party lock-in, total data ownership. Unlike invasive SaaS dependency bots that create noise or require external permissions, Watchtower runs on your own GitHub Actions runners (or locally in VS Code) and keeps all history within your own repository.

## Operating Context

- Automated scheduled scans running on GitHub Actions cron.
- Standup-ready morning Telegram summary notifications.
- Optional static GitHub Pages or localhost-only Docker dashboard.
- In-editor dependency inspection inside VS Code during active development.

## Capabilities and Constraints

- **Two discrete products**:
  1. **Watchtower GitHub Template**: Forkable repo with scheduled GitHub Actions workflows, `config/projects.yml` configuration, repo-saved scan history, optional Telegram bot notifications, optional GitHub Pages dashboard, and private Docker mode.
  2. **Watchtower Dependency Monitor**: Standalone VS Code extension scanning active workspace for security advisories, major/routine updates, deprecations, and monorepo version alignment.
- **Strictly read-only**: Inspects manifests/lockfiles, queries official npm metadata and OSV advisories.
- **Negative constraints**: Never mention AI analysis, automatic package upgrades, automated pull requests, health scores, or drift scores.

## Brand Commitments

- Visual style: Dark charcoal/navy canvas, electric blue, cyan, violet, and subtle green accents.
- Typography: Strong sans-serif display/headings paired with clean monospace for code, versions, and terminal metadata.
- Tone: Calm, premium, developer-first, observability-inspired precision.
- Core trust promise: "Read-only · Zero hosting cost · Your data stays in your GitHub repository".

## Evidence on Hand

- GitHub Template repository: `https://github.com/4bhiy23/Watch-Tower-Public-Tempelate`
- VS Code Marketplace extension: `https://marketplace.visualstudio.com/items?itemName=4bhiy.watchtower-vscode`

## Product Principles

- **Report facts only**: Verified package versions, exact CVE/OSV IDs, clean changelogs.
- **Zero intrusion**: Never mutate repository code or open uninvited PRs.
- **Total privacy & ownership**: Runs on temporary runners or local machine; data stays in user's repo.
- **High-signal observability**: Distinguish major breaking changes from routine updates and security vulnerabilities at a glance.

## Accessibility & Inclusion

- Semantic HTML landmarks and full keyboard navigation.
- High-contrast color palette meeting WCAG 2.1 AA/AAA standards.
- Clear status indicators with text/icon reinforcement (not color alone).
- Respect `prefers-reduced-motion`.
