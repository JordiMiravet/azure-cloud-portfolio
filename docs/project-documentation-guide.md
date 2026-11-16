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
  - [Project README Template](#project-readme-template)
  - [Architecture Documentation](#architecture-documentation)
    - [Architecture Diagrams](#architecture-diagrams)
    - [Architecture Components](#architecture-components)

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

## Project README Template

Every independent project must include a `README.md` file describing its purpose, architecture, implementation, and results.

The README serves as the main entry point for understanding the project and should provide enough information for readers to understand its design and technical approach.

The following template establishes the recommended structure for documenting independent projects:

```markdown
# Project Title

## Overview

Describe the project, its purpose, the problem it addresses, and the main technologies involved.

## Objectives

List the main technical objectives and expected outcomes of the project.

## Architecture

Describe the overall architecture, including the main components, Azure services, and their relationships.

Include an architecture diagram when appropriate.

## Technologies

List the main technologies, frameworks, tools, and Azure services used in the implementation.

## Prerequisites

Describe the required tools, permissions, subscriptions, dependencies, and configurations.

## Implementation

Provide an overview of the implementation process and link to detailed technical documentation when necessary.

## Deployment

Explain how the solution is deployed and configured.

Include relevant commands, infrastructure templates, and deployment instructions.

## Testing and Validation

Describe how the implementation is tested and how its expected behavior is verified.

Include relevant results and supporting evidence.

## Cost Analysis

Document relevant Azure resource costs, estimates, and cost optimization considerations when applicable.

## Security Considerations

Describe relevant security configurations, access controls, and data protection considerations.

## Results

Summarize the final implementation, achieved objectives, and relevant technical outcomes.

## Future Improvements

Identify potential enhancements, limitations, or additional features that could be implemented.

## References

Include links to official documentation, technical resources, and other relevant references.
```

The template should be adapted according to the project's scope and complexity.

Sections that are not applicable may be omitted, while additional sections may be introduced when necessary.

The README should prioritize a clear overview rather than reproducing every implementation detail. More extensive technical explanations should be maintained in the project's `docs/` directory.

## Architecture Documentation

Architecture documentation must describe the design of an independent project, identifying its main components, Azure services, infrastructure resources, and their interactions.

The goal is to provide a clear understanding of how the solution is structured, how its components communicate, and how the architecture supports the project's objectives.

The following guidelines apply:

- Describe the overall architecture and its main components.
- Identify the Azure services, infrastructure resources, and external dependencies involved.
- Explain the responsibilities of each major component.
- Document how components communicate and exchange data.
- Describe relevant network configurations, connectivity, and security boundaries.
- Identify important data flows and integration points.
- Explain relevant architectural patterns and design considerations.
- Ensure that the documented architecture reflects the actual implementation.

Architecture documentation should provide enough technical context for readers to understand the solution without requiring them to inspect every implementation file.

### Architecture Diagrams

Architecture diagrams should be included whenever they help communicate the structure, components, or interactions of the solution.

The following guidelines apply:

- Use diagrams to represent the main infrastructure components and their relationships.
- Clearly identify Azure services, external systems, and relevant application components.
- Illustrate important communication paths and data flows.
- Use descriptive labels and consistent visual conventions.
- Keep diagrams readable and avoid unnecessary complexity.
- Store architecture diagrams in the project's `assets/diagrams/` directory.
- Reference diagrams from the project README or relevant technical documentation using relative paths.
- Prefer editable diagram formats and keep their source files whenever practical.
- Use exported formats such as PNG or SVG when embedding diagrams in Markdown.

Diagrams should complement written explanations rather than replace essential architectural information.

### Architecture Components

Relevant architecture components should be documented to explain their purpose and role within the solution.

Depending on the project, documentation may include:

- **Compute:** Virtual machines, containers, App Services, serverless functions, and other compute resources.
- **Networking:** Virtual networks, subnets, network security groups, gateways, and connectivity configurations.
- **Storage:** Storage accounts, databases, file systems, and data management services.
- **Identity and Security:** Microsoft Entra ID, managed identities, role-based access control, and security configurations.
- **Monitoring:** Azure Monitor, Log Analytics, Application Insights, and diagnostic configurations.
- **Integration:** APIs, messaging services, event-driven components, and external system integrations.

Only components relevant to the project need to be documented.

The level of detail should reflect the complexity of the architecture and the technical decisions involved.
