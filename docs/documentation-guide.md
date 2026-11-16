# Documentation Guide

This document defines how the Azure Cloud Portfolio is organized and documented: folder structure, naming, Markdown conventions, and templates for labs and projects.

For branch names, commit messages, and pull requests, see the [Development Workflow](development-workflow.md) guide.

## Table of Contents

- [Documentation Guide](#documentation-guide)
  - [Table of Contents](#table-of-contents)
  - [Folder Structure](#folder-structure)

## Folder Structure

Content is placed as close as possible to what it describes.

```text
azure-cloud-portfolio/
├── .github/                 # Issue and pull request templates
├── assets/                  # Images shared across the repository
├── certifications/
│   └── az-900/
│       └── labs/            # One folder per lab
├── docs/                    # Repository guides
└── projects/                # Independent projects
```

Folders are created only when there is content for them. Other certifications follow the same pattern as `az-900/`, and an optional `notes/` folder can be added next to `labs/` when study notes are needed.

A lab folder looks like this:

```text
labs/
├── README.md                # Index of labs and their status
└── storage-account/
    ├── README.md
    └── assets/
        └── screenshots/
```

Add a `src/` folder to a lab or project only when it includes scripts or templates.
