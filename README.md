# Azure Cloud Portfolio

Hands-on labs and projects documenting my learning journey through Microsoft Azure and AI, as part of my certification path.

This portfolio was started during the **IT Academy Azure and AI Certification program** (5 November – 3 December 2026), a free 80-hour training program covering four official Microsoft learning paths. It showcases my practical work throughout the program, including step-by-step labs, implementation screenshots, technical documentation, and lessons learned.

## Table of Contents

- [Azure Cloud Portfolio](#azure-cloud-portfolio)
  - [Table of Contents](#table-of-contents)
  - [Certification Progress](#certification-progress)
  - [Completed Labs](#completed-labs)
  - [Repository Structure](#repository-structure)
  - [Development Workflow](#development-workflow)
  - [Documentation Guide](#documentation-guide)
  - [Documentation](#documentation)

## Certification Progress

| Certification | Status | Links |
| --- | --- | --- |
| **AZ-900** - Microsoft Azure Fundamentals | In progress | [Labs](certifications/az-900/README.md) · [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/exams/az-900/) |
| **AI-901** - Microsoft Azure AI Fundamentals | Pending | [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-901/) |
| **AI-103** - Azure AI Apps and Agents Developer Associate | Pending | [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-103/) |
| **AI-200** - Azure AI Cloud Developer Associate | Pending | [Microsoft Learn](https://learn.microsoft.com/en-us/credentials/certifications/exams/ai-200/) |

## Completed Labs

- [Create an Azure resource](certifications/az-900/create-azure-resource/README.md) - AZ-900
- [Create a virtual machine and configure it as a web host](certifications/az-900/create-virtual-machine/README.md) - AZ-900
- [Create a storage blob](certifications/az-900/create-storage-blob/README.md) - AZ-900
- [Estimate workload costs with the Pricing calculator](certifications/az-900/estimate-workload-costs/README.md) - AZ-900

Every completed lab is documented with step-by-step instructions, implementation screenshots, results, and lessons learned.

See the [AZ-900 labs index](certifications/az-900/README.md) for the full list of labs.

## Repository Structure

```text
azure-cloud-portfolio/
├── .github/                         # Issue and pull request templates
├── assets/                          # Shared images and resources
├── certifications/
│   └── az-900/                      # AZ-900 hands-on labs
│       ├── README.md                # Labs index
│       ├── lab-template/            # Template for documenting new labs
│       └── <lab-name>/              # One folder per lab
├── docs/
│   ├── development-workflow.md      # Issues, branches, commits, and pull requests
│   └── documentation-guide.md       # Folder structure, formatting, and templates
├── CONTRIBUTING.md
├── LICENSE
└── README.md
```

New certifications and projects get their own folders as the work progresses. For more details on how content is organized, see the [Folder Structure](docs/documentation-guide.md#folder-structure) section of the Documentation Guide.

## Development Workflow

Work is tracked with GitHub Issues and delivered through pull requests, following consistent conventions:

| Element | Convention | Example |
| --- | --- | --- |
| Issue | `[CATEGORY] - Short description` | `[DOCS] - Rewrite README to showcase certification progress and labs` |
| Branch | `<type>/<task-number>-<short-description>` | `feature/25-create-certification-structure` |
| Commit | `<type>(<scope>): <description> (#<task-number>)` | `feat(labs): add reusable lab README template (#25)` |
| Pull request | Commit format as title, referencing its task | `docs(readme): rewrite README (#26)` |

For the full process, see the [Development Workflow](docs/development-workflow.md) guide.

## Documentation Guide

Each lab and project is documented in its own folder, following a common structure:

- Every lab has a `README.md` with five sections: Overview, Steps, Result, Lessons Learned, and References.
- Files and folders use lowercase `kebab-case`, and all documentation is written in English.
- Screenshots are stored in the lab's `assets/screenshots/` folder, numbered by step, with sensitive data removed.

For the folder structure, formatting conventions, and templates, see the [Documentation Guide](docs/documentation-guide.md).

## Documentation

The following table lists all the guides and policies available in the repository:

| Document | Description |
| --- | --- |
| [Development Workflow](docs/development-workflow.md) | Issues, branch naming, commit messages, and pull requests. |
| [Documentation Guide](docs/documentation-guide.md) | Folder structure, naming and formatting conventions, and lab and project templates. |
| [Contributing Guidelines](CONTRIBUTING.md) | How to report issues and propose changes. |
| [License](LICENSE) | Terms of use for the original materials. |

---

[↑ Back to top](#azure-cloud-portfolio)
