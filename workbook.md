# EquaLint Project Workbook

## EPIC-001: Publish Core Package to NPM as `@equalint/core`

### Status: Done
**Assignee:** Antigravity
**Reporter:** Ehab Khedr Fathy
**Priority:** High

### Description
The core package inside `06-Projects/equalint/core` needs to be published to NPM under the scope `@equalint/core`. Currently, the package is named `core` in `package.json`, which conflicts with the public npm package namespace and causes publishing failures.

### Acceptance Criteria
1. [x] A GitHub issue is created on `equalint/core` for the publishing task.
2. [x] A feature branch is created for the task in the `equalint/core` repository.
3. [x] `package.json` in `core` is updated to name `@equalint/core`.
4. [x] `.npmignore` is configured correctly to prevent unnecessary files from being published.
5. [x] Package is validated locally (e.g. dry-run package packing/listing).
6. [x] Package is successfully published to npm as `@equalint/core`.
7. [x] A PR is created and merged to `main` for the changes.
8. [x] A walkthrough/report is generated and updated in the project documentation.

---

## Tasks & Sub-Tasks

### [EQL-1] Repository & Issue Setup
- **Status:** Done
- **Action:** Create GitHub issue and checkout a feature branch in `core`.

### [EQL-2] Configuration Update
- **Status:** Done
- **Action:** Update package name in `package.json` and configure `.npmignore` to exclude development-only files.

### [EQL-3] Local Validation
- **Status:** Done
- **Action:** Dry-run the package using `npm pack` to check contents.

### [EQL-4] Package Publishing
- **Status:** Done
- **Action:** Run `npm publish` to publish `@equalint/core`.

### [EQL-5] PR & Clean Up
- **Status:** Done
- **Action:** Create a pull request, merge the branch into `main`, and clean up.

---

## EPIC-002: Bootstrap and Integrate `@equalint/config` Package

### Status: Done
**Assignee:** Antigravity
**Reporter:** Ehab Khedr Fathy
**Priority:** High

### Description
Bootstrap the `@equalint/config` package locally and integrate it with the remote repository on GitHub, fixing package.json and adding missing entrypoint index.js.

### Acceptance Criteria
1. [x] A GitHub issue is created on `equalint/config`.
2. [x] A feature branch is checked out locally.
3. [x] `publicConfig` in `package.json` is corrected to `publishConfig`.
4. [x] Missing entrypoint `index.js` is added.
5. [x] Divergence between local and remote git repositories is resolved via pull rebase.
6. [x] Changes are committed, pushed, PR created, and merged to `main`.
7. [x] Walkthrough report is updated.

---

## Tasks & Sub-Tasks

### [EQL-6] Repository & Git Issue Setup
- **Status:** Done
- **Action:** Create GitHub issue and checkout a feature branch in `config`.

### [EQL-7] Bug Fixes & Entrypoint
- **Status:** Done
- **Action:** Correct package.json configuration and add placeholder index.js.

### [EQL-8] Git Integration & Merge
- **Status:** Done
- **Action:** Pull remote commits with rebase, push changes, create PR and merge to `main`.

---

## EPIC-003: Bootstrap and Integrate `@equalint/reporters` Package

### Status: Done
**Assignee:** Antigravity
**Reporter:** Ehab Khedr Fathy
**Priority:** High

### Description
Create a new package called `@equalint/reporters` inside the `reporters` workspace folder. Initialize npm configuration, configure git, create the remote GitHub repository under the `equalint` organization, and make it ready for public publishing.

### Acceptance Criteria
1. [x] A public GitHub repository `equalint/reporters` is created under the `equalint` organization.
2. [x] The local directory `reporters/` is created, git-initialized, and connected to the remote repository.
3. [x] A local feature branch `feature/issue-1-bootstrap-reporters` is created.
4. [x] `package.json` is initialized with `@equalint/reporters`, `"publishConfig": {"access": "public"}`, correct repository url, keywords, author, and `AGPL-3.0-only` license.
5. [x] A placeholder entrypoint `index.js`, `.npmignore`, `.gitignore`, and `README.md` are created.
6. [x] Git commits are pushed to the remote repository, a pull request is created, and merged into `main`.
7. [x] Walkthrough report is updated.

---

## Tasks & Sub-Tasks

### [EQL-9] Directory, Git Repo, & Branch Creation
- **Status:** Done
- **Action:** Create directory, create GitHub repository, initialize git locally, connect remote, and checkout feature branch.

### [EQL-10] Package Configuration
- **Status:** Done
- **Action:** Create package.json, index.js, README.md, .gitignore, and .npmignore.

### [EQL-11] Git Workflow & Clean Up
- **Status:** Done
- **Action:** Commit, push to feature branch, create PR, merge to `main`, and clean up.

---

## EPIC-004: Monorepo Workspaces Consolidation

### Status: Done
**Assignee:** Antigravity
**Reporter:** Ehab Khedr Fathy
**Priority:** High

### Description
Consolidate separate packages (`cli`, `core`, `config`, `reporters`) into a single Git repository workspaces monorepo structure.

### Acceptance Criteria
1. [x] GitHub repository `equalint/cli` is renamed to `equalint/equalint`.
2. [x] The `.git` repository folder is moved to the parent directory and remote URL is updated.
3. [x] All packages are consolidated under `packages/` directory.
4. [x] Root `package.json` defines workspaces `["packages/*"]` and is private.
5. [x] `packages/equalint/package.json` dependencies point to the workspace packages (`*`).
6. [x] `npm install` is run at the root to link the workspace packages successfully.
7. [x] Commits are pushed, a pull request is created, and merged into `main`.
8. [x] Walkthrough report is updated.

---

## Tasks & Sub-Tasks

### [EQL-12] Codebase Reorganization & Configuration
- **Status:** Done
- **Action:** Rename GitHub repo, migrate git, move sub-packages under `packages/`, configure root package.json and workspace dependencies.

### [EQL-13] Workspace Linking & Testing
- **Status:** Done
- **Action:** Run npm install to link packages locally and verify structure.

### [EQL-14] PR & Merge
- **Status:** Done
- **Action:** Commit, push feature branch, create PR, and merge to `main`.

---

## EPIC-005: pnpm Native Workspaces Migration

### Status: Done
**Assignee:** Antigravity
**Reporter:** Ehab Khedr Fathy
**Priority:** High

### Description
Transition the workspaces monorepo package manager from plain npm to pnpm native.

### Acceptance Criteria
1. [x] Remove npm lockfile `package-lock.json`.
2. [x] Remove workspaces configuration from root `package.json`.
3. [x] Create a root `pnpm-workspace.yaml` specifying workspaces packages.
4. [x] Configure local dependencies in `packages/equalint/package.json` to use `workspace:*`.
5. [x] Run `pnpm install` at root to generate `pnpm-lock.yaml`.
6. [x] Commits are pushed, a pull request is created, and merged into `main`.
7. [x] Walkthrough report is updated.

---

## Tasks & Sub-Tasks

### [EQL-15] Workspaces Manager Transition
- **Status:** Done
- **Action:** Delete package-lock.json, remove npm workspaces config, create pnpm-workspace.yaml, and update packages/equalint dependencies to workspace:*.

### [EQL-16] Native Installation & Lockfile Setup
- **Status:** Done
- **Action:** Run pnpm install to link workspaces and create pnpm-lock.yaml.

### [EQL-17] PR & Merge
- **Status:** Done
- **Action:** Commit, push branch, create PR and merge to `main`.

---

## EPIC-006: Update AGENTS.md for Monorepo Workspace Structure

### Status: Done
**Assignee:** Antigravity
**Reporter:** Ehab Khedr Fathy
**Priority:** Medium

### Description
Update the project's local agent context in `AGENTS.md` to reflect the progress and new monorepo layout (pnpm workspaces structure with sub-packages inside `packages/`).

### Acceptance Criteria
1. [x] A GitHub issue is created on `equalint/equalint`.
2. [x] A feature branch `feature/issue-5-update-agents` is checked out locally.
3. [x] Update `okf.dates.updated` to `2026-07-14`.
4. [x] Update relationships in the YAML frontmatter to point to the packages under `packages/` directory instead of root packages.
5. [x] Update the rules and next actions to reflect the monorepo structure and the completion of the transition epics.
6. [x] Push branch, create PR, and merge to `main`.

---

## Tasks & Sub-Tasks

### [EQL-18] Issue & Branch Setup
- **Status:** Done
- **Action:** Create issue #5 on GitHub and checkout feature branch.

### [EQL-19] AGENTS.md Updating
- **Status:** Done
- **Action:** Update relationships, updated date, and rules in AGENTS.md to match the pnpm monorepo structure.

### [EQL-20] PR & Merge
- **Status:** Done
- **Action:** Push, create PR, and merge to `main`.



