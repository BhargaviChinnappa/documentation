---
title : RingCentral Integration
sidebar_label : RingCentral Integration
---

Integrate your RingCX Account with IVA Professional to allow agents on RingCentral to leverage IVA Professional's AI capabilities and effortlessly answer live chat queries from users.

This article will help you with the following:

1. [Integrating IVA Professional with RingCX Account](#connect-iva-professional-with-ringcx-account)
2. [Displaying RingCX account's chat widget on the website](#display-ringcx-accounts-chat-widget-on-your-website)
3. [Creating bot conversational flow](#build-bot-conversation-flow--for-ringcentral)

## Connect IVA Professional with RingCX Account

To connect your RingCX account with IVA Professional, you need to create message routing categories, a channel to recieve messages, virtual agents to take up chats and input the API key and API URL in IVA Professional. 

### Create categories for message routing

You need to create categories based on which the user queries will be routed.

1. Log in to your [RingCX account](https://engage.ringcentral.com/).
2. Go to **Categorization** > **Categories**.

   ![](https://i.imgur.com/SIjC5PQ.png)
   
3. Click **New group**.

   ![](https://i.imgur.com/2T3yzmQ.png)
   
4. In **Name**, enter a name for your category and fill in the remaining fields based on your preferences and click **Save**.

   <img src="https://i.imgur.com/fbc5ZU3.png" alt="drawing" width="50%"/>

:::info
You can create separate categories for chats handled by the bot and the chats handled by the agent.
:::

5. Navigate to the category you created, click to expand it, and then select **Add Category**.

    <img src="https://i.imgur.com/kBzvFV1.png" alt="drawing" width="80%"/>

6. Enter the name of the category and click **Save**.    

   <img src="https://i.imgur.com/gTFni8W.png" alt="drawing" width="50%"/>
   
 
#### Fetch category ID

We need the category ID to route the messages to that specific category. 

1. Go to **Digital** > **Exports**.

   <img src="https://i.imgur.com/gwdYsO5.png" alt="drawing" width="70%"/>

2. Select categories and click **Export**.

   ![](https://i.imgur.com/VthlcYB.png)

3. Choose the channel that you have created. 

   <img src="https://i.imgur.com/KBlfrKz.png" alt="drawing" width="50%"/>

4. Select the desired format (Excel or BI) for the export and specify the fields that you want to export, then click **Export**.   

* You will receive a notification via email with the download link.   

5. Open the downloaded excel sheet and go to the category you created in the sheet to copy the **category ID**.

    <img src="https://i.imgur.com/J0Kp4Zy.png" alt="drawing" width="80%"/>

### Create a channel

After creating a category, you need to create a channel to recieve the messages. 

1. Click **Channels** > **New channel**.
   ![](https://i.imgur.com/eoUlj1b.png) 

2. Click **Engage Messaging**.

   ![](https://i.imgur.com/Yhn6YD1.png)

3. Fill **General Settings** as per your preference.

   ![](https://i.imgur.com/u3uwq7G.png)

4. Under **Scope Configuration** select **Enable Web Messaging**.

    ![](https://i.imgur.com/w6xHkvm.png)
    
5. Under **Message settings:**

* In **Default categories**, choose the category created for the bot ([in the previous section](#create-categories-for-message-routing)).
*  In **Default categories (agent messages)**, choose the category created for agent ([in the previous section](#create-categories-for-message-routing)).
 
   ![](https://i.imgur.com/fMT0T9I.png)
 
6. Fill the rest of the fields based on your preference and click **Save**.

   ![](https://i.imgur.com/C5VnJRN.png)
   
### Create a virtual agent

Engage Digital lets you create virtual agents to assist your human agents. Virtual agents provide 24/7 support and can handle first interactions outside regular business hours.

1. Go to **AI Tools** > **Virtual agents** > **New Virtual agent**.

   ![](https://i.imgur.com/0HHTRiJ.png)

2. Click **Intelligent Virtual Agent**.

   ![](https://i.imgur.com/x936uRQ.png)

3. Under **General**, enable **Active** and fill in the following fields:

   ![](https://i.imgur.com/3dB2kBb.png)

    * **Name**: Provide a name to the Virtual Agent.
    * **Role**: Auto-populated by the RingCentral platform as **Virtual Agent Role**.
    * **First Name**: Provide a first name to your agent.
    * **Last Name**: Provide a last name to your agent.
    * **Channels**: Choose the channel created in [this](#create-a-channel) step.
    * **Categories**: Choose the category created in [this](#create-categories-for-message-routing) step.

4. Under **Configuration**, enter the following details.
   
   ![](https://i.imgur.com/CmAC5us.png)

*  **URL**: Enter the webhook URL of your bot.

| Description | URL Format                                                                       |
|-------------|----------------------------------------------------------------------------------|
| Format      | `https://{{region}}.cloud.yellow.ai/integrations/ringCentral/receive/{{bot ID}}` |
| Example     | `https://r1.cloud.yellow.ai/integrations/ringCentral/receive/x1234567890` |

* **Verification token**: Enter **ringcentral_webhook_token**
* **Secret key**: Enter a dummy text as a secret key.

5. Fill the rest of the fields based on your preference and click **Save**. To understand what each each field indicates, click [here](https://support.ringcentral.com/article-v2/Creating-a-new-virtual-agent-in-Engage-Digital.html?brand=RingCentral&product=ED&language=en_US#engage-virtual-agent).

6. Once the Virtual Agent gets created, click the **edit** icon.

   ![](https://i.imgur.com/vm8EXgw.png)

7. Scroll down to **Configuration** and copy the **API access token**.

   ![](https://i.imgur.com/PnPC8gX.png)

Activate identities after creating a virtual agent. Only then user information can be passed.

  ![](https://i.imgur.com/AWtTFTR.png)


   
### Authorize IVA Professional to access RingCX account

1. Log in to your [IVA Professional account](https://cloud.yellow.ai) and go to **Channels** > **RingCentral**.

   ![](https://i.imgur.com/76Bmw03.png)

2. In **API access token**, paste the API token copied in the previous step.
3. In **API URL**, enter the API URL in this format `https://{{ringcentraldomainname}}.api.lab.digital.ringcentral.com` for example, `https://test-account.api.lab.digital.ringcentral.com`
4. Click **Save**.

:::note
Please refer to this [doc](https://developers.ringcentral.com/engage/digital/guide/interactions/structured-messages#channel-capabilities) for nodes supported in RingCX
:::

## Display RingCX account's chat widget on your website

You need to paste the respective channel's script in the HTML file of your website to use RingCX's chat-widget with IVA Professional's AI capabilities.

1. Log in to your [RingCX account](https://engage.ringcentral.com/) and go to **Channels** > click the channel you created.

   ![](https://i.imgur.com/WeP8fsW.png)

2. Scroll down to **Chat connection** and copy the script under **Code to include**.

   ![](https://i.imgur.com/5Agip5T.png)
3. Paste this script in the HTML file of your website.





## Identity fields in RingCentral



Identity fields are personal data points used to uniquely identify and authenticate users. Examples include username, email, phone number, and gender.

The following identity fields from RingCentral are supported in Yellow.ai, allowing updates in RingCentral to be reflected in Yellow.ai and vice versa:

- First name
- Last name
- Gender
- Email
- Cell phone
- Company
- Tags
- Notes

To begin, create the **Company** and **Notes** fields in Yellow.ai’s User360. 

Learn more about [Creating user properties](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/user_data/user_properties#custom-user-properties) in User360.




### Accessing Identity information of known user

If RingCentral already has identity data for a user, you can access these field values within the Yellow.ai bot journey using user properties.

To display user information in the bot, click on the variable icon and select the desired user property.

   ![](https://i.imgur.com/qB51D84.png)

**Example:**  
You can welcome back the user by using a personalized message.


Below is a list of fields you can access in a flow, along with the corresponding expressions:

- Email: `{{{user.email}}}`
- Phone: `{{{user.phone}}}`
- Last name: `{{{user.lastName}}}`
- Gender: `{{{user.gender}}}`
- Tags: `{{{user.tags}}}`
- Notes: `{{{user.notes}}}`
- Company: `{{{user.company}}}`


   ![](https://i.imgur.com/zESO9wa.png)


### When Identity information of an user is unknown

In this scenario, you’ll need to collect user information through the bot journey.

For example, when a user is prompted to provide their email address, it is stored in a user property variable called email_id.

After collecting the email address, the value is updated in the RingCentral portal. This means that the next time the user interacts with the bot, there’s no need to ask for this information again.



---

## Custom fields in RingCentral

Custom fields are user-defined data points that enable the collection of specific information tailored to your application's or organization's needs, extending beyond standard data types.

To use custom fields, you must first create them in the RingCentral platform.

1. In the Admin Portal of the RingCentral platform, navigate to the Digital section and select **Custom Fields** to create the necessary fields.

   ![](https://i.imgur.com/GNxIu0v.png)

2. While creating the fields, you will be prompted to enter a key. Make note of this key value, as you will need it later.

   ![](https://i.imgur.com/uWlGuSe.png)

3. In the Yellow.ai platform, go to **User360** under the Engage section.
4. You will be taken to the User360 screen. Click the **User Properties** button in the top right corner.
5. Select **Custom Attribute** on the bottom left corner. For more details, refer to [Custom fields](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/user_data/user_properties#custom-user-properties) in User360.

   ![](https://i.imgur.com/86bmUDt.png)

6. Paste the key value from Step 2 in the **Property Name** field, choose the same property type you selected in Step 2, and click **Save** (You do not need to include the RingCX prefix).

   ![](https://i.imgur.com/KrGzGpD.png)

7. Then, you can use the custom fields within the bot journey in the same manner as the identity fields.


## Add custom fields for agents

If user information originates from RingCentral, bot developers can access any custom fields included in the RingCentral payload through the channel metadata.


You can access this data in the System Variables section. To accept data from RingCentral, just use `{{data.channelMetadata}}`, as all relevant data is available within RingCentral.

   <center><img src="https://i.imgur.com/0KHym1Q.png" width="65%"/></center>

### Channel metadata structure

The `channelMetaData` variable contains a JSON object structured as follows:

```json
{
  "contentId": "66ec21787a77bd0007d2dc36",
  "sourceId": "659be03f014f1700073cf5f1",
  "userId": "659d746d2fabaa0007689502",
  "identityGroupId": "659d746d2fabaa0007689503",
  "interventionId": "66ec20eb07ea830007d28497",
  "customFields": {
    "policyno": "test123"
  },
  "extraValues": {
    "hello": "world",
    "user_role": "admin"
  },
  "profile": {
    "company": "Yellow.ai",
    "community_id": "659be0166bdf6d0004b0924d",
    "type": "mobile_messaging",
    "uuid": "a6b397e3-9e31-4bcc-bf85-9848]d6cc242ad",
    "firstname": "Tom",
    "gender": "male",
    "identity_group_id": "659d746d2fabaa007689503",
    "lastname": "James",
    "email": "mk@test.com",
    "mobile_phone": "917004000000",
    "emails": ["mk@test.com"],
    "mobile_phones": ["917004324388"]
  },
  "traceId": "19b5e64b8b550d458b2f4433b3c18567",
  "containerType": "new"
}

```

<!--
#### Field descriptions

- **contentId**: Unique identifier for the content.
- **sourceId**: Identifier for the source of the data.
- **userId**: Unique identifier for the user.
- **identityGroupId**: Identifier for the user's identity group.
- **interventionId**: Identifier for the specific intervention.
- **customFields**: Object containing custom fields related to the user or context.
- **extraValues**: Additional key-value pairs that provide more context, such as:
  - `hello`: A sample value ("world").
  - `user_role`: User role information (e.g., "admin").
- **profile**: Object containing user profile information, including:
  - `company`: Name of the user's company.
  - `community_id`: Identifier for the community.
  - `type`: Type of messaging (e.g., "mobile_messaging").
  - `uuid`: Unique user identifier.
  - `firstname`, `lastname`: User's name.
  - `email`, `mobile_phone`: Contact information.
  - `emails`, `mobile_phones`: Arrays of email addresses and phone numbers.
- **traceId**: Identifier for tracing requests.
- **containerType**: Indicates the type of container (e.g., "new").
-->

### Accessing values

To access specific fields within this structure, you can use the following syntax:

- To access the `hello` field in `extraValues`:
  ```handlebars
  {{data.channelMetaData.extraValues.hello}}  // Outputs: "world"
  ```

- To access the `user_role`:
  ```handlebars
  {{data.channelMetaData.extraValues.user_role}}  // Outputs: "admin"
  ```

- To access the user's first name:
  ```handlebars
  {{data.channelMetaData.profile.firstname}}  // Outputs: "Tom"
  ```

:::note
If Yellow.ai intends to push data into RingCentral's custom fields, it is essential to create corresponding custom fields within User 360. 
:::

### Adding custom fields to agent profile
To add custom fields to agent profiles in RingCX:

1. Go to **RingCX Admin portal** > **Digital** > **Custom Fields** > **Add** and create a new custom field.

 ![](https://i.imgur.com/HnvvH07.png)

2. In IVA professional, create a new custom attribute(**Engage** > **User 360** > **User properties** > **+ Custom attribute**). The custom attribute's name should contain the keyword RINGCX as prefix and should have the same name as the custom field created in RingCX account. For example, RINGCX(custom field name).

 ![](https://i.imgur.com/YUP0o17.png)

3. In the flow you have constructed [previously](#build-a-bot-conversation-flow), you can collect dynamic data for the custom field by including a [prompt node](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/prompt-nodes) and [storing the response](https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables#store-data-in-variables) in the user property variable (created in the previous step). Or you can simply type static data in that variable and pass it in the flow.
4. This custom field will appear in the agent profile as highlighted below.

 ![](https://i.imgur.com/SugTBvr.png)




## Build bot conversation flow  for RingCentral

After connecting your IVA Professional account with RingCX, you need to design the flow based on how you want the bot to handle the user chats in RingCX account using Yellow's AI capabilities.

1. Login to you [IVA Professional account](https://cloud.yellow.ai) and go to **Automation** > **Build** > and [create a new flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/journeys#manually-create-a-flow).  
2. Include a [Dynamic chat node](https://docs.yellow.ai/docs/platform_concepts/studio/dynamicchatnode) to the **Start** node.

   ![](https://i.imgur.com/CPo5GDt.png)

:::info

**Tip:**

* You can also [create an intent](https://docs.yellow.ai/docs/platform_concepts/studio/train/intents#add-intents-and-utterances) for the RingCX account and [assign this intent as a trigger for this flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/configureflow#trigger-a-flow-using-intent) in the Start node. Whenever a user types the intent or utterance associated to this intent, the bot will automatically trigger this particular flow.
* Settings in the **Channel options** do not apply to the RingChannel widget.
:::

3. In the **Dynamic chat node**, [type the prompt](https://docs.yellow.ai/docs/platform_concepts/studio/dynamicchatnode#write-your-own-prompts) based on which the bot should function. You can also [use AI to generate these prompts](https://docs.yellow.ai/docs/platform_concepts/studio/dynamicchatnode#generate-prompts-with-ai-prompt-generator). There are several other options using which you can optimize the conversation. Refer to this [doc](https://docs.yellow.ai/docs/platform_concepts/studio/dynamicchatnode) to know everything about the Dynamic chat node.

   ![](https://i.imgur.com/Jl5lswM.png)

4. Connect a [Raise Ticket node](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/action-nodes-overview/raise-ticket) to the Dynamic Chat node and fill the following fields:

   ![](https://i.imgur.com/kLObbST.png)



| Field name | Data type | Description | Sample value |
|------------|-----------|-------------|--------------|
| Live chat agent | - | Choose **RingCentral Live Chat** in the drop-down | - |
| Message after ticket assignment | String | The message that will be displayed to the end user after a ticket is successfully assigned to an agent | Requesting live agent connection. |
| Name | String | Name of the end user | John |
| Mobile | String | Mobile number of the end user | 987600000 |
| Email | String | Email address of the end user. This is a mandatory field | test@gmail.com |
| Query | String | The subject/topic/reason why the ticket was created | I have a concern regarding my flight ticket |
| RingCentral category ID | String | The ID of the category to which the chat should be transferred, click [here](#fetch-category-id) for the steps. | 123abc1abc2abc3abc4abc5abc6 |

You can enable **Advanced Options** to set the priority, auto-translation, custom fields, tags and department.

<img src="https://i.imgur.com/tPS9R0J.png" alt="drawing" width="50%"/>

 Once the dynamic chat node completes its conversation with the user and transfers the chat to RingCX account, this is how the chat looks on RingCX account's side.

 ![](https://i.imgur.com/Xrc60f6.png)


### Nodes supported on RingCentral widget

Most nodes are supported on the RingCentral widget, but there are a few nodes that are not currently supported.

Here’s the revised table with the second and third columns swapped:

| Category | Supported Nodes | Nodes Not Supported |
|----------|-----------------|---------------------|
| [Message nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/message-nodes1/message-nodes) | <ul><li>Text</li><li>Image</li><li>Carousel</li><li>Video</li><li>File</li><li>Quick replies</li></ul> | <ul><li>WhatsApp list</li><li>WhatsApp product catalogue</li></ul> |
| [Prompt nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/prompt-nodes) | <ul><li>Question</li><li>Quick replies</li><li>Name</li><li>Email</li><li>Phone</li><li>Carousel</li><li>Voice input</li><li>Dynamic chat</li><li>Store comment</li><li>File prompt</li><li>Feedback</li></ul>    <br/><b>Note</b>:  <ul><li> The **Dynamic chat node** is not enabled by default; you can send an email to [support@yellow.ai](mailto:support@yellow.ai) to enable this node.</li><li>The **Make Prompt Smarter** option is not supported.</li></ul> | <ul><li>Multi-select node</li><li>WhatsApp list node</li><li>Date node</li><li>Location node</li><li>Speak node</li><li>Input node</li><li>Product search node</li></ul> |
| [Logic nodes](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes) | <ul><li>Condition</li></ul>  | <ul><li>Channel filter</li></ul> |



<!-- 
#### Supported Action nodes:

It supports all the [Action nodes]https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/action-nodes) except the following two nodes.

**Unsupported Action nodes:**


- Date & time validator
- Location validator

-->


## IVA Professional nodes and their supported formats

| Nodes | Supported Formats                       | Sample screenshots|
|-------|-----------------------------------------|-------|
| Image | jpeg, jpg, png, gif                     |   <img src="https://i.imgur.com/SIbhela.png" alt="drawing" width="50%"/>    |
| Audio | MP3, AMR                                |  <img src="https://i.imgur.com/LwNloOn.png" alt="drawing" width="50%"/>      |
| Video | Mp4, MP4, MOV                           |  <img src="https://i.imgur.com/1UwgJd6.png" alt="drawing" width="50%"/>      |
| File  | PDF, DOCX, PPTX, XLSX                  |   <img src="https://i.imgur.com/61AeXRJ.png" width="50%"/>       |

**Structured message:**

|Type| Sample screenshots| Supported formats|
|-----|----------------|----------------|
| Select| <img src="https://i.imgur.com/QIoENt2.png" alt="drawing" width="50%"/> | NA |
| Template| <img src="https://i.imgur.com/HCI0brt.png" alt="drawing" width="50%"/> | NA |
| Carousel | <img src="https://i.imgur.com/HbuyMGF.png" alt="drawing" width="50%"/> | GIF, jPg jpeg, png |
 

## Voice configuration for Ring central

After connecting your IVA Professional account with RingCX, you need to configure a voice flow to handle user calls to a Live Agent through the Yellow platform.

#### Build a Voice flow

1. Go to **Automation** > **Build** > and [create a new flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/journeys#manually-create-a-flow).

2. Add a **Prompt** node and go to its **Settings**.

    <img src="/img/integration/voiceconfig1.png" alt="drawing" width="70%"/>

3. Select **Voice** and add the **Custom SIP headers**. The "key" and "value" fields are mandatory. Set "value" to a boolean (true). The `Key > value > issue` can be customized based on your requirements.

   <img src="/img/integration/voice3.png" alt="drawing" width="80%"/>
   
4. In **Custom voice option**, add the following Key-value pairs:
 
| Key | Value |
|------|------|
| send_info | Set "value" to a boolean "true" | 
| ringcentral_disconnect | Set "value" to a boolean "true" | 

:::note
For new bots, the **Custom voice option** will not be enabled by default. To enable this option, contact the [support team](mailto:mehek.shaikh@yellow.ai) with your Bot ID and environment (Production or Development) details to configure it on the backend.
:::

   <img src="/img/integration/voiceconfig4.png" alt="drawing" width="80%"/>
<br/>   

   
5. Click **Save**.

#### Map IVR number/SIP URI

:::note
To map an IVR number or SIP URI, contact the [support team](mailto:mehek.shaikh@yellow.ai) with your Bot ID and environment (Production or Development) details to configure it on the backend. 
:::

   ![](https://imgur.com/wmkc74l.png)
   
#### Add the IVR number in RingCX 

1. Log in to your [RingCX account](https://engage.ringcentral.com/) and navigate to **AI tools** > **IVA Integrations**.

   <img src="/img/integration/addivrcx1.png" alt="drawing" width="60%"/>
   
2. Select the integration where you want to add the IVR number.

     ![](/img/integration/addivrcx2.png)

3. Paste the copied IVR number in the placeholder `+12XXXXXXXX` in the given URL with your IVR number.
**Development environment SIP URI**: `sip:+12XXXXXXXX@r4dev.sip.yellow.ai:5061`<br/>
**Live environment SIP URI**: `sip:+12XXXXXXXX@r4.sip.yellow.ai:5061`


4. Ensure you replace +12XXXXXXXX with the correct country code and your IVR number in the proper format. Once updated, paste this SIP URI in the** SIP URI** field and click **Save**.

   ![](/img/integration/addivrcx3.png)
     
#### Configure Workflow in RingCX     
     
1. In your RingCX account, go to **Categorization** > **Workflows**.

      <img src="/img/integration/workflowcx1.png" alt="drawing" width="60%"/>
      
2. Select the workflow you created for this integration.

     ![](/img/integration/workflowcx2.png)
      
3. Open **Workflow Studio** to access your workflow.

    ![](/img/integration/workflowcx3.png)
    
14. In the workflow, locate the IVA node and select the IVA integration where the IVR number was added to ensure calls are received on the Yellow platform

    ![](/img/integration/workflowcx5.png)
      
