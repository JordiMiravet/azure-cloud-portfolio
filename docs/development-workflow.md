# Development Workflow

This document describes the development workflow of Azure Cloud Portfolio, including how work is organized, how branches and commits are named, and how epics, tasks, and pull requests are structured.

It serves as the detailed reference for the project's development conventions and contribution workflow.

For a brief overview, see the [Development Workflow](../README.md#development-workflow) section in the README.

For contribution guidelines, including how to report issues and propose changes, see [CONTRIBUTING.md](../CONTRIBUTING.md).

## Table of Contents

- [Development Workflow](#development-workflow)
  - [Table of Contents](#table-of-contents)
  - [Issue and Pull Request Structure](#issue-and-pull-request-structure)
    - [How They Relate](#how-they-relate)
    - [Quick Reference](#quick-reference)
    - [Development Flow](#development-flow)
  - [Branch Naming](#branch-naming)
  - [Commit Messages](#commit-messages)
  - [Epic Structure and Conventions](#epic-structure-and-conventions)
      - [Epic Title](#epic-title)

## Issue and Pull Request Structure

Development work is organized into epics, tasks, and pull requests to ensure that every contribution can be traced from its initial objective to its implementation.

- **Epics:** Represent larger objectives, features, or improvements. They define the motivation, overall scope, and expected outcomes of an initiative.
- **Tasks:** Break epics down into smaller, actionable units of work. Each task defines a specific objective, implementation scope, and verifiable acceptance criteria.
- **Pull Requests (PRs):** Submit and document the changes implemented to complete tasks, providing the context needed to review and validate them before merging into `main`.

The relationship between these elements follows this structure:

```text
Epic
 └── Task                 (linked to its parent epic)
      └── Pull Request    (references the task it implements)
```

### How They Relate

- Each task must be linked to its parent epic through GitHub. Tasks should be sufficiently focused to be implemented and reviewed independently. Together, they should cover the epic's scope and acceptance criteria.
- An epic is considered complete when all its required tasks have been completed and its acceptance criteria have been satisfied.
- Each pull request must reference the task it implements. A task may require multiple pull requests when its implementation involves separate changes, but each PR should remain focused on a clear set of changes.
- Epics and tasks are managed as GitHub Issues. Their issue numbers provide traceability throughout the development workflow and are used to identify the corresponding tasks in branch names, commit messages, and pull request titles.

### Quick Reference

| Element | Title Format | Sections (in order) | Template |
| --- | --- | --- | --- |
| Epic | `[CATEGORY] - Short description` | Description, Scope, Acceptance Criteria | [epic.md](../.github/ISSUE_TEMPLATE/epic.md) |
| Task | `[CATEGORY] - Short description` | PR Reference, Description, Scope, Acceptance Criteria | [task.md](../.github/ISSUE_TEMPLATE/task.md) |
| Pull Request | `<type>(<scope>): <short description> (#<task-number>)` | Task Reference, Summary, Components, What's included, Notes | [PULL_REQUEST_TEMPLATE.md](../.github/PULL_REQUEST_TEMPLATE.md) |

GitHub automatically loads the corresponding templates when creating issues or opening pull requests. These templates establish a consistent structure for documenting work across the repository.

The following sections explain the conventions and expected content for each element. Note that the pull request title must be written manually, as it is not populated by the template.

### Development Flow

The typical development process follows these steps:

1. Create an epic to define the overall objective, scope, and expected outcomes of an initiative.
2. Create individual tasks for the work required to complete the epic, linking each task to its parent epic.
3. Create a dedicated branch for each task, following the [Branch Naming](#branch-naming) convention.
4. Implement the task through small, focused commits that follow the [Commit Messages](#commit-messages) convention.
5. Open a pull request referencing the corresponding task and following the [Pull Request Structure and Conventions](#pull-request-structure-and-conventions).
6. Review the pull request, address feedback, and merge it into `main` once approved.

## Branch Naming

Create a new branch from `main` using the following naming convention:

```text
<type>/<task-number>-<short-description>
```

Where:

- `<type>` identifies the type of change.
- `<task-number>` corresponds to the GitHub Issue number of the task.
- `<short-description>` briefly describes the purpose of the branch.

Examples:

```text
feature/234-document-development-workflow
fix/198-handle-null-response
docs/234-update-readme
```

## Commit Messages

Commit messages must follow this format:

```text
<type>(<scope>): <short description in English> (#<task-number>)
```

Examples:

```text
feat(terraform): add storage account module (#145)
fix(networking): correct subnet configuration (#182)
docs(workflow): document development workflow (#7)
```

Common types:

- `feat`: a new feature.
- `fix`: a bug fix.
- `docs`: documentation changes.
- `test`: adding or updating tests.
- `refactor`: code changes that neither fix a bug nor add a feature.
- `chore`: maintenance tasks such as dependency updates.

Branch names use the same types, with `feature` written in full instead of `feat`.

To keep commit messages consistent:

- Keep commit messages concise.
- Write them in English.
- Focus each commit on a single logical change.

## Epic Structure and Conventions

Epics group larger features, improvements, or technical objectives into a single initiative. They define the overall goal and scope of the work, which is broken down into multiple related tasks.

All epics must follow the structure defined in the [Epic Template](../.github/ISSUE_TEMPLATE/epic.md).

#### Epic Title

Epics must follow this title format:

`[CATEGORY] - Short description of the objective`

The category identifies the type of work, while the description summarizes the overall objective of the epic.

Example: `[DOCS] - Document project workflow and issue templates`