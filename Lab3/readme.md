## Lab3 - Creation of Agents

In this lab, we will explore the process of creating a new Agent in the Management Portal and then using it in the Chat Portal. We will also look at the capabilities of the OpenAI Assistant and how 
it can be used to generate contract templates and specific contracts with details.

> [!NOTE]
> To start this lab, the presenter will go through a demonstration of creating an Agent in the Management Portal and explain all the options available. The attendees will then be asked to perform all the tasks in the lab guide.

### Task 1: Create an Agent with OpenAI Assistant capabilities

1. **Navigate to the Management Portal**: Log in with the credentials that you were provided. Once logged in, head over to the left sidebar and click on `Create New Agent`.

![Create New Agent](/media/Lab3-1.jpg)

2- **Fill in the Agent details**: Fill in the first 3 details for the new Agent. You can name it with your own name so it does not conflict with the other agents created by the rest of the attendees and provide a description like `Agent with OpenAI Assistant capabilities for the New York Workshop`.  finaly, enter a welcome message display in the chat portal when a user starts a new conversation with the agent. If a message is not provided, the default welcome message will be displayed which is `Start the conversation using the text box below.`

![Agent Details](/media/Lab3-2.jpg)

3- **Knowledge Source**: 
- Change the answer to the question `Does this agent have an inline context?` to `Yes`
- That means we will target the LLM directly with our questions with no embedding or vectorization of content at this time.

![Knowledge Source](/media/Lab3-3.jpg)

4- **Agent Configuration**:
- For the `Conversation History` **enable** the conversation history and set the maximum Message to 10. This will allow the user to include the last 10 messages in the prompt in the chat portal.

![Conversation History](/media/Lab3-4.jpg)

- Keep the Gatekeeper disabled for now. This will be used in a later lab.

![Gatekeeper](/media/Lab3-5.jpg)

- **Choose your orhestrator:** Select the orchestrator that you want to use for this agent. You can choose between `Langchain`, `Semantic Kernel`, `AzureOpenAIDirect` and `AzureAIDirect`. For this lab, we will choose `LangChain`.

![Orchestrator](/media/Lab3-6.jpg)

- **Choose your AI Model:** Select the LLM Model you would like to use for this agent. Several LLM Model have already been deployed for the workshop, for the purpose of this Lab use `GPT-4o` based model to conintue.

![AI Model](/media/Lab3-7.jpg)

- **Add the `OpenAI Assistant` capability**: Enable the OpenAI Assistant capability for this agent. This will allow the agent to generate responses based on the OpenAI Assistant model.

![OpenAI Assistant](/media/Lab3-8.jpg)

- **Create an optional cost center:** This is optional and can be used to track the cost of the agent. You can create a new cost center and call it `New York Workshop`. 

![Cost Center](/media/Lab3-9.jpg)

- **Set an expiration date for the Agent:** This is optional and can be used to set an expiration date for the agent. You can set the expiration date to `March 31st 2025`.

![Expiration Date](/media/Lab3-10.jpg)

5- **System Prompt**: 

- **Set the System Prompt for the agent:** Give your agent a personality by setting the system prompt. This is the prompt that will be used to generate responses from the LLM. You can set the system prompt to `You are a professional and accurate agent that responds to questions with knowledge and respect.`.

![System Prompt](/media/Lab3-11.jpg)

- **Click on `Create Agent`** to create the new agent.

### Task 2: Use the New Agent in the Chat Portal

1- **Navigate to the Chat Portal**: Log in with the credentials that you were provided. Once logged in, head over to the top right dropdown and choose the newly created agent you just created.

![Choose Agent](/media/Lab3-12.jpg)

2- **Start a conversation with the Agent**: In the chat user prompt, type a question for the agent that would require the use of the OpenAI Assistant capability. You can ask a question like `Generate a template document that I can use to help with Merger and acquisitions, be detailed and accurate`.

3- **Observe the response**: The agent should respond with a generated contract template that you can use for Merger and acquisitions. The response should be detailed and accurate based on the GPT-4o model and contains placeholders as we asked for a template.

![Agent Response](/media/Lab3-13.jpg)

4- **Continue the conversation**: You can continue the conversation with the agent by asking more questions or providing more details for the contract template. For this lab, you can ask the agent to generate a specific contract with details for a hypothetical merger and acquisition scenario. using the template just generated.

**Prompt:** `Use this template to create a legal document for a company called Contoso Corporation with the main location at 11 Times Square New York, NY 10036`

5- **Observe the response**: The agent should respond with a specific contract document for the company `Contoso Corporation` based on the template that was generated. The response should be detailed and accurate based on the GPT-4o model and contains the details you provided including the address. 

![Agent Response](/media/Lab3-14.jpg)

6- Finally ask the agent to download a word document version of the contract. The agent should respond with a link to download the word document version of the contract.

![Agent Response](/media/Lab3-15.jpg)

7- **Analysis:** Click on the `analysis` hyperlink to view the code that was executed in the sandbox/secure environment to create and download the contract document. You can see the code that was executed to generate the document for Contoso download the file using the `OpenAI Assistant` that was added as a capability to the agent.

![Agent Response](/media/Lab3-16.jpg)

