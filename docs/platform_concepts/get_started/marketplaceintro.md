---
title: Marketplace template 
sidebar_label : Marketplace templates
---

## Overview

Yellow.ai marketplace contains more than 100 pre-built bot templates for the most common business use cases to help fast-track building solutions for customers and prospects.  

This is a one-stop solution that helps you quickly build conversational agents for your use case without prior coding or platform knowledge. You can import a fully functioning template that we have built for you with a click of a button. 

We have 100+ templates and components on Marketplace spanning across Ecommerce, Automobile, Healthcare, Ed-tech, BFSI, and Employee Experience verticals. Along with the templates, we have flows which are frequently used reusable components which we have researched and are present across most customer use cases. 

Some prime examples of frequently used flows are ‘Chat with an Agent’ or ‘Change Language’. Similarly, you will find a host of flows/templates built around integrations with applications like CRM, Payments, Live Agents, and Marketing Clouds among others.

In this article, you will learn:

1. [How to browse for the required template](#12-search-templates-using-keywords)
2. [How to preview and experience a demo of template](#21-preview-selected-template)
3. [How to use the selected template in your bot](#22-use-template-in-your-bot)
4. [How to edit or delete the flows inside your template](#3-edit-imported-flows)


## 1. Choose a right marketplace template 

### 1.1 Open marketplace 

To start customizing a bot with the help of our templates, login to [yellow.ai](https://cloud.yellow.ai/auth/login) and click **Marketplace** from the overview page.

> Click [here](https://cloud.yellow.ai/marketplace) to visit marketplace. 


![](https://i.imgur.com/oQJRB60.jpg)


There are different ways in which you can fetch the template that you are looking for. See the following sections for details. 

:::info
**Sort templates**   

You can sort the template list by popularity or recently added. 
![](https://i.imgur.com/EXT9Vk1.png)
:::

### 1.2 Search templates using keywords

Search for the templates using keywords related to your use case. You can also filter the search results by specific purpose. Select the respective filter that you want to apply. 

- **Kick starter**: Bank templates, payroll management, eCommerce, attendance monitoring, etc. 
- **Flow**: Download flows to track orders, browse products, get feedback, etc. 
- **Integrator**: Templates with integrations such as SAP, Twilio, Salesforce, etc.
- **Validator**: Templates used for validating PAN or Aadhar numbers. 

![](https://i.imgur.com/5veE3JM.png)



### 1.3 Filter templates by Industry, Use case, and Channels

To make your search experience easy, there are several filters available on the Marketplace template. You can get templates of a specific industry, use case, and/or channel. You can choose more than one value in filter using the checkbox.

Filter templates for the following:
1. **Most common use cases**: Employee Engagement, Customer Engagement, Enterprise Automation, Customer Support, and WhatsApp For Business. Select the use cases that you would need.
2. **Channels**: There are templates created to support 22 different channels. Select the channel(s) for which you want to see the supported templates.
3. **Industry**: Templates are available for Agriculture, Automobile, B2B, BFSI, E-commerce, Energy & Utilities, HR, Healthcare, IT, Lead Generation, Manufacturing, and Travel. Select the industry by which you want to filter templates.


![](https://i.imgur.com/5cJ8FHS.png)


### 1.4 Explore collections

Templates are categorized into 7 different collections. You can explore templates of each collection and use the right one for your bot. You can further filter the template list by use case, channels, or industry.

![](https://i.imgur.com/MlEkolg.png)


***

## 2. View & import template

### 2.1 Preview selected template 

1. To see a template, click on any template name (or View icon). 

   ![](https://i.imgur.com/m5VECfy.png)

   You will see the template details such as supported channels, supported languages, number of user installs, key features, description, etc. 

   ![](https://i.imgur.com/zuYvhvA.png)

2. Click **Preview** to try the demo of how the bot functions in real-time. 

   ![](https://i.imgur.com/lxSkaNt.png)

3. Interact with the preview bot.

   <img src="https://i.imgur.com/7FYZVtd.png" alt="drawing" width="50%"/>



### 2.2 Use template in your bot

1. To import the template, click on any template name (or Use template icon). 

   ![](https://i.imgur.com/Wey5PYw.png)

- (Or) You can also open the template and click **+Use template**.

   ![](https://i.imgur.com/SP1uMq4.png)

2. Choose the bot that you want to add this template (these flows) and click **Use template**.

   ![](https://i.imgur.com/0uV4TOP.png)

:::note

**Export flows from one bot to another**

If you have an existing flow that is being used in one of your bots and you want to use the same flow in the current bot, you can do with the help of Marketplace component feature. This feature can be used when the available templates on our Marketplace does not match your requirement, but there is a functioning flow which is already existing on yellow.ai platform in another bot.
Click [here](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/exportflow) to learn how. 
:::

3. Flows will be imported and trained automatically for your bot. 


## 3. Edit imported flows 


To edit imported flows, go to **Automation** > **Build** > **Flows** and edit the flow. Learn more about flows and how to edit flows [here](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/journeys). 

The following actions can be performed after exporting the template: 



#### Delete flow

If you have exported flows that are not relevant to your use case, you can delete the flows by clicking the menu on the right and selecting **Delete**. 
For example, if you have exported the same flow twice, one flow can be deleted or if your bot does not require verification, that flow can be deleted. 

![](https://i.imgur.com/u3yhreX.png)

#### Clone flow

If you want to reuse one flow more than once, you can clone the flows by clicking the menu on the right and selecting **Clone**. While cloning you can enter a custom flow name and description. 
For example, the 'Bike Models' and 'Bike Models clone' flow will have the same flow except the models displayed through it will be different. 

![](https://i.imgur.com/6fvtk0R.png)


#### Edit flow 

:::info

To import and use specific flows directly from the Marketplace into a **Sandbox or Development** environment, open the Flows section, click **+Create new flow**, and import from Marketplace.

:::

To edit a flow: 

1. Open the flow by clicking on the flow name. 

![](https://i.imgur.com/gfw2hy9.png)

2. **Edit text**: Text inside each node can be rephrased. Open any node and enter the text in **Bot says**. For example,  "Remember me? I'm Mia, here to collect your AADHAR information." can be changed to "Hey! Please provide your AADHAR information."

<img src="https://i.imgur.com/ypOZfjh.png" alt="drawing" width="70%"/>

3. **Add new nodes**: New nodes can be added when required. 


| Nodes         | Description |
| ------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Prompts**  | Prompts can be used when the bot expects a user to respond to the posed question. Click [here](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/prompt-nodes) to learn more.                           |
| **Messages** | Messages can be used when the bot has to display information to the user without expecting any response. Click [here](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/message-nodes1/message-nodes) to learn more. These nodes can be used to provide a human touch to the conversation. |
| **Action**   | Actions are non-interactive nodes that can be used to perform a specific task. Click [here](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/action-nodes) to learn more.                            |
|    **Logic**   |  Logic nodes can be used when the flow must be branched based on the given conditions. Click [here](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes) to learn more.  |

4. **Delete nodes**: You can delete a few unnecessary nodes provided in the default flow by clicking the delete icon. After deleting the node, connect the node to the next node so that the flow persists. 

![](https://i.imgur.com/7O9NTQz.png)

5. After editing, click **Publish changes**. 

![](https://i.imgur.com/oRoCiRc.jpg)





:::info

1. Learn how to **export flows** from one bot to another, [click here](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/exportflow)
2. Learn to **debug the flows** in the template you imported, [click here](https://docs.yellow.ai/docs/platform_concepts/studio/test-and-publish-bot/debug-flow). 
3. Learn how to **publish the changes** after customizing your bot, [click here](https://docs.yellow.ai/docs/platform_concepts/studio/test-and-publish-bot/modes).
:::
   


