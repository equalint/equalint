---
okf:
  identity:
    id: local-agent-context-equalint
    title: Equalint Project Local Agent Context
    type: standard
    status: active
  ownership:
    owner: Ehab Khedr Fathy
    steward: Antigravity
  dates:
    created: 2026-07-12
    updated: 2026-07-14
  classification:
    track: project
    visibility: public
    sensitivity: level-1-sensitive
  location:
    workspace_path: AGENTS.md
    canonical_path: /Users/ekf/Downloads/Ehab Roadmap/06-Projects/equalint/AGENTS.md
  relationships:
    cli_package: packages/equalint/
    core_package: packages/core/
    config_package: packages/config/
    reporters_package: packages/reporters/
  review:
    checked_folder: /Users/ekf/Downloads/Ehab Roadmap/06-Projects/equalint
  next_action:
    summary: Define and implement CLI commands and core engine features
---

# Equalint Project Local Agent Context

## Purpose
This workspace holds the EquaLint accessibility evidence toolkit codebases (monorepo of CLI, Core, Config, and Reporters packages).

## Local Rules and Guidelines
1. **Monorepo Structure (pnpm Workspaces)**: Code execution and development are organized inside the `packages/` directory within a single git repository. Workspace packages are managed at the root using pnpm.
2. **JIRA-Style Workbook**: Plan all tasks in a local JIRA-style workbook (`workbook.md`) at the root of the project.
3. **Task Checklist**: Maintain a `task.md` file in the artifact directory/workbook to track progress.
4. **Git Workflow**:
   - Create a GitHub issue for each task.
   - Create a new branch (e.g., `feature/issue-<num>-<description>`) for each task.
   - Implement, test, and document all changes.
   - Create a Pull Request (PR) and merge it to `main`.
5. **Autonomy & Verification**: Verify all publish configurations, builds, and package setup before execution.

## Stop And Ask
If there are npm registry authentication or scope permission issues, stop and report them to the user with all steps needed from the user step by step.
