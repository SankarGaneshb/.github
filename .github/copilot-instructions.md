# Universal Copilot & AI Agent Instructions

> **Repository Profile**: `@SankarGaneshb`  
> **Scope**: Applies to all AI pair-programming agents (Antigravity, GitHub Copilot, Claude Code, Cursor, Codex) interacting with any repository under this profile.

---

## 🧭 Core Principles

1. **Session-to-GitHub Formalization**:
   - Concluded design sessions and architectural decisions must be synthesized into tracked GitHub Issues (`bug_report.yml`, `feature_request.yml`, `rfc_proposal.yml`) or Architecture Decision Records (ADRs under `docs/decisions/`).
   - Do not leave critical conclusions locked in ephemeral transcripts.

2. **PR-First Branching (Never Push to `main`)**:
   - Always branch off `main` (or `master`) using standard naming:
     - `feat/<issue-number>-<short-description>`
     - `fix/<issue-number>-<short-description>`
     - `docs/<issue-number>-<short-description>`
   - Link Pull Requests to their tracked issue using keywords (e.g., `Closes #12`).

3. **Green-on-Arrival (GoA) Verification**:
   - All tests across the CI matrix must pass cleanly (`100% green`) before considering any task complete.
   - Maintain high test coverage (minimum 90% on newly written code).
   - Never skip, comment out, or weaken failing assertions to force CI green.

4. **Conventional Commits**:
   - Commit messages must follow [Conventional Commits](https://www.conventionalcommits.org/):
     - `feat(<scope>): <description>`
     - `fix(<scope>): <description>`
     - `docs(<scope>): <description>`
     - `refactor(<scope>): <description>`
     - `test(<scope>): <description>`
     - `chore(<scope>): <description>`

---

## 🛠️ Polyglot Engineering Standards

* **Python**:
  - Prefer modern Python 3.10+ features, strict typing (`typing.Optional`, `typing.List`, `typing.Dict`), and Pydantic models for configuration/data contracts.
  - Manage dependencies via `pyproject.toml` or pinned `requirements.txt`.
* **TypeScript / Node.js**:
  - Strict mode enabled in `tsconfig.json`.
  - Use modern ES modules and clean asynchronous `async/await` handling.
* **Rust**:
  - Idiomatic error handling via `Result<T, E>` and `thiserror` / `anyhow`.
  - Separate `[dependencies]` from `[dev-dependencies]` and strip release binaries.
* **.NET / C#**:
  - Target modern LTS (.NET 8+), prefer nullable reference types, and keep tests isolated in xUnit/NUnit.

---

## 🐳 Containerization & Security Standards

1. **Non-Root Execution**:
   - All Docker containers must run as an unprivileged non-root user (e.g. `appuser` with explicit UID `10001`).
2. **Multi-Stage Synthesis**:
   - Separate build/compilation tooling from the lightweight final runtime layer (`*-slim`, `distroless`, or `alpine`).
3. **Secret Hygiene**:
   - Never hardcode API keys, tokens, or credentials in source code or commit histories.
   - Use environment variables or GitHub Secrets exclusively.
