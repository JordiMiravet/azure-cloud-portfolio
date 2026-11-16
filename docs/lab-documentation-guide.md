# Laboratory Documentation Guide

This document defines the documentation guidelines and conventions for hands-on laboratories within the Azure Cloud Portfolio.

It establishes a consistent approach for documenting laboratory objectives, prerequisites, implementation procedures, technical results, and supporting evidence.

The goal is to ensure that practical exercises are clearly documented, reproducible, and easy to understand while providing a reliable reference for future learning and technical implementations.

For general documentation conventions, including Markdown formatting, file naming, and writing guidelines, see the [Documentation Standards](documentation-standards.md) guide.

For information about laboratory directory organization, see the [Repository Structure](repository-structure.md) guide.

## Table of Contents

- [Laboratory Documentation Guide](#laboratory-documentation-guide)
  - [Table of Contents](#table-of-contents)
  - [Laboratory Directory Structure](#laboratory-directory-structure)
  - [Laboratory README Template](#laboratory-readme-template)
  - [Expected Documentation Sections](#expected-documentation-sections)
  - [Screenshots and Evidence](#screenshots-and-evidence)
    - [Screenshot Naming Conventions](#screenshot-naming-conventions)
  - [Architecture Diagrams and Scripts](#architecture-diagrams-and-scripts)
    - [Architecture Diagrams](#architecture-diagrams)
    - [Scripts and Configuration Files](#scripts-and-configuration-files)
  - [Troubleshooting and Lessons Learned](#troubleshooting-and-lessons-learned)
    - [Troubleshooting](#troubleshooting)
    - [Lessons Learned](#lessons-learned)
  - [Microsoft Learning References](#microsoft-learning-references)

## Laboratory Directory Structure

Each hands-on laboratory must have its own dedicated directory within the `labs/` directory of its corresponding certification learning path.

The directory should contain all documentation, implementation files, and supporting resources required to understand and reproduce the laboratory.

A typical laboratory directory follows this structure:

```text
storage-account-lab/
├── README.md
├── src/
│   ├── scripts/
│   └── templates/
└── assets/
    ├── screenshots/
    └── diagrams/
```

The directories and files serve the following purposes:

- **`README.md`:** Contains the laboratory documentation, including objectives, prerequisites, implementation steps, expected results, and references.
- **`src/`:** Stores scripts, configuration files, templates, and other implementation resources used in the laboratory.
  - **`scripts/`:** Contains automation scripts and commands used during the implementation.
  - **`templates/`:** Stores infrastructure templates and configuration files.
- **`assets/`:** Contains supporting resources such as screenshots, architecture diagrams, and other visual evidence.
  - **`screenshots/`:** Stores screenshots documenting implementation steps and validation results.
  - **`diagrams/`:** Contains architecture diagrams and their source files.

The internal subdirectories are optional and should only be created when required by the laboratory.

Additional files or directories may be introduced depending on the laboratory's complexity and implementation requirements.

The structure should remain as simple as possible, avoiding unnecessary files and directories for straightforward exercises.

## Laboratory README Template

Each laboratory must include a `README.md` file describing its objectives, requirements, implementation procedures, and results.

The following template establishes the recommended structure for documenting hands-on laboratories:

```markdown
# Laboratory Title

## Overview

Briefly describe the laboratory, its purpose, and the Azure services or technologies involved.

## Objectives

List the main learning objectives and technical skills addressed by the laboratory.

## Prerequisites

Describe the required knowledge, tools, permissions, Azure resources, and configurations needed before starting the laboratory.

## Architecture

Describe the architecture and Azure resources involved in the implementation.

Include an architecture diagram when it helps explain the solution.

## Implementation

Document the implementation procedure in a logical sequence.

Include relevant commands, configurations, code examples, and screenshots where necessary.

## Validation and Results

Explain how to verify that the implementation works as expected.

Include relevant outputs, screenshots, and observations.

## Cleanup

Describe how to remove the resources created during the laboratory.

Include relevant commands, portal instructions, or configuration changes required to safely remove the deployed resources and avoid unnecessary Azure costs.

## Troubleshooting

Document relevant issues encountered during implementation and their solutions.

## Lessons Learned

Summarize the main technical concepts, challenges, and practical knowledge gained from the laboratory.

## References

Include links to official Microsoft Learn materials and other relevant technical documentation.
```

The template may be adapted depending on the laboratory's complexity, objectives, and implementation requirements. Sections that are not relevant may be omitted, while additional sections may be introduced when necessary.

## Expected Documentation Sections

Laboratory documentation should provide enough information for readers to understand the purpose of the exercise, follow its implementation, and verify the expected results.

The following sections should be included when relevant:

- **Overview:** Introduces the laboratory, its purpose, and the Azure services or technologies involved.
- **Objectives:** Defines the technical concepts and practical skills the laboratory aims to develop.
- **Prerequisites:** Identifies the required knowledge, tools, permissions, subscriptions, and resources.
- **Architecture:** Describes the solution design, Azure components, and their relationships.
- **Implementation:** Documents the configuration and deployment procedures in a logical sequence.
- **Validation and Results:** Explains how to verify the implementation and presents the expected outcomes.
- **Cleanup:** Explains how to remove resources created during the laboratory and avoid unnecessary Azure costs.
- **Troubleshooting:** Records relevant issues, their causes, and their resolutions.
- **Lessons Learned:** Summarizes the main concepts, challenges, and technical knowledge gained.
- **References:** Provides links to official Microsoft Learn materials and other relevant technical resources.

Documentation should prioritize practical clarity and reproducibility. Instructions must be detailed enough for readers to understand and repeat the implementation without unnecessary ambiguity.

The level of detail may vary depending on the laboratory's complexity. Simple exercises do not require unnecessary sections or excessive explanations.

## Screenshots and Evidence

Screenshots and other supporting evidence should be included when they help demonstrate implementation steps, resource configurations, or successful validation results.

The following guidelines apply:

- Capture screenshots at relevant stages of the laboratory implementation.
- Ensure screenshots clearly show the configuration, operation, or result being documented.
- Include a short explanation describing what each screenshot demonstrates.
- Remove credentials, access keys, tokens, personal information, and other sensitive data before publishing evidence.
- Use descriptive filenames that identify the corresponding implementation step or resource.
- Store screenshots and supporting evidence in the laboratory's `assets/` directory.
- Reference screenshots from the laboratory `README.md` using relative paths.
- Avoid redundant screenshots that do not provide additional technical value.

Evidence should support the documented implementation and provide readers with a clear understanding of the expected results.

Screenshots should complement written instructions rather than replace essential implementation details.

### Screenshot Naming Conventions

Screenshots should follow consistent naming conventions to improve identification and navigation.

The following guidelines apply:

- Use lowercase letters and hyphens (`kebab-case`) in filenames.
- Use descriptive names that identify the resource, operation, or implementation step.
- Use sequential numbering when screenshots follow a specific implementation sequence.
- Use the `.png` format for screenshots containing interfaces, terminal output, or configuration details.
- Avoid spaces, special characters, and generic filenames.

Example:

```text
assets/
└── screenshots/
    ├── 01-resource-group-created.png
    ├── 02-storage-account-created.png
    └── 03-container-created.png
```

Screenshots should be named consistently throughout each laboratory to make their purpose immediately recognizable.

## Architecture Diagrams and Scripts

Architecture diagrams and implementation scripts should be documented clearly to help readers understand the laboratory design and reproduce its implementation.

### Architecture Diagrams

The following guidelines apply:

- Include architecture diagrams when they help explain Azure resources, infrastructure components, or service interactions.
- Clearly identify the main components and their relationships.
- Use consistent visual conventions and descriptive labels.
- Keep diagrams readable and avoid unnecessary complexity.
- Store diagrams in the laboratory's `assets/` directory.
- Reference diagrams from the laboratory `README.md` using relative paths.
- Prefer editable diagram formats whenever possible.
- Use exported image formats such as PNG or SVG when embedding diagrams in Markdown.
- Keep the original diagram source alongside the exported image whenever practical.

### Scripts and Configuration Files

The following guidelines apply:

- Store implementation scripts, configuration files, and infrastructure templates in the `src/` directory.
- Use descriptive filenames that reflect their purpose.
- Document the purpose and expected behavior of each relevant script.
- Include execution instructions and required parameters when applicable.
- Identify required dependencies, permissions, and configuration values.
- Never include hardcoded credentials, secrets, or sensitive information.
- Use placeholders or environment variables for sensitive configuration values.

Scripts and configuration files should be organized to support reproducibility, readability, and maintainability.

## Troubleshooting and Lessons Learned

Laboratory documentation should capture relevant implementation issues, their resolutions, and the technical knowledge gained throughout the exercise.

### Troubleshooting

The following guidelines apply:

- Document relevant errors and unexpected behaviors encountered during implementation.
- Describe the conditions under which each issue occurred.
- Explain the identified cause whenever possible.
- Provide the steps taken to resolve the issue.
- Include relevant error messages or screenshots when they provide useful context.
- Document alternative solutions or workarounds when appropriate.

Troubleshooting information should help readers understand common issues and avoid repeating the same mistakes.

When documenting troubleshooting scenarios, the following structure can be used:

```markdown
### Issue: Brief description of the problem

**Error:**

Describe the error message or unexpected behavior encountered.

**Cause:**

Explain the identified cause of the issue.

**Resolution:**

Document the steps taken to resolve the issue.

**Additional Notes:**

Include relevant observations, alternative solutions, or preventive recommendations.
```

This structure is recommended for documenting relevant issues consistently. It may be adapted depending on the complexity and nature of the problem.

### Lessons Learned

The following guidelines apply:

- Summarize the main technical concepts explored during the laboratory.
- Highlight important Azure services, configurations, and implementation decisions.
- Describe relevant challenges and how they were addressed.
- Identify areas for improvement or further exploration.
- Explain how the knowledge gained can be applied to other cloud scenarios.

Lessons learned should focus on practical knowledge and meaningful technical insights rather than simply repeating the implementation steps.

## Microsoft Learning References

Laboratory documentation should include relevant learning materials and official technical references to provide additional context and support further learning.

The following guidelines apply:

- **Microsoft Learn:** Include relevant learning modules, learning paths, and guided exercises related to the laboratory objectives.
- **Azure Documentation:** Reference official technical documentation when explaining Azure services, configurations, features, or implementation procedures.
- **Additional Resources:** Include relevant community tutorials, repositories, or external technical materials when they provide useful complementary information.
- Use direct links to specific learning resources or documentation pages whenever possible.
- Ensure references are relevant to the laboratory implementation and learning objectives.
- Use descriptive link text that clearly identifies each resource.
- Verify that external links are valid and accessible before publishing documentation.
- Clearly distinguish official Microsoft resources from community tutorials and other external references.

When a laboratory is based on an official Microsoft Learn exercise, include a direct reference to the original learning material whenever possible.

References should help readers understand the concepts behind each laboratory and provide reliable resources for further exploration.

---

[↑ Back to top](#lab-documentation-guide)
