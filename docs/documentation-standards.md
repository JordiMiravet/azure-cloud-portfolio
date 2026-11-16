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

## Markdown Formatting Standards

Markdown documentation must follow consistent formatting conventions to ensure readability and maintainability.

The following rules apply:

- Use ATX-style headings (`#`, `##`, `###`) to structure documents.
- Maintain a logical heading hierarchy without skipping levels.
- Use descriptive headings that clearly identify each section.
- Use unordered lists for related items and ordered lists for sequential instructions.
- Use Markdown checkboxes (`- [ ]`) for actionable checklists.
- Use fenced code blocks with the appropriate language identifier for code examples.
- Use inline code formatting for file paths, commands, configuration values, and technical identifiers.
- Use tables when presenting structured information or comparisons.
- Separate sections with blank lines to improve readability.

Formatting should remain consistent throughout each document.
