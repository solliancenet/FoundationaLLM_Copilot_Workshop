## Lab2 - Chat Portal Discovery and capabilities
In this lab, we will explore the Chat Portal and its capabilities. We will also look at each part of the User Interface and understand the different sections and features.

> [!NOTE]
> To start this lab, the presenter will go through a demonstration of the Chat Portal and its capabilities. The attendees will then be asked to perform all the tasks in the lab guide.

![Chat Portal](/media/Lab2-1.jpg)

### Task 1: Chat Portal Discovery
Visit the Chat portal site and log in with the credentials that you were provided. Once logged in, explore the portal and familiarize yourself with the different sections and features.

1- **Chat Sidebar**: Where all your sessions are listed and the ability to create new ones with the `+` sign, rename the session or delete it altogether.

2- **Identity**: Your user that you are logged in as.  If you have multiple email addresses for the same user, you can hover over your name to see a tooltip with the email address you are logged in with.

![Identity](/media/Lab2-2.jpg)

3- **Attachment**: The attachment icon allows you to upload files to the chat session.  You can upload images, documents, etc...

![Attachments](/media/Lab2-3.jpg)

4- **Chat User Prompt**: This is where you will be able to type your question to end up being answered by the agent.

5- **Agent Dropdown**: This is where you can select the agent you want to interact with.  You can select from a list of agents that are available to you.

6- **Send Button**: This is the button you will click to send your question to the agent.

## Task 2: Chat with an Agent
In this Task we will start a chat session with an agent in the chat portal.  Select an agent from the dropdown and type multiple questions, one by one.  Click the send button to send each question to the agent and observe the response.

1- **Select Agent**: Click on the dropdown and select an agent from the list. You can select `Monica` for this task.

2- **Type Question**: In the chat user prompt, type a question for the agent.  You can ask anything you like. Example: `Why is the sky blue?`  just to get a feel for the interaction.

3- **Try the following prompts (questions)**: 

### Code Interpreter with OpenAI Assistant

- Write a Python function that reverses the string that was passed into it
- Execute this code with the following input: "Hello, FoundationaLLM!!!"
- Click on the `analysis` hyperlink to view the code that was executed in the sandbox/secure environment
- Create a reverse.py file that contains the function code
- Click on the `analysis`hyperlink to view the code that executed to generate the file, download and show the file.

### File Search Assistance

- Upload the file `ed_thorp_beatthemarket.docx` which is the Ed Thorp beat the market book and ask using the prompt `show the size/num pages of the doc`
- Follow that response with the prompt `Summarize this book?`
- Finally, ask `What is a "call?"` this will demonstrates context awareness as `call` would typically be interpreted as a phone call

### Generation of Graphs - Plotting

- **Prompt:** Show me a graph that contains all these functions: 2*sqrt(-abs(abs(x)-1)abs(3-abs(x))/((abs(x)-1)(3-abs(x))))(1+abs(abs(x)-3)/(abs(x)-3))sqrt(1-(x/7)^2)+(5+0.97(abs(x-.5)+abs(x+.5))-3(abs(x-.75)+abs(x+.75)))(1+abs(1-abs(x))/(1-abs(x))),-3sqrt(1-(x/7)^2)sqrt(abs(abs(x)-4)/(abs(x)-4)),abs(x/2)-0.0913722(x^2)-3+sqrt(1-(abs(abs(x)-2)-1)^2),(2.71052+(1.5-.5abs(x))-1.35526sqrt(4-(abs(x)-1)^2))sqrt(abs(abs(x)-1)/(abs(x)-1))+0.9
- Notice the formation of the Batman logo in the graph that is generated
- Show the analysis of the code generated to create the graph

### Generating 3D Charts - Mutiplot

- **Prompt:** Generate a 3D plot of the following formulas: (01) xy^3-yx^3 (02) (x^2+3y^2)e^(-x^2-y^2) (03) -xye^(-x^2-y^2)

### Analysis of data in a chart for Wealth Management

- Upload the image `quote-chart.jpg` in the data folder and ask the following prompts: Explain this image to someone who is new to reading charts.

### Analysis of financial data using an Excel Spreadsheet

- Upload the file `Sample_10k_Income.xlsx` from the data folder and ask the following prompt:
- **Prompt:** Create a bar chart comparing the `total interest income` versus the `salaries and other personnel expense` by year

## Task3: Branding

In this task, we will explore the branding capabilities of the Chat Portal.  We will change the logo and the color scheme of the Chat Portal.

Every possible `Branding` customization is available in the documentation at [Branding Customization](https://docs.foundationallm.ai/setup-guides/branding/branding-management-portal.html) for you to experiment with.

> [!NOTE]
> We recommend that you experiement with the branding capabilities in the Manamagement Portal to get a feel for the customization that is available to you but reset it after you are done as the portal is shared with other attendees.




