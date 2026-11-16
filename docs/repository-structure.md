# Repository Structure

This document describes the directory structure and organizational conventions of the Azure Cloud Portfolio.

It explains the purpose of each main directory and establishes guidelines for organizing certification learning materials, hands-on laboratories, independent projects, and shared resources.

The goal is to maintain a consistent, scalable, and easy-to-navigate repository structure as the portfolio grows.

For general documentation conventions, including file naming, Markdown formatting, and writing guidelines, see the [Documentation Standards](documentation-standards.md) guide.

## Table of Contents

- [Repository Structure](#repository-structure)
  - [Table of Contents](#table-of-contents)
  - [Root Directory Structure](#root-directory-structure)
  - [Main Directories](#main-directories)

## Root Directory Structure

The repository is organized into dedicated directories for certification learning paths, general documentation, shared resources, and independent cloud projects.

The root directory also contains repository-level configuration files, contribution guidelines, and licensing information.

The following tree provides an overview of the main repository structure:

```text
azure-cloud-portfolio/
├── .github/
├── assets/
├── certifications/
│   ├── az-900/
│   ├── ai-901/
│   ├── ai-103/
│   └── ai-200/
├── docs/
├── projects/
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

The structure separates certification materials, independent projects, and general repository resources to keep related content organized and easy to navigate.

## Main Directories

The repository contains the following main directories:

- **`.github/`:** Contains GitHub configuration files, including issue templates and pull request templates.
- **`assets/`:** Stores images, diagrams, and other resources shared across the repository.
- **`certifications/`:** Contains certification learning paths, including study notes, hands-on laboratories, and related resources organized by certification.
- **`docs/`:** Contains general repository documentation, including development guidelines, documentation standards, and repository organization guides.
- **`projects/`:** Contains independent cloud projects demonstrating practical implementations, architectures, and technical solutions.

Each directory has a specific responsibility to maintain a clear separation between certification learning materials, independent projects, and general repository resources.

