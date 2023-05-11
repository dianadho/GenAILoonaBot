# GenAILoonaBot
Finding the Right Answers in Reproductive and Menstrual Health
## About the project
Our research project explores how well can ChatGPT and Roo (Planned Parenthood Chatbot) answer women’s reproductive and menstrual health queries in comparison to the existing resources. In order to determine if the response from the LLM is sufficient, we considered these three factors: factuality, accessibility, and timeliness. As the source of truth, we evaluated these responses against the most trusted online resources for women’s health which are Bedsider and Planned Parenthood.

# Getting Started
Follow these steps to reproduce our analysis
## Prerequisites
ChatGPT
1. Go to [Open AI Chat](https://chat.openai.com/) in your preferred browser
2. Enter your email address or use single sign-on via Google or Microsoft account 

Roo
1. Go to [Roo](https://roo.plannedparenthood.org/chat) in your preferred browser
2. Enter your information to start chatting with Roo

Azure Language Studio
1. Create an [Azure subscription](https://azure.microsoft.com/en-us/free/ai/) for free

## How to use the files
[Bedsider Verified Questions and Answers](https://github.com/dianadho/GenAILoonaBot/blob/main/BedsiderVerifiedQA.csv) is the data scraped from Bedsider's verified FAQ that can be used to train/test your own LLM

[Evaluation Chatgpt vs Roo](https://github.com/dianadho/GenAILoonaBot/blob/main/EvalChatVsRoo.csv) is our analysis of the LLM's responses classified as correct, incorrect, or refused to answer

[Prompt Engineering Evaluation](https://github.com/dianadho/GenAILoonaBot/blob/main/PromptEngEval.csv) shows how we modified the prompt to avoid Roo refusing to answer

## Create your own LLM
1. Log into [Language Studio](https://language.cognitive.azure.com/) with your Azure credentials
4. Scroll down to the **Answer questions** section and select **Open custom question answering**
5. Conect your resource to Azure Search
6. Select Enable custom question answering, choose the Azure Search resource to link to, and then select **Apply**
7. Refresh the page and create a new project
8. On the left menu bar, click **Manage sources** and click **Add source**
9. Add [Bedsider Verified Questions and Answers](https://github.com/dianadho/GenAILoonaBot/blob/main/BedsiderVerifiedQA.csv) 
10. Select **Test** from the menu bar to talk to your LLM
11. Select **Inspect** to examine the response in more detail
12. Follow [instructions](https://learn.microsoft.com/en-us/azure/cognitive-services/language-service/question-answering/quickstart/sdk?pivots=studio&tabs=macos#test-your-project) if you want to manage your knowledge base, deploy your project, or review suggestions
