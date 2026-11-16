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

## Writing Guidelines

Documentation must be written in a clear, consistent, and professional manner.

The following guidelines apply:

- Write all documentation in English.
- Use clear and concise language.
- Prefer technical accuracy over unnecessary complexity.
- Explain technical concepts and procedures in a way that is easy to understand.
- Use consistent terminology throughout the repository.
- Avoid ambiguous descriptions and unnecessary repetition.
- Write instructions in a logical sequence.
- Use active voice whenever possible.
- Ensure that examples and commands are relevant to the documented content.

Documentation should prioritize clarity, accuracy, and practical usefulness.

## Links and References

Documentation should include relevant links and references to help readers navigate related content and access authoritative information.

The following guidelines apply:

- Use relative links when referencing files and directories within the repository.
- Use descriptive link text that clearly identifies the destination.
- Prefer official documentation and trusted sources when referencing external technical information.
- Ensure that external references point to relevant and reliable resources.
- Verify that links are valid and accessible before publishing documentation.
- Avoid unnecessary duplication of information by linking to existing documentation when appropriate.

References should provide additional context and support the information presented in each document.

## Documentation Maintenance

Documentation must be kept accurate, consistent, and up to date as the repository evolves.

The following guidelines apply:

- Update documentation whenever relevant changes affect its content.
- Remove outdated or redundant information.
- Ensure that documented procedures and examples reflect the current implementation.
- Review internal and external links periodically.
- Keep documentation consistent with the actual repository structure.
- Include relevant documentation updates in the pull requests associated with the corresponding changes.

Documentation should evolve alongside the project to remain a reliable source of information.
