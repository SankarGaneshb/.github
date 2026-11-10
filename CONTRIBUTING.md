# Contributing to SankarGaneshb Projects

Thank you for your interest in contributing to our open-source projects! We welcome bug reports, feature suggestions, architecture proposals, and pull requests.

---

## 🛠️ Contributor Guidelines

### 1. Branching & PR-First Model
To maintain full traceability and clean project management across all repositories:
* **Never push directly to `main` (or `master`)**.
* Always create a dedicated branch following standard naming conventions:
  * `feat/<issue-number>-<short-description>`
  * `fix/<issue-number>-<short-description>`
  * `docs/<issue-number>-<short-description>`
* Link your pull request to the corresponding issue in the description (e.g., `Closes #12`).

### 2. Green-on-Arrival (GoA) CI Verification
* All Pull Requests must pass the repository's continuous integration pipeline (tests, linting, and security audits) with 100% green status before merging.
* New features should maintain high test coverage and include corresponding unit or integration tests.

### 3. Commit Message Standards
We follow [Conventional Commits](https://www.conventionalcommits.org/):
* `feat:` A new feature or capability
* `fix:` A bug fix
* `docs:` Documentation changes only
* `refactor:` Code changes that neither fix a bug nor add a feature
* `test:` Adding or updating tests
* `chore:` Maintenance, dependency updates, or tooling configuration

### 4. Automated Contributor Acknowledgement
Every incoming Pull Request is greeted instantly by our automated GitHub Actions workflow (`.github/workflows/pr-acknowledgement.yml`) to ensure quick acknowledgement and clear feedback.
