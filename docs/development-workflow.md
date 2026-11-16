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
      - [Epic Structure](#epic-structure)
      - [Epic Example](#epic-example)
  - [Task Structure and Conventions](#task-structure-and-conventions)
      - [Task Title](#task-title)
      - [Task Structure](#task-structure)
      - [Task Example](#task-example)

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

#### Epic Structure

Every epic must contain the following sections, in this order:

1. Description
2. Scope
3. Acceptance Criteria

**Description**

Explain the problem, need, or objective behind the epic, providing enough context to understand why the work is necessary and what it aims to achieve.

- Introduce the overall goal of the initiative.
- Explain the current situation or problem when relevant.
- Describe the expected outcome or improvement.
- Focus on the overall objective rather than individual implementation steps.

**Scope**

Define the work covered by the epic using a bullet list.

- Describe the main changes, improvements, or deliverables included.
- Keep each item focused on a specific area of work.
- Establish clear boundaries to prevent unrelated changes from being included.
- Ensure the scope is consistent with the objective described in the description.

**Acceptance Criteria**

List the conditions that must be satisfied for the epic to be considered complete.

- Use a checklist with Markdown checkboxes (`- [ ]`).
- Describe specific, verifiable outcomes rather than implementation steps.
- Ensure each criterion corresponds to the epic's objective and scope.
- Include relevant constraints, such as preserving existing functionality or limiting changes to documentation, when applicable.

#### Epic Example

**Title:** `[DOCS] - Document development workflow`

The following example illustrates how an epic should be structured:

```markdown
## Description

Document the development workflow of Azure Cloud Portfolio and establish consistent conventions for organizing development work.

The goal is to ensure that all repository contributions follow a clear and consistent process, making development activities easier to understand, manage, and track.

## Scope

- Document the relationship between epics, tasks, and pull requests.
- Define branch naming conventions.
- Define commit message conventions.
- Document the expected structure of epics, tasks, and pull requests.
- Explain the typical development workflow.
- Document how GitHub Projects is used to organize and track work.

## Acceptance Criteria

- [ ] The development workflow is documented.
- [ ] The relationship between epics, tasks, and pull requests is clearly explained.
- [ ] Branch naming conventions are defined.
- [ ] Commit message conventions are defined.
- [ ] Epic and task structures are documented.
- [ ] Pull request conventions are documented.
- [ ] The typical development workflow is explained.
- [ ] GitHub Projects usage is documented.
- [ ] The documentation is consistent, readable, and written in English.
```

## Task Structure and Conventions

Tasks break epics down into specific, manageable units of work. Each task defines a clear objective, an implementation scope, and verifiable acceptance criteria.

All tasks must follow the structure defined in the [Task Template](../.github/ISSUE_TEMPLATE/task.md).

#### Task Title

Tasks must follow this title format:

`[CATEGORY] - Short description of the task`

The category identifies the type of work, while the description summarizes the specific objective of the task.

Example: `[DOCS] - Document issue and pull request workflow`

#### Task Structure

Every task must contain the following sections, in this order:

1. PR Reference
2. Description
3. Scope
4. Acceptance Criteria

**PR Reference**

Reference the pull request associated with the task using the following format:

`### [PR #]()`

Leave the reference empty until a pull request is created. Once available, replace the placeholder with the corresponding PR number and URL.

This reference connects the task to its implementation.

**Description**

Explain the specific objective of the task, providing enough context to understand what needs to be achieved and why.

- Focus on the particular piece of work covered by the task.
- Explain the expected outcome.
- Avoid repeating the overall objective of the parent epic.

**Scope**

Define the changes required to complete the task using a bullet list.

- Describe the specific changes or deliverables included.
- Keep each item focused on a clear part of the implementation.
- Establish boundaries to avoid unrelated changes or work belonging to other tasks.
- Ensure the scope contributes to the parent epic's objective.

**Acceptance Criteria**

List the conditions that must be satisfied for the task to be considered complete.

- Use a checklist with Markdown checkboxes (`- [ ]`).
- Describe specific, verifiable outcomes.
- Ensure each criterion corresponds to an item in the task's scope or its expected result.
- Include relevant constraints, such as preserving existing behavior or limiting changes to documentation, when applicable.

#### Task Example

**Title:** `[DOCS] - Document development workflow`

The following example illustrates how a task should be structured:

```markdown
### [PR #]()

## Description

Document the development workflow of Azure Cloud Portfolio, including how development work is organized and how contributions are managed throughout the implementation process.

The goal is to establish clear conventions for branches, commits, epics, tasks, and pull requests, ensuring that contributions follow a consistent and traceable workflow.

## Scope

- Create `docs/development-workflow.md`.
- Document the relationship between epics, tasks, and pull requests.
- Define branch naming conventions.
- Define commit message conventions.
- Document epic and task structures and conventions.
- Document pull request structure and conventions.
- Explain the typical development workflow.
- Document how GitHub Projects is used to organize work.

## Acceptance Criteria

- [ ] The development workflow document exists.
- [ ] The relationship between epics, tasks, and pull requests is documented.
- [ ] Branch naming conventions are defined.
- [ ] Commit message conventions are defined.
- [ ] Epic and task structures are documented.
- [ ] Pull request conventions are documented.
- [ ] The typical development workflow is explained.
- [ ] GitHub Projects usage is documented.
```
