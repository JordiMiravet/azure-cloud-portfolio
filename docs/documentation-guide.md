# Documentation Guide

This document defines how the Azure Cloud Portfolio is organized and documented: folder structure, naming, Markdown conventions, and templates for labs and projects.

For branch names, commit messages, and pull requests, see the [Development Workflow](development-workflow.md) guide.

## Table of Contents

- [Documentation Guide](#documentation-guide)
  - [Table of Contents](#table-of-contents)
  - [Folder Structure](#folder-structure)
  - [Naming and Formatting](#naming-and-formatting)
  - [Lab Documentation](#lab-documentation)
    - [Lab README Template](#lab-readme-template)
    - [Screenshots](#screenshots)

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

## Naming and Formatting

- Use lowercase `kebab-case` for files and folders, for example `storage-account/` or `documentation-guide.md`.
- Write all documentation in English.
- Use ATX headings (`#`, `##`, `###`) without skipping levels.
- Use fenced code blocks with a language identifier.
- Use inline code for file paths, commands, and Azure resource names.
- Use relative links for files inside the repository, and official Microsoft documentation for external references.
- Add a table of contents only to documents with several sections.

## Lab Documentation

Each lab has its own folder with a `README.md`. Labs based on an official exercise must link to the original, such as the [AZ-900 labs](https://microsoftlearning.github.io/AZ-900-Microsoft-Azure-Fundamentals/).

### Lab README Template

```markdown
# Lab Title

## Overview

What the lab covers and which Azure services are involved. Link the original exercise if there is one.

## Steps

Main steps in order, with the key commands or portal actions and screenshots where they help.

The last step should delete the resources created, to avoid unnecessary costs.

## Result

How it was verified that everything worked.

## Lessons Learned

What was learned, what was difficult, and any issue found with its solution.

## References

Links to Microsoft Learn and official documentation.
```

Sections that do not apply can be omitted.

### Screenshots

- Store them in the lab's `assets/screenshots/` folder and link them with relative paths.
- Use `.png` files named in `kebab-case` with a sequence number, for example `01-resource-group-created.png`.
- Add a short sentence explaining what each screenshot shows.
- Remove or blur subscription IDs, keys, tokens, and personal data before committing.
