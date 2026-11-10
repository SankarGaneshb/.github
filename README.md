# SankarGaneshb / .github

Welcome to the central community health, default templates, and open-source governance hub for all repositories owned by **[@SankarGaneshb](https://github.com/SankarGaneshb)**.

GitHub uses the files in this repository as **account-wide defaults** for all repositories under this profile that do not define their own.

---

## 🏛️ Central Standards & Included Defaults

| File / Directory | Purpose & Behavior |
| :--- | :--- |
| **[`.github/copilot-instructions.md`](.github/copilot-instructions.md)** | Universal rulebook for AI coding assistants (Antigravity, Copilot, Claude Code, Cursor) establishing PR-first branching, Green-on-Arrival CI, conventional commits, and container security. |
| **[`.github/workflows/reusable-pr-ack.yml`](.github/workflows/reusable-pr-ack.yml)** | Central **reusable workflow (`workflow_call`)** for automated PR acknowledgement across any repository. |
| **[`.github/dependabot.yml`](.github/dependabot.yml)** | Account-wide dependency scanning for GitHub Actions, Python (pip), Node.js (npm), Docker, and Rust (Cargo). |
| **[`.github/DISCUSSION_TEMPLATE/`](.github/DISCUSSION_TEMPLATE/)** | Pre-configured discussion forms for 💡 **Ideas & RFCs**, 🙌 **Show & Tell**, and 🙋 **Q&A**. |
| **[`.github/FUNDING.yml`](.github/FUNDING.yml)** | Automatically activates the "Sponsor this project" heart badge across all repositories. |
| **[`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/)** | Standardized YAML issue forms: 🐛 **Bug Reports**, 🚀 **Feature Requests**, and 💡 **RFC / Architecture Proposals**. |
| **[`.github/pull_request_template.md`](.github/pull_request_template.md)** | Standard Pull Request checklist ensuring verification, documentation, and clean commit standards. |
| **[`CONTRIBUTING.md`](CONTRIBUTING.md)** | Contributor guidelines outlining our PR-first branching model, Green-on-Arrival (GoA) CI expectations, and commit standards. |
| **[`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md)** | Contributor Covenant Code of Conduct v2.1 to foster an open, welcoming community. |
| **[`SECURITY.md`](SECURITY.md)** | Responsible disclosure instructions for reporting potential security vulnerabilities. |
| **[`workflow-templates/`](workflow-templates/)** | Official workflow templates (e.g. Contributor PR Acknowledgement) available in the GitHub Actions dashboard. |

---

## 🚀 Using the Central Reusable Workflows

Any repository under `@SankarGaneshb` can call our central workflows in just a few lines without duplicating logic:

### Contributor PR Acknowledgement
In any repository, create `.github/workflows/pr-acknowledgement.yml`:

```yaml
name: Contributor PR Acknowledgement

on:
  pull_request_target:
    types: [opened]

jobs:
  acknowledge:
    uses: SankarGaneshb/.github/.github/workflows/reusable-pr-ack.yml@main
    permissions:
      pull-requests: write
      issues: write
```

Whenever the acknowledgement message or security logic is updated here, all connected repositories benefit instantly.

---

## 🔄 The SankarGaneshb Contributor & AI Agent Lifecycle

All repositories under this profile adhere to a standard **Session-to-GitHub Lifecycle**:
1. **Formalize to Tracked Issues**: Concluded designs and AI pair-programming discussions are synthesized into tracked issues with clear acceptance criteria.
2. **PR-First Branching**: All modifications occur on `feat/*`, `fix/*`, or `docs/*` branches linked to tracked issues (`Closes #12`).
3. **Green-on-Arrival (GoA) CI**: Automated tests, linting, and health verification must pass 100% green before merging.
4. **Instant Contributor Acknowledgement**: Every external contribution is greeted immediately by our automated GitHub Actions hook.
