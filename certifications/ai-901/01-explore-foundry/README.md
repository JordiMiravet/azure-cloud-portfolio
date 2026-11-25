# Get Started with Microsoft Foundry

## Overview

This lab creates a Microsoft Foundry project, explores the Foundry portal, deploys a model, and connects a client application to the project to try text analysis, speech, computer vision, information extraction, and safety guardrails. It uses the services Microsoft Foundry, Azure Speech in Foundry tools, and Resource groups.

Based on the official exercise: [Get started with Microsoft Foundry](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Exercises/00-explore-foundry.html).

Region used: TODO region.

Model used: TODO model and deployment name.

## Steps

### 1. Create a Foundry project

1. Open [Microsoft Foundry](https://ai.azure.com) and sign in with the Azure account.
2. Create a new project with a unique name. In **Advanced options**, set a name for the Foundry resource, the subscription, a new resource group named `TODO resource group`, and a recommended region.
3. Wait for the project to be created.

The project home page. The API key and endpoints shown on this page were hidden:

![Foundry project home](assets/screenshots/01-foundry-project-home.png)

### 2. Explore the project resources and the portal

1. From the project name menu, select **View all resources** and open the parent Foundry resource to see its projects, users, and connected resources.
2. Review the main sections of the portal: **Catalog** (models and services), **Build** (agents, models, services, tools, knowledge, guardrails, and memory), and **Manage** (costs, quotas, and connectivity).

The parent Foundry resource:

![Foundry parent resource](assets/screenshots/02-foundry-parent-resource.png)

The Build page:

![Foundry Build page](assets/screenshots/03-foundry-build-page.png)

### 3. Deploy a model

1. In **Build** > **Models**, deploy a base model from the catalog using the default settings.
2. When the deployment finishes, the model playground opens.
3. Ask `Who was Ada Lovelace?` and then a follow-up question about her work.

The model deployed:

![Model deployed](assets/screenshots/04-model-deployed.png)

The playground with the model's response:

![Model playground response](assets/screenshots/05-model-playground-response.png)

## References

- [Official AI-901 lab instructions - Get started with Microsoft Foundry](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Exercises/00-explore-foundry.html)
- [Exercise - Get started with Microsoft Foundry (Microsoft Learn)](https://learn.microsoft.com/training/modules/get-started-with-ai-in-azure/6-exercise)
- [Microsoft Foundry documentation](https://learn.microsoft.com/azure/foundry/)
