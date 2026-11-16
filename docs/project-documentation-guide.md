# Project Documentation Guide

This document defines the documentation guidelines and conventions for independent technical projects within the Azure Cloud Portfolio.

It establishes a consistent approach for documenting project objectives, cloud architectures, technical decisions, implementation procedures, deployment processes, and project outcomes.

The goal is to ensure that independent projects are clearly documented, technically understandable, reproducible, and easy to maintain.

For general documentation conventions, including Markdown formatting, file naming, and writing guidelines, see the [Documentation Standards](documentation-standards.md) guide.

For information about repository organization and independent project directories, see the [Repository Structure](repository-structure.md) guide.

## Table of Contents

- [Project Documentation Guide](#project-documentation-guide)
  - [Table of Contents](#table-of-contents)
  - [Project Directory Structure](#project-directory-structure)

## Project Directory Structure

Each independent project must have its own dedicated directory within the root `projects/` directory.

The directory should contain the documentation, source code, infrastructure definitions, and supporting resources required to understand and reproduce the project.

A typical project directory follows this structure:

```text
project-name/
├── README.md
├── docs/
│   ├── architecture.md
│   └── technical-decisions.md
├── src/
│   ├── infrastructure/
│   ├── scripts/
│   └── application/
└── assets/
    ├── diagrams/
    └── screenshots/
```

The directories and files serve the following purposes:

- **`README.md`:** Provides an overview of the project, including its objectives, architecture, technologies, implementation, and results.
- **`docs/`:** Contains detailed technical documentation, architecture descriptions, design decisions, and additional implementation information.
- **`src/`:** Stores application source code, infrastructure definitions, scripts, and configuration files.
  - **`infrastructure/`:** Contains infrastructure-as-code templates and deployment definitions.
  - **`scripts/`:** Stores automation scripts and supporting commands.
  - **`application/`:** Contains application source code when applicable.
- **`assets/`:** Contains project-specific supporting resources.
  - **`diagrams/`:** Stores architecture diagrams and their editable source files.
  - **`screenshots/`:** Contains screenshots and visual evidence of the implementation.

The internal directories are optional and should only be created when required by the project.

Additional files and directories may be introduced depending on the project's architecture, technologies, and implementation requirements.

Projects should maintain a simple and logical structure, avoiding unnecessary directories and duplicated documentation.
