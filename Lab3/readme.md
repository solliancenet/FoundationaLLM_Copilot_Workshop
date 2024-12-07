## Lab3 - Creation of Agents

In this lab, we will explore the process of creating a new Agent in the Management Portal and then using it in the Chat Portal. We will also look at the capabilities of the OpenAI Assistant and how 
it can be used to generate contract templates and specific contracts with details.

### Task 1: Create an Agent with OpenAI Assistant capabilities

1. **Navigate to the Management Portal**: Log in with the credentials that you were provided. Once logged in, head over to the left sidebar and click on `Create New Agent`.

![Create New Agent](/media/Lab3-1.jpg)

2- **Fill in the Agent details**: Fill in the first 3 details for the new Agent. You can name it with your own name so it does not conflict with the other agents created by the rest of the attendees and provide a description like `Agent with OpenAI Assistant capabilities for the New York Workshop`.  finaly, enter a welcome message display in the chat portal when a user starts a new conversation with the agent. If a message is not provided, the default welcome message will be displayed which is `Start the conversation using the text box below.`

![Agent Details](/media/Lab3-2.jpg)

3- **Knowledge Source**: 
- Change the answer to the question `Does this agent have an inline context?` to `Yes`
- That means we will target the LLM directly with our questions with no embedding or vectorization of content at this time.

![Knowledge Source](/media/Lab3-3.jpg)