# Laboratory Documentation Guide

This document defines the documentation guidelines and conventions for hands-on laboratories within the Azure Cloud Portfolio.

It establishes a consistent approach for documenting laboratory objectives, prerequisites, implementation procedures, technical results, and supporting evidence.

The goal is to ensure that practical exercises are clearly documented, reproducible, and easy to understand while providing a reliable reference for future learning and technical implementations.

For general documentation conventions, including Markdown formatting, file naming, and writing guidelines, see the [Documentation Standards](documentation-standards.md) guide.

For information about laboratory directory organization, see the [Repository Structure](repository-structure.md) guide.

## Laboratory Directory Structure

Each hands-on laboratory must have its own dedicated directory within the `labs/` directory of its corresponding certification learning path.

The directory should contain all documentation, implementation files, and supporting resources required to understand and reproduce the laboratory.

A typical laboratory directory follows this structure:

```text
storage-account-lab/
├── README.md
├── src/
└── assets/
```

The directories and files serve the following purposes:

- **`README.md`:** Contains the laboratory documentation, including objectives, prerequisites, implementation steps, expected results, and references.
- **`src/`:** Stores scripts, configuration files, templates, and other implementation resources used in the laboratory.
- **`assets/`:** Contains supporting resources such as screenshots, architecture diagrams, and other visual evidence.

Additional files or directories may be introduced when required by the laboratory's complexity or implementation technologies.

The structure should remain as simple as possible, avoiding unnecessary files and directories for straightforward exercises.
