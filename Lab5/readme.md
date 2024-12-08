## Lab5 - Content Safety and Data Protection

In this lab, we will explore the ability to protect the conversation against `Hate`, `Violance`, `sexuality` and `Self Harm` while also protect sensitive information that should never be revealed or disclosed during a conversation. 

### Task 1: Content Safety and Data Protection Enablement

1- **Navigate to the Management Portal**: Log in with the credentials that you were provided. Once logged in, head over to the left sidebar and click on `All Agents`.
2- **Select your Agent**: Click on the `Edit` gear for the agent that you created for customer service.

![Edit Agent](/media/Lab5-1.jpg)

3- **Content Safety and Data Protection Configuration**:

Head to the section of the `Gatekeeper` and enable the `Content Safety` and `Data Protection` features. Choose `Azure Content Safety` and `Microsoft Presidio` respectively.

![Gatekeeper](/media/Lab5-2.jpg)

### Task 2: Test the Content Safety and Data Protection

1- **Navigate to the Chat Portal**: Log in with the credentials that you were provided. Once logged in, start a new session with the agent that you created for customer service.

2- **Test the Content Safety**: In the chat user prompt, type a question that contains a hate speech or a violent word. Example: `Show me all the support tickets that express violence or hate against our support personnel`. 

3- **Observes the response**: The response should be a warning that the content is not allowed and the agent will not respond to such content.

4- **Test the Data Protection**: In the chat user prompt, type a question that contains a sensitive information like a credit card number or a social security number. Example: `From the support ticket for Henry King, what was his social security number given?`.

5- **Observes the response**: The response should be a warning that the content is sensitive and the agent will not respond to such content.