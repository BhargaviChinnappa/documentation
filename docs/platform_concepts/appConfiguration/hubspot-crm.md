---
title : Hubspot CRM
sidebar_label : Hubspot CRM
---

The HubSpot CRM integration enables direct management of your HubSpot CRM account through yellow.ai's bot. This integration allows effortless creation, retrieval, updating, deletion, and searching for contacts in your HubSpot CRM account directly from the bot interface.


## Supported Hubspot CRM actions in Yellow.ai
Once the integration is established, you can perform the following HubSpot CRM actions directly from the bot interface.

| Action  | Description |
|--------- | -----------|
| Create a contact |    Creates a new contact |
| Get a contact | Fetches a particular contact |
| Delete a contact | Deletes a contact |
| Update a contact| Modifies details of a particular contact |
| Search a contact by phone| Looks for a contact using phone number |
| Search a contact by email| Looks for a contact using email address |

## Connect Hubspot CRM with Yellow.ai

**Prerequsites:**

1. An active Hubspot CRM account
2. An active yellow.ai account.

To connect your Hubspot CRM account with Yellow.ai, follow the these steps:

1. On the left navigation bar, go to **Extensions** > **Integrations** > **CRM** > **Hubspot**. Alternatively, you can use the Search box to find the integration app.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/hub-spot.png)

2. In **Give account name** give a unique name to your Hubspot CRM account and click **Connect**.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/hub-spot.png)

:::info
1. In a two-tier environment, add account names in Development and use them in Live.
2. In a three-tier environment, add accounts in Staging and Sandbox, and they'll be available in Production.
:::

3. Sign in to your **Hubspot CRM** account when prompted. From there, select the Hubspot CRM account you want to link with Yellow.ai and click **Choose Account** to authorize Yellow.ai to access **Hubspot CRM**.
 
   <img src="https://i.imgur.com/8hvI81j.png" alt="drawing" width="60%"/>

4. You can add up to 15 accounts. To add another Hubspot CRM account, click on **Add account** and follow the steps mentioned above.


## Enable events for Hubspot CRM actions

For the bot to perform certain actions when an event occurs in Hubspot CRM, the event needs to be activated.

The following are the events available for Hubspot in Yellow.ai:

| Event                      | Description                               |
| -------------------------- | ----------------------------------------- |
| hubspot-contact-created    | Contact is created in Hubspot       |
| hubspot-contact-changed    | Contact is modified in Hubspot     |
| hubspot-contact-deleted    | Contact is deleted in Hubspot      |
| hubspot-contact-merged     | Contacts are merged in Hubspot       |
| hubspot-contact-restored   | Contact is restored in Hubspot     |


### Add webhook to receive events

You need to add the webhook URL from the integration page in your Hubspot CRM app to receive the events mentioned above. To do so:

1. Go to **Hubspot CRM integration** and copy the Webhook URL.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/hub-webhook.png)

2. Go to your **Hubspot CRM** account and click the **Settings** icon.

   ![](https://i.imgur.com/x1eUiqz.png)

3. Go to **Integrations** > **Private Apps** and click **Create a private app**.

   ![](https://i.imgur.com/7r7HQyo.png)

4. In **Basic Info**, enter a **Name** and **Description**. You can also upload a logo for that app if required.

   ![](https://i.imgur.com/QiTtI94.png)

5. Go to **Scopes**, and enable the scopes for the actions for which you wish to recieve events from Hubspot.

   ![](https://i.imgur.com/dlWYtXU.png)
   
6. Go to **Webhooks** and past the Webhook URL copied in step 1. then, click **Create Subscription** to create the app.

   ![](https://i.imgur.com/otbZ7pA.png)

7. In the following screen, select the object types and the events you'd like to get notified. Then, click **Subscribe**.

   
   <img src="https://i.imgur.com/REVgszK.png" alt="drawing" width="50%"/>
   
 8. Click **Create app** on the top right corner.

   ![](https://i.imgur.com/BkgUaxh.png)


### Activate events in Yellow.ai

 To activate an event and use it in your flow,

1. Go to **Event** > **Integrations** and search for Hubspot events and click **Activate** next to the respective event.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/hub-event.png)

3. Go to a flow and include that event in the Start node and [build the flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/journeys#2-create-a-flow) to carry out the action when that event occurs.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/hub-event-trigger.png)
    

## Manage Hubspot CRM via Yellow.ai AI agent

To manage your Hubspot CRM account through yellow.ai bot, follow these steps:

1. Go to **Automation** and [create a flow](https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/journeys#2-create-a-flow) based on your requirement. 

2. In whichever point you want the bot to access Hubspot CRM, inlcude the Hubspot CRM node. For that, drag the node connector, go to **Integrations** > **Hubspot**.

   <img src="https://cdn.yellowmessenger.com/assets/yellow-docs/hub-node.png" alt="drawing" width="60%"/>

3. Configure the **Hubspot CRM** node based on the descriptions provided in the following:

   <img src="https://cdn.yellowmessenger.com/assets/yellow-docs/create-contact.png" alt="drawing" width="60%"/>

* **Account name:** Choose the Hubspot CRM account.
* **Action:** Choose the [action](#supported-hubspot-crm-actions-in-yellowai) to be performed.
* Depending on the selected object, the corresponding fields will be shown. To fill those fields, you need to collect it as an input from users beforehand. Construct the flow accordingly and [store the data in variables](https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables#41-store-data-in-variables). These variables will then be passed in those fields.


4. Each Hubspot CRM action returns a response as a JSON object. [Store that response in a variable](https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables#41-store-data-in-variables) and [pass that variable](https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables#42-retrieve-data-from-variables) in a [message node](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/message-nodes1/message-nodes) to display that response to the end user.

For example, if you receive the following response, you can use this syntax ``` {{{variables.variablename.results.0.properties.lastname}}}  ``` to filter out the contact's last name.

```
{
  "total": 0,
  "results": [
    {
      "createdAt": "2019-10-30T03:30:17.883Z",
      "archived": false,
      "id": "512",
      "properties": {
        "company": "Biglytics",
        "createdate": "2019-10-30T03:30:17.883Z",
        "email": "bcooper@biglytics.net",
        "firstname": "Bryan",
        "lastmodifieddate": "2019-12-07T16:50:06.678Z",
        "lastname": "Cooper",
        "phone": "(877) 929-0687",
        "website": "biglytics.net"
      },
      "updatedAt": "2019-12-07T16:50:06.678Z"
    }
  ],
  "paging": {
    "next": {
      "link": "?after=NTI1Cg%3D%3D",
      "after": "NTI1Cg%3D%3D"
    }
  }
}
```

-----




