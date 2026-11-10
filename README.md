# SankarGaneshb / .github

Welcome to the central community health, default templates, and open-source governance hub for all repositories owned by **[@SankarGaneshb](https://github.com/SankarGaneshb)**.

GitHub uses the files in this repository as **account-wide defaults** for all repositories under this profile that do not define their own:

---

## 🏛️ Central Standards & Included Defaults

| File / Directory | Purpose & Behavior |
| :--- | :--- |
| **[`.github/FUNDING.yml`](.github/FUNDING.yml)** | Automatically activates the "Sponsor this project" heart badge across all repositories. |
| **[`.github/ISSUE_TEMPLATE/`](.github/ISSUE_TEMPLATE/)** | Provides standardized issue forms: 🐛 **Bug Reports**, 🚀 **Feature Requests**, and 💡 **RFC / Architecture Proposals**. |
| **[`.github/pull_request_template.md`](.github/pull_request_template.md)** | Standard Pull Request checklist ensuring verification, documentation, and clean commit standards. |
| **[`CONTRIBUTING.md`](CONTRIBUTING.md)** | Contributor guidelines outlining our PR-first branching model, Green-on-Arrival (GoA) CI expectations, and commit standards. |
| **[`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md)** | Contributor Covenant Code of Conduct v2.1 to foster an open, welcoming community. |
| **[`SECURITY.md`](SECURITY.md)** | Responsible disclosure instructions for reporting potential security vulnerabilities. |
| **[`workflow-templates/`](workflow-templates/)** | Official workflow templates (e.g. Contributor PR Acknowledgement) available in the GitHub Actions dashboard. |

---

## 🔄 The SankarGaneshb Contributor & AI Agent Lifecycle

All repositories under this profile adhere to a standard **Session-to-GitHub Lifecycle**:
1. **Formalize to Tracked Issues**: Concluded designs and AI pair-programming discussions are synthesized into tracked issues with clear acceptance criteria.
2. **PR-First Branching**: All modifications occur on `feat/*`, `fix/*`, or `docs/*` branches linked to tracked issues (`Closes #12`).
3. **Green-on-Arrival (GoA) CI**: Automated tests, linting, and health verification must pass 100% green before merging.
4. **Instant Contributor Acknowledgement**: Every external contribution is greeted immediately by our automated GitHub Actions hook.
