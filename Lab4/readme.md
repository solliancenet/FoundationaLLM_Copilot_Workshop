## Lab4 - Embedding and Vectorization Pipelines

In this lab, we will explore the process of creating a new `datasource` with access to multiple documents and then using the `embedding` and  `vectorization` process and pipeline to create indexes in `Azure AI Search`. 

> [!NOTE]
> To start this lab, the presenter will go through a demonstration of invoking an embedding and vectorization of documents in an Azure storage account and explain all the options available through the Management Portal and through the API using POSTMAN. The attendees will then be asked to perform all the tasks in the lab guide.

### Task 1: Create a new Datasource

By January 31st 2025, the Management portal in FoundationaLLM will have the capability to create a new datasource and upload multiple documents to the storage account using the user interface.
For now, we use a POSTMAN Collection to create a new datasource and upload documents to the storage account.

### Starting the process using the API

1. 3 documents have been provided to you in the `data` folder. These documents are `customer_service_data.pdf`, `customer_service_data_2.pdf` and `customer_service_data_3.pdf`. These documents contain the content that we will use to create the datasource and the vectorization profile.

> [!NOTE]
> As you have no access to the Azure Resource Group during the workshop, we added the documents to the storage account for you. You will use the POSTMAN collection to create the datasource and the vectorization profile.

2. **Open POSTMAN**: Open the POSTMAN application and import the collection `New York Workshop Demo.postman_collection.json` that was provided to you in the `data` folder.
3. This collection will allow you to create the datasource, the Vectroization profile and invoke the Vectorization pipeline to create the indexes in Azure AI Search.

![POSTMAN Collection](/media/Lab4-1.jpg)

### Task 2: Create a new Agent

1. **Navigate to the Management Portal**: Log in with the credentials that you were provided. Once logged in, head over to the left sidebar and click on `Create New Agent`.
2. **Fill in the Agent details**: Fill in the first 3 details for the new Agent. You can name it with your own name + `CustomerService` so it does not conflict with the other agents created by the rest of the attendees and provide a description like `Agent with Customer Service RAG for the New York Workshop`.  finaly, enter a welcome message display for the chat portal when a user starts a new conversation with the agent, somethis like `Welcome to the Customer Service agent that is augmented by customer service documents from Contoso, please start your conversation below`. If a message is not provided, the default welcome message will be displayed which is `Start the conversation using the text box below.`

![Agent Details](/media/Lab4-2.jpg)

3. **Knowledge Source**:
   
- Keep the answer to the question `Does this agent have an inline context?` to `No`
- Keep the answer to the question `Do you want this agent to have a dedicated pipeline?` to `Yes`

![Knowledge Source](/media/Lab4-3.jpg)

- In the `Where is the data?` section, select the datasource that you created in Task 1.
  `Screenshot will go here`
- In the `Where should the data be indexed?` section, select the index that you created in Task 1.
  `Screenshot will go here`
- in the `Select the text embedding profile` section, select a profile that was created during the initial deployment for you.
  `Screenshot will go here`
- In the `How should the data be processed for indexing?` section, choose the `Chunk Size` and the `Overlap Size` you wish to use. For the purpose of this lab we will keep it at `500` for chunk size and `50` for overlap size.
  
![Chunk-overlap](/media/Lab4-4.jpg)

- In the `When should the data be indexed?` section, choose the `Manual`  frequency for the purpose of this lab.

![Manual](/media/Lab4-5.jpg)

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

- **Set the System Prompt for the agent:** Give your agent a personality by setting the system prompt. This is the prompt that will be used to generate responses from the LLM. You can set the system prompt to `You are a professional and accurate agent that responds to questions with knowledge and respect. If you don't know the answer respond with "I don't know"`.

![System Prompt](/media/Lab4-6.jpg)

- **Click on `Create Agent`** to create the new agent.

### Task 3: Use the New Customer Service Agent in the Chat Portal

1- **Navigate to the Chat Portal**: Log in with the credentials that you were provided. Once logged in, head over to the top right dropdown and choose the newly created agent you just created.
2- **Start a new conversation**: In the chat user prompt, type a question for the agent. You can ask anything you like that will require private knowledge about content only available in the 3 documents we vectorized previously. Examples: `What was the issue with Emily Davis and how did support handle it?`  just to get a feel for the interaction.  Also try `What was the resolution regarding the support ticket opened for Jessica Walker?`
