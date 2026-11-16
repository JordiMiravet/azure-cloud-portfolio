# Documentation Standards

This document defines the documentation standards and conventions for the Azure Cloud Portfolio.

It establishes guidelines for structuring, writing, formatting, and maintaining documentation across the repository to ensure consistency, readability, and maintainability.

These standards apply to certification materials, hands-on laboratories, independent cloud projects, and general repository documentation.

For development conventions, including branch naming, commit messages, and pull request requirements, see the [Development Workflow](development-workflow.md) guide.

## Documentation Structure

Documentation must be organized according to its context and purpose to keep the repository structured and easy to navigate.

The following conventions apply:

- **Certifications:** Study notes, learning materials, and laboratory documentation must be organized within their corresponding certification directory.
- **Laboratories:** Each laboratory should have its own directory when it includes multiple files or supporting resources.
- **Projects:** Independent projects must maintain their documentation within their respective project directories.
- **General Documentation:** Repository-wide guidelines, development conventions, and documentation standards belong in the root `docs/` directory.

Documentation should be placed as close as possible to the content it describes, avoiding unnecessary duplication and keeping related resources together.

## File Naming Conventions

Documentation files must follow consistent naming conventions to improve readability and navigation throughout the repository.

The following rules apply:

- Use lowercase letters.
- Separate words using hyphens (`kebab-case`).
- Use descriptive names that clearly identify the document's content.
- Use the `.md` extension for Markdown documentation.
- Avoid spaces, special characters, and unnecessary abbreviations.

Examples:

```text
development-workflow.md
documentation-standards.md
azure-fundamentals.md
storage-account-lab.md
```
