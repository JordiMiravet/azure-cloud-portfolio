# Get Started with Generative AI and Agents in Microsoft Foundry

## Overview

This lab deploys a generative AI model in Microsoft Foundry, shapes its behavior with instructions and a web search tool, saves the configuration as an agent, and reviews the agent's activity and cost. It uses the services Microsoft Foundry, Foundry Agent Service, and Resource groups.

Based on the official exercise: [Get started with generative AI and agents in Microsoft Foundry](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Exercises/02a-generative-ai.html).

Region used: TODO region.

Model used: TODO model and deployment name.

## Steps

### 1. Create a Foundry project and deploy a model

1. Open [Microsoft Foundry](https://ai.azure.com) and create a project with a unique name. In **Advanced options**, set the Foundry resource name, the subscription, a new resource group named `TODO resource group`, and a recommended region.
2. In the **Catalog**, search for the model and select **Deploy** with the default settings.
3. When the deployment finishes, the model playground opens.

The model deployed:

![Model deployed](assets/screenshots/01-model-deployed.png)

### 2. Chat with the model

1. In the playground, ask `Who was Ada Lovelace?` and then a follow-up question about her work with Charles Babbage. The model understands who "her" refers to because the conversation history is sent with each prompt.
2. Start a new chat and ask `List three facts about Ada Lovelace.` to see how a more specific prompt changes the response.

The conversation with follow-up:

![Playground chat](assets/screenshots/02-playground-chat.png)

The response to the more specific prompt:

![Specific prompt response](assets/screenshots/03-playground-specific-prompt.png)

### 3. Specify instructions

1. Start a new chat and write instructions (the system prompt) that limit the model to answering about the history of computing.
2. Ask questions about ELIZA and how it compares with modern LLMs.
3. Ask an off-topic question to see how the instructions affect the response.

The instructions and the off-topic response:

![Instructions and off-topic question](assets/screenshots/04-instructions-off-topic.png)

### 4. Add a web search tool

1. In the **Tools** section of the playground, make sure **Web search** is enabled.
2. Start a new chat and ask the model to find a vintage computer store near Seattle.

The tool enabled and the response:

![Web search tool](assets/screenshots/05-web-search-tool.png)

## References

- [Official AI-901 lab instructions - Get started with generative AI and agents in Microsoft Foundry](https://microsoftlearning.github.io/mslearn-ai-fundamentals/Instructions/Exercises/02a-generative-ai.html)
- [Exercise - Get started with generative AI and agents in Microsoft Foundry (Microsoft Learn)](https://learn.microsoft.com/training/modules/get-started-with-generative-ai-and-agents/6-exercise)
- [Cost and FinOps in Microsoft Foundry](https://learn.microsoft.com/azure/foundry/concepts/manage-costs)