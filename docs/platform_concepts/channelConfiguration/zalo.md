---
title: Zalo
sidebar_label: Zalo
---

Zalo is an instant messaging application that allows you to send text messages, create and join group chats, and share photos, videos, and audio. This app was developed by VNG Corporation, a Vietnamese technology company. It is supported on both iOS and Android devices.

Businesses can use Zalo to communicate with their customers, respond quickly to customer inquiries, provide customer support, promote their brand by sending promotional offers, and host virtual meetings with colleagues and customers.

In this article, you will learn:
* [How to create a Zalo official account?](#create-zalo-official-account)
* [How to setup a Zalo channel using Developer portal?](#setup-zalo-channel-using-developer-portal)
* [How to connect Zalo business channel to your bot?](#connect-zalo-channel-to-your-bot)
* [How to test your bot on Zalo channel?](#test-your-bot-on-zalo)


## Create Zalo official account

1. Go to [Zalo website](https://oa.zalo.me/home) and click **Create Official Account now**.

   ![](https://i.imgur.com/wW1lYlA.png)

2. Choose the account type that you wish to create. Click **Enterprise** as the account type.

   ![](https://i.imgur.com/BJ6ckdw.png)
   
3. Click **Register** to proceed further.

   ![](https://i.imgur.com/HT352pb.png)

4. Select the required subcategory, enter your business details, and click **Create an OA account**.

   ![](https://i.imgur.com/pnCOWxW.png)
   
5. Verify the information that you provided and click **Confirm** to register your official account.

    <img src="https://i.imgur.com/ctPBoaG.png" alt="drawing" width="60%"/> 

	
6. After registering for an OA account and submitting the authentication profile, Zalo OA BQT will verify the account information and respond within 7 working days. 

## Setup Zalo channel using developer portal

To set up a Zalo channel using the developer portal, use this [link](https://developers.zalo.me/). Once your channel is set up in the developer portal, you can get the **OA server key** and **Access token ID** to connect your bot to the Zalo channel.

To setup Zalo channel using developer portal, follow these steps:

1. Login to the developer portal using the URl `https://developers.zalo.me/`.

2. Select your **Official Account** and click **Link**.

   ![](https://i.imgur.com/m5di5ye.png)

3. You need to enable all the required permissions.

   ![](https://i.imgur.com/VDNR5q4.png)
   
### Configure Webhook on Zalo channel

After connecting to your official account on the developer portal, you need to [setup a Webhook](https://developers.zalo.me/docs/api/official-account-api/webhook/gioi-thieu-ve-webhook-post-4219) on the Zalo. Enter the Webhook URL shared by the yellow.ai product team to test your bot on the Zalo channel. 

To configure Webhook on Zalo, follow these steps:

1. Click on **Webhook**, and enter the URL shared by the yellow.ai product team.

   ![](https://i.imgur.com/tahIfUZ.png) 
   
2. You can enable all the required permissions based on your requirements.
   
   ![](https://i.imgur.com/N5WTVXY.png)
   
3. Copy the **OA Secret Key**.
   
   ![](https://i.imgur.com/oxOFK36.png)

4. Navigate to **Settings** tab and copy the **App id**.

    ![](https://i.imgur.com/1kvYbgr.png)   
  
5. Select **API Explorer** from the **Tools** drop-down.

   ![](https://i.imgur.com/FI5ke8H.png)
  
6. Select **OA Access token** from the **Access token type** drop-down.

   ![](https://i.imgur.com/acPoIAH.png)
   
7. Select your account from the **Lay Access Token**.

    ![](https://i.imgur.com/bFvqmj9.png)

8. Agree to allow the application to manage the Official Account and click **Allow**.

   <img src="https://i.imgur.com/TimLjWW.png" alt="drawing" width="80%"/>
  
9. Copy the **Access token**.

   ![](https://i.imgur.com/3R48lse.png)

### Add DNS TXT record to verify Webhook URL domain

In order to verify the Webhook URL domain, you need to add Zalo DNS TXT to Yellow.ai's domain.

To verify the Webhook URL domain, follow these steps:

1. Select Domain Authentication and enter a domain based on the bot region, for example, `cloud.yellow.ai` or `r1.cloud.yellow.ai`. Click **Accuracy**.

   ![](https://i.imgur.com/r9km3E6.png)
  
2. If your domain is not verified, click **Verify now**.

   ![](https://i.imgur.com/kbFkuJF.png)

2. Copy the content value to establish the [connection between the Zalo channel](#connect-zalo-channel-to-your-bot) and your bot on the platform. 

   ![](https://i.imgur.com/plj0GDc.png)

3. Once your bot is connected to Zalo, open the following link and keep it active for 10–20 minutes in a browser window:

   `https://cloud.yellow.ai/zalo_verifierVzQC6wkaBK1jshzBv_ibOnRbZKpwcbmMDpG.html?bot=<botID>`

   To create the above URL, follow these steps:

   1. Expand **Upload an HTML file to your website** drop-down and copy the highlighted query path.

      ![](https://i.imgur.com/B3Eh4tJ.png)  

   2. Enter the domain (for example, https://cloud.yellow.ai) that you have specified during the verification and paste the copied query parameter (zalo_verifierVzQC6wkaBK1jshzBv_ibOnRbZKpwcbmMDpG.html). 

   3. Append your bot ID as a Parameter (`bot=<botID>`) to the URL.

4. Go back to **Domain Authentication**, enter your domain in the input field to verify your domain, and click **Accuracy**.

     ![](https://i.imgur.com/x48ZD4q.png)

* Your domain will be successfully verified.   

   <img src="https://i.imgur.com/I1lTg2Z.png" alt="drawing" width="60%"/>

## Connect Zalo channel to your bot

To connect the Zalo channel on the Yellow.ai platform, follow these steps:

1. On the left navigation bar, click **Extensions**.

    ![](https://imgur.com/PIOvT6K.png)

2. Click **Channels** > **Messaging** > **Zalo**.

   ![](https://imgur.com/lmP3bzo.png)
   
2.  Enter the **OA server key**, **Refresh token**, **App ID**, and **Zalo DNS TXT** that were copied from the developer portal, and then click **Save**.   
   
    ![](https://imgur.com/YUT0vHF.png)

3. Your Zalo channel will be successfully connected. 

:::note
If you don't use your bot for 3 months, the "refresh token" will expire. You'll get an email asking you to manually reset the "refresh token" in the Zalo developer portal. Once you reset it, a new "refresh token" will be created. You can add this token to our platform to reconnect your bot
:::

## Test your bot on Zalo

After configuring Webhook, you can test your bot on the Zalo channel and you can start responding to the user queries.

To test your bot on Zalo, follow these steps:

1. Navigate to your Official Account

   ![](https://i.imgur.com/LzTtcXe.png)

2. Click **Manage > Account Management > account information**. In this section, you can see the QR Code.

   ![](https://i.imgur.com/H8zlSyf.png)
   
3. Scan the QR Code to chat with your bot. Click on **message** to start testing with your bot.   

    <img src="https://i.imgur.com/Nsv10ho.jpg" alt="drawing" width="60%"/>
	 
4. Once you have tested your bot, the configuration of the Zalo channel for your business is completed.