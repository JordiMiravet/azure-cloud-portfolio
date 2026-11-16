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
  - [Certification Organization](#certification-organization)
  - [Laboratory Organization](#laboratory-organization)

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

## Certification Organization

The `certifications/` directory contains the learning materials and practical exercises associated with each Microsoft certification learning path.

Each certification has its own dedicated directory, identified by its exam code:

```text
certifications/
├── az-900/                  # Microsoft Azure Fundamentals
├── ai-901/                  # Microsoft Azure AI Fundamentals
├── ai-103/                  # Azure AI Apps and Agents Developer Associate
└── ai-200/                  # Azure AI Cloud Developer Associate
```

Each certification directory follows a consistent internal structure:

```text
az-900/
├── notes/
├── labs/
└── assets/
```

The directories serve the following purposes:

- **`notes/`:** Contains study notes, technical explanations, and certification-related learning materials.
- **`labs/`:** Contains practical exercises and hands-on laboratories related to the certification topics.
- **`assets/`:** Stores supporting resources such as images, diagrams, and screenshots.

This structure is shared across all certification learning paths to maintain consistency and make learning materials easy to navigate.

## Laboratory Organization

Hands-on laboratories are organized within the `labs/` directory of their corresponding certification learning path.

Each laboratory should have its own dedicated directory to keep its implementation files, documentation, and supporting resources together.

A typical laboratory directory may follow this structure:

```text
labs/
└── storage-account-lab/
    ├── README.md
    ├── src/
    └── assets/
```

The directories and files serve the following purposes:

- **`README.md`:** Describes the laboratory objectives, prerequisites, implementation steps, and expected results.
- **`src/`:** Contains scripts, configuration files, and other implementation resources used in the laboratory.
- **`assets/`:** Stores supporting resources such as screenshots, diagrams, and images.

The internal structure may vary depending on the complexity and requirements of each laboratory. Unnecessary directories should be avoided for simple exercises.


