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
    updated: 2026-07-12
  classification:
    track: project
    visibility: private
    sensitivity: level-2-sensitive
  location:
    workspace_path: AGENTS.md
    canonical_path: /Users/ekf/Downloads/Ehab Roadmap/06-Projects/equalint/AGENTS.md
  relationships:
    core_package: core/
    cli_package: cli/
  review:
    checked_folder: /Users/ekf/Downloads/Ehab Roadmap/06-Projects/equalint
  next_action:
    summary: Publish core package to npm as @equalint/core
---

# Equalint Project Local Agent Context

## Purpose
This workspace holds the EquaLint accessibility evidence toolkit codebases (specifically the CLI and Core packages).

## Local Rules and Guidelines
1. **Separation of Scope**: Code execution and development are in `core/` and `cli/` directories respectively. Each is its own independent git repository.
2. **JIRA-Style Workbook**: Plan all tasks in a local JIRA-style workbook (`workbook.md`) at the root of the project.
3. **Task Checklist**: Maintain a `task.md` file in the artifact directory/workbook to track progress.
4. **Git Workflow**:
   - Create a GitHub issue for each task.
   - Create a new branch (e.g., `feature/issue-<num>-<description>`) for each task.
   - Implement, test, and document all changes.
   - Create a Pull Request (PR) and merge it to `main`.
5. **Autonomy & Verification**: Verify all publish configurations, builds, and package setup before execution.

## Stop And Ask
If there are npm registry authentication or scope permission issues, stop and report them to the user.
