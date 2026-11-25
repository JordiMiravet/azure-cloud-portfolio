# Get Started with Microsoft Foundry

## Overview

This lab creates a Microsoft Foundry project, explores the Foundry portal, deploys a model, and connects a client application to the project to try text analysis, speech, computer vision, information extraction, and safety guardrails. It uses the services Microsoft Foundry, Azure Speech in Foundry tools, and Resource groups.

Based on the official exercise: [Get started with Microsoft Foundry](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Exercises/00-explore-foundry.html).

Region used: Spain Central.

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

The Catalog page:

![Foundry Catalog page](assets/screenshots/03-foundry-catalog.png)

The Build page:

![Foundry Build page](assets/screenshots/04-foundry-build-page.png)

The Manage page:

![Foundry Manage page](assets/screenshots/05-foundry-manage-page.png)

#### Note about the lab sessions

During the initial deployment attempts, the model deployments failed because the maximum output token limit was not configured correctly. The deployment required a maximum output token limit of 30,000.

After correcting this configuration, the model was successfully deployed. Due to the time limitations of the Azure lab environment, the exercise was continued across two separate lab sessions.

### 3. Deploy a model

1. In **Build** > **Models**, deploy a base model from the catalog using the default settings.
2. When the deployment finishes, the model playground opens.
3. Ask `Who was Ada Lovelace?` and then a follow-up question about her work.

The model deployed:

![Model deployed](assets/screenshots/06-model-deployed.png)

The playground with the model's response:

![Model playground response](assets/screenshots/07-model-playground-response.png)

### 4. Connect the Computing History app

1. From the project home page, take note of the project endpoint, the deployment name, and the API key. These are credentials and are not shown in this document.
2. Open the [Computing History Agent](https://aka.ms/computing-history-foundry) app provided by the exercise, enter those values in its configuration panel, and save.

### 5. Explore AI capabilities with the app

Each capability was tried in a new conversation.

**Generative AI.** Asked about the ELIZA chatbot and how it compares with modern large language models.

![Generative AI response](assets/screenshots/08-app-generative-ai.png)

**Text analysis.** Asked the agent to summarize a short article and identify people, places, and dates.

![Text analysis response](assets/screenshots/09-app-text-analysis.png)

**Speech.** Used voice input to ask about computer speech. The response was returned as text and read aloud.

![Speech response](assets/screenshots/10-app-speech.png)

**Computer vision.** Uploaded an image of a vintage computer provided by the exercise and asked about it.

![Computer vision response](assets/screenshots/11-app-computer-vision.png)

**Information extraction.** Uploaded an image of a printed circuit board provided by the exercise and asked what could be identified from it.

![Information extraction response](assets/screenshots/12-app-information-extraction.png)

**Safety guardrails.** Tried prompts asking for harmful help to see how the model reacted.

![Guardrails response](assets/screenshots/13-app-guardrails.png)

### 6. Clean up

1. In the Azure portal, open the resource group used for the lab.
2. Select **Delete resource group**.
3. Type the resource group name to confirm and select **Delete**.

Deleting the resource group removes the Foundry resource, the project, and the model deployment, which avoids unnecessary charges.

![Resource group deleted](assets/screenshots/14-resource-group-deleted.png)

## Result

The Foundry project was created, a model was deployed and tested in the playground, and the Computing History app answered using that deployment for text, speech, and image prompts. TODO describe what the guardrails did with the prompts you tried.

## Lessons Learned

- A Foundry project organizes models, agents, and tools, and belongs to a parent Foundry resource in an Azure subscription, where several projects can share services and settings.
- Models are deployed in the Foundry resource and can be tested in the playground before being used from an application.
- A client application needs the project endpoint, the deployment name, and an API key to use a deployed model. The key is a credential and must never be committed or shown in screenshots.
- Text analysis, image interpretation, and information extraction were all done by the same deployed model through prompts, while speech used Azure Speech in the Foundry tools of the same resource.
- Foundry models apply content safety guardrails by default.
- Model deployments depend on regional quota, so a different model or region may be needed if the quota is missing.
- Deleting the resource group removes the project and everything it contains.

## References

- [Official AI-901 lab instructions - Get started with Microsoft Foundry](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Exercises/00-explore-foundry.html)
- [Exercise - Get started with Microsoft Foundry (Microsoft Learn)](https://learn.microsoft.com/training/modules/get-started-with-ai-in-azure/6-exercise)
- [Microsoft Foundry documentation](https://learn.microsoft.com/azure/foundry/)
