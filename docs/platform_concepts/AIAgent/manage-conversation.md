---
title: Preview your AI agent   
sidebar_label: Preview AI agent
---



<!-- 
This section helps you tp define rules, access helpful resources, and preview how your bot responds in real time.

## Help section

Help section provides a sample structure that shows how a conversation should be designed. It includes examples of how to define start triggers and write prompts. This helps users understand how to structure conversations.

  <img src="https://cdn.yellowmessenger.com/assets/yellow-docs/keyboard.png" alt="drawing" width="80%"/>

**Key components of the Help section**:

 * **Start trigger sample**: Defines how a conversation begins. Example: "Book a flight" or "Check my order status".
 * **Prompt writing guide**: Provides a sample format for writing clear prompts. It shows how to ask users for input in a conversational and user-friendly way.
Example: "Please enter your flight booking ID to continue".
 * **Sample prompt structue**: Demonstrates how to organize the conversation steps. It displays written outline of how different prompts and responses should connect.
 * **Variable usage tips**: Explains how to use variables in prompts and responses to keep the conversation dynamic and personalized.
Example: Hi `{} var: user_name`, your last booking was for `{} var: destination`.

### Keyboard shortcuts

Help section displays specific shortcut keys to help users access actions and variables faster while designing conversations.
   <img src="https://cdn.yellowmessenger.com/assets/yellow-docs/keywboardshortcuts.png" alt="drawing" width="80%"/>
<br/>



### Define conversation rules at prompt level

Conversation rules guide how the AI agnet should behave based on user input at each prompt.

**Example: Flight booking**

Trip type prompt: "Would you like to book a one-way or round-trip flight?""

**Conversation rules that you define for the above prompt:**

  * If the user says "One-way", save it as the selected trip type and ask for the departure details.
  * If the user says "Round-trip", save it as the selected trip type and ask for both departure and return details.
  * If the user says something else, guide them to choose either "One-way" or "Round-trip".

   <img src="https://cdn.yellowmessenger.com/assets/yellow-docs/conversationrules.png" alt="drawing" width="80%"/>


-->


You can preview AI Agent to test and experience how your AI agent interacts with users in real-time. It simulates live conversations, helping you validate if prompts, workflows, and conversation rules work as expected before publishing the AI agent.

You can preview and test the AI agent using two methods:
* [AI Copilot](#ai-copilot)
* [Preview via agent builder](#preview-via-agent-builder)

### AI Copilot

You can also preview and test the AI Agent using the Copilot, which simulates user sessions and helps in validating both functionality and performance.

To preview via Copilot, follow these steps:

1. Select the AI Agent you want to test.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/selectbot.png)

1. Navigate to **Automation** > **Co-pilot** from the left navigation bar.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/copilot1.png)

2. Start a new session or use an existing test scenario.

3. Interact with the agent to observe how it responds to different queries and whether the flows work as intended.

   ![Copilot preview](/files/Copilotpreview.gif)

### Preview via agent builder

You can also test the AI agent directly within the Agent builder interface.

To preview the AI agent, follow these steps:

1. Go to **Agents**.

2. Click on the **Preview** icon at the top right corner of the screen.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/previewagent.png)

    * A preview panel will open on the right. Use this panel to interact with your agent and test flows.

3. Test the AI agent in the preview panel.

   * Review the responses, check variable values, and see if fallback and workflows are triggered.

4. Click the below high-lighted icon to preview the AI agnet in a different tab.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/preview.png)

