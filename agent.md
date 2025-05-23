# 🧠 AI Agent User Guide

## Overview  
The Agent feature in our platform enables you to create intelligent chatbots powered by your own datasets. You can easily upload or label data sources, configure the agent’s personality and behavior, define its tasks, and choose the AI model that best fits your use case. Additionally, you can enhance your agent by adding tools to extend its capabilities. Each agent can be customized and deployed to support a wide range of use cases, from customer service to internal automation providing a flexible, data-driven solution tailored to your needs.

## 1. Upload or Connect Data  
- Navigate to the **My Data** menu and upload or link the required data to be used as a source for the AI Agent.  

![My Data](/documentation/agent/agent-1.webp)  

## 2. Manage and Integrate Data  
- Go to **Pipeline**, create a new pipeline by clicking **"+ New Pipeline"**.  

![Pipeline](/documentation/agent/agent-2.webp)  

- Input the required agent information and add the **Agent Widget**.  

![Pipeline](/documentation/agent/agent-3.webp)  

## 3. Configure the AI Agent  

### Agent Type

![Agent Type](/documentation/agent/agent-type.webp)  

You can select the type of agent based on your intended use case:

- **Bot**: A chat-based agent designed to interact directly with users. This type allows the agent to respond to messages, answer questions, and perform tasks through conversational interfaces. It's suitable for customer support, virtual assistants, and knowledge-based interactions.

- **Processor**: *(Upcoming)*

### Basic Setting

![Agent Config Basic](/documentation/agent/agent-basic-config.webp)  

In this section, you can customize the core characteristics of your AI Agent to match your specific use case:

- **Agent Name**  
  Set a unique and recognizable name for your agent. This name will be displayed during interactions and helps identify the agent in multi-agent environments.

- **Personality**  
  Define how the agent communicates by setting its tone, behavior, and conversational style. For example, the agent can be friendly, professional, casual, or formal depending on your audience.

- **Tasks (Jobs)**  
  Specify the main responsibilities or goals of the agent. These tasks define what the agent is designed to do, such as answering questions, summarizing documents, or guiding users through a process.

- **Language**  
  Choose the language your agent will use to interact with users. Currently, two options are available: **English** and **Indonesian**. Selecting the appropriate language ensures the agent communicates effectively with your audience.

- **Censorship**  
  Enable content filtering to control which topics the agent is allowed to discuss. This helps prevent the agent from responding to inappropriate, sensitive, or restricted queries.

### Data Source Configuration

![Agent Source Config](/documentation/agent/agent-data-source.webp)  

Configure how your data is labeled and filtered to ensure the AI Agent uses it correctly:

- **Data Source Label**  
  Assign a label to describe the role or type of each dataset. This helps the agent understand how to use the data in context.  
  Available labels:
  - **Data**: General raw information used for reference or processing.
  - **Knowledge Base**: Structured information such as FAQs, manuals, or guides intended for direct user support.
  - **Policy**: Official documents or rules that the agent must follow or reference.
  - **Additional Context**: Supplemental data that helps the agent provide better answers, such as background info or definitions.

- **Data Source Rules**  
  Define filtering rules to control the topics your agent is allowed or not allowed to respond to. This helps ensure the agent only uses relevant and approved data when generating answers.

  Each rule consists of:
  - **Parameter Name**: The specific field or tag in the dataset to evaluate (e.g., `topic`, `category`, or `label`).
  - **Operator**: The condition applied to the parameter. Available operators include:
    - `equal`: Includes data where the parameter exactly matches the given value.
    - `not equal`: Excludes data where the parameter matches the given value.
    - `greater than`: Includes data where the parameter is greater than the specified value (numeric or date-based).
    - `greater than or equal`: Includes data where the parameter is greater than or equal to the specified value.
    - `less than`: Includes data where the parameter is less than the specified value.
    - `less than or equal`: Includes data where the parameter is less than or equal to the specified value.

  Example:
  - Parameter Name: `priority`
  - Operator: `greater than or equal`
  - Value: `3`

  This rule tells the agent to include only data where the `priority` value is 3 or higher.

### Model Selection

![Agent Model](/documentation/agent/agent-model.webp)  

Choose a language model to power your AI Agent. The selected model will handle how the agent understands user input and generates responses.

Currently available models:
- **Volantis Local LLM**  
- **Anthropic Claude 3.5 Haiku**  

### Tools Integration

![Agent Tools](/documentation/agent/agent-selesct-tool.webp)  

Enhance your AI Agent by integrating additional tools that extend its functionality and task-specific capabilities.

Available tools:

- **Model Tool**  
  Attach a specific AI model to your agent to perform targeted tasks such as predictions or domain-specific analysis. For example, you can connect a model that forecasts currency exchange rates based on user input.

- **Create/Write Schema**  
  Enable your agent to interact with structured data by writing user inputs into a predefined schema and reading values from it.
  To enable the Create/Write Schema feature on your AI Agent, first connect the Create/Write Schema transformer through the Tools Integration menu. Then, go to  the Jobs section and provide clear instructions in the prompt so the agent knows how to fill in the database schema based on user input.

- **Webpage** *(Upcoming)*
- **Read Attacment** *(Upcoming)*

By integrating these tools, your agent becomes more powerful, flexible, and aligned with your unique workflows.


## 4. Save Pipeline & Run Job  
- After configuring your pipeline, click the Save button. A popup will appear—select Save Pipeline & Run Job to proceed.
- In the next step, set the execution schedule for the job according to your desired run time.
- Once the schedule is set, click Save Pipeline and Create Job to finalize and run the job.

## 5. Manage AI Agents  
- Go to **Agent Management** to create or view the list of existing AI Agents.  
- Click **"New Agent Widget"** to create a new AI Agent.  

![Agent Management](/documentation/agent/agent-7.webp)  

## 6. Configure the Agent Widget  
- Add a **widget name** and select an existing AI Agent.  
- Set the **default first message** and customize the chatbot appearance to match your brand identity.  
- Click **Create** when finished.  

![Widget Configuration](/documentation/agent/agent-8.webp)  

## 7. Test the Chatbot  
- Run a test to ensure all features are working correctly and meet expectations.  

![Chatbot Test](/documentation/agent/agent-9.webp)  

## 8. Publish the AI Agent  

![Chatbot Test](/documentation/agent/agent-10.webp)  

Once testing is complete, you can publish the chatbot using one of three options:  
- **Embed Code**: Integrate the chatbot into your website.  

![Chatbot Test](/documentation/agent/agent-11.webp)  

- **Publish**: Make it publicly available.  

![Chatbot Test](/documentation/agent/agent-12.webp)  

- **Share**: Distribute it within your organization.  

![Chatbot Test](/documentation/agent/agent-13.webp)  

## 9. AI Agent Ready for Use  
Your AI Agent is now fully configured and ready to support your business or organizational needs! 🚀  
