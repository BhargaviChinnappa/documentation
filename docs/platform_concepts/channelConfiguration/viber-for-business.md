---
title: Viber for business
sidebar_label : Viber for business
---

Viber is a messaging and voice-over app, which is used to interact with registered users, especially in countries like Eastern Europe, the Middle East, and Southeast Asia.

A Viber for business is a Viber business message account that allows you to send messages to your customers using their phone numbers. You can send transactional, promotional, and conversational messages. The platform supports both 1-way and 2-way communication for Viber business. Businesses can use Viber for marketing, sales, and customer support. 

Using your Viber business account, you can raise a support enquiry with an airline company over chat, collect survey responses and feedback, explore new furniture offerings conversationally, and so on.

In this article, you will learn:

* [How to create a Viber business account?](#create-a-viber-business-account)
* [How to connect Viber business channel to your brand?](#connect-viber-business-channel-to-your-brand)
* [How to access Viber business account?](#to-access-viber-business-account)
* [How to change Webhook?](#change-of-webhooks)
* [How to test your bot on Viber?](#test-your-bot-on-viber)

## Create a Viber business account

To create a Viber business account, you need to send your business details to our Yellow.ai support team. Based on the details provided, your Viber business account and business card are set up.

#### Prerequisites

* Raise a product query/support ticket on JIRA with type PSD board, including all the details to create a Viber business account and business card. 
* Send all the details of the sandbox, staging, and production bot IDs in the ticket.
* The yellow product team might take one working day to review the documents submitted. If no change is required, then the product team will submit the details to the Viber business team.
* The Viber business team will take up to one week to approve the Viber business channel request. 
* If there are any changes or additional information required, then you need to share the expected details.	

:::note
After activating your account, if you want to change the information related to your business, you need to reach our support team. The support team will request Viber businesses to change the required information.
:::

### Add your business details

Provide all your business details as per the information in the following table:

Option| Description
-------- | ---------
Business name | Enter the name of the company to appear in your monthly billing reports or billing system. | 
| Business category | Select the relevant categories that suit your business: <li> Media Agency</li> <li>Financial Institution</li><li> Community Org</li><li>Govt./non- govt Org</li><li>Publisher </li><li> Commerce </li><li> E-commerce </li><li> Real estate and construction companies </li><li> IT and Internet companies </li><li> Education </li><li> Healthcare</li><li> Transportations </li><li> Retail </li><li> Others</li> |
| Registered country | Select the country in which your business is registered. |
| Message type | Select your preferred message type: one-way and two-way. | 
| Destination countries | List down the destination country of your targeted users. | 
|Sample messages | Add sample bot messages. | 
| Business launch date | Select the date when you want your Viber business account to be activated. |
| Warranty letter | Share the [Viber business warranty letter](/files/Viber-business-warranty-letter.docx) in the expected format on the company’s letter head. This warranty letter is required to ensure that the company adheres to Viber's guidelines and legal requirements when sending messages to users, including obtaining consent from opted-in customers, complying with applicable laws, following Viber's service messages guidelines, and preventing unauthorized use of the verified messages channel by third parties.  | 

### Setup your business card

To set up a business card, you need to provide the details of your brand to appear on Viber such as your **business name**, **description**, **address**, **phone number**, **website**, and **logo**. Ensure that, you send the logo images with a size of **50\*50, 65\*65, 100\*100, 130\*130, 360*280** (mandatoy). The supported image types are JPG and PNG

<img src="https://i.imgur.com/sWcCeCf.png" alt="drawing" width="60%"/>

After creating an official Viber business account, a unique business Id or service Id is created for your brand. You need to use these details while connecting your brand to Viber business channel.		
		
## Connect Viber business channel to your brand

To connect Viber's business channel to your brand, you need to follow these steps:

1. On the left navigation bar, click **Extensions**.

    ![](https://imgur.com/PIOvT6K.png)

2. Click **Channels** > **Messaging** > **Viber for business**.

   ![](https://imgur.com/17d2En5.png)

3. Enter **Viber business service ID** and **Message TTL**, which are generated after creating an account, and click **Save**.

   ![](https://imgur.com/Z9fff2k.png)
	
4. Navigate to the **Overview** page, under **Active channels** section, you can see that Viber business channel is successfully connected to your bot.
	
	![](https://imgur.com/698n2UW.png)
	
## To access Viber business account
	
To access your Viber business account, follow these steps:
	
1. Ensure that Viber app is installed on your phone.
2. Replace `<<service_ID>>` with your account service ID in the generic URL format, `viber://chat?service=<<service_ID>>`. For example, `viber://chat?service=12345`
3. Click on the link to navigate to the Viber business account in the app.
	
## Change of Webhooks
	
While switching from a development to Production environment (in case of 2-tier platform) and from Sandbox -> Staging -> Production (in case of 3 tier), it is important to change the Webhook. In order to change the Webhook, you need to raise a ticket to the yellow product team with Viber business service ID and bot ID details.

## Test your bot on Viber

After connecting your bot to Viber, you can test your bot by downloading the Viber app on your mobile device from the Playstore.

To test your bot on Viber, follow these steps:

1. Open the Viber app that you have downloaded on your mobile device and search for your bot.

2. Search for your bot and start the conversation to test the chatbot. Ensure that you have created the bot with intents and configured the flows with the same intent.

   <img src="https://imgur.com/FtvF3yR.png" width="40%"/>
    
* If the intent does not match, the bot should be able to respond with a fallback message.    

3. To view the entire conversation between the bot and user, navigate to the **Inbox** module in the platform and select **Bot messages** in the **Chats** section.

   ![](https://imgur.com/8Zjimdm.png)
