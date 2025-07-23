---
title: WhatsApp Frequently Asked Questions
sidebar_label : WhatsApp FAQs
---

### Whatsapp business account 

<details><summary><b> How to verify your business account with Facebook? </b></summary>
<p>

- Document verification:

1. Go to https://business.facebook.com/overview
2. Click on More Tools > Business Settings > Select your Business.
3. Select Security Centre.

You will be able to initiate verification here.
Click [here](https://docs.yellow.ai/docs/platform_concepts/channelConfiguration/whatsapp-configuration#13-verfiy-business-account-with-facebook) for more details.

</p>
</details>


<details><summary><b> Is FB Business account verification mandatory? </b></summary>
<p>

Account verification is no longer a mandate for creating your WA business API account and the WhatsApp bot. Though there are some limitations to the same as mentioned, after completing embedded sign-up or "on behalf of" (OBO) onboarding processes, businesses will be able to:

1. Respond to unlimited customer-initiated conversations (24-hour messaging windows).
2. Send business-initiated conversations to 50 unique customers in a rolling 24-hour period.
3. Register for up to two phone numbers.<br/> <b>Note:</b> It is suggested to complete the business verification before making your bot live on WhatsApp to ensure unlimited business-initiated conversations after the increase in the daily limit tier.

</p>
</details>

<details>
<summary><b>After business verification on WhatsApp, can we change the website URL? Will there be any impact?</b></summary>

Yes, it is possible to change the website URL after business verification on WhatsApp. However, there may be some potential impacts on the business account that need to be considered.<br/>

Changing the website URL may require re-verification or re-approval from WhatsApp. The new URL will need to meet WhatsApp's guidelines and requirements for business verification.
</details>

<details><summary> <b> Do I need a phone number to create a bot on your platform? </b> </summary>
<p>

Yes, you can create a bot on the platform without adding a number and can even test your WhatsApp bot on our test number.

Go to the Whatsapp channel page to find the option to test your bot with the test number. 

</p>
</details>


<details><summary> <b> Will I lose my whatsApp data once I use it as a WABA Business API number?  </b> </summary>
<p>

Yes. Before initiating a WA business API setup on any number, you will have to delete your existing WA account, during which you will lose all existing contacts and conversations. 

</p>
</details>

<details><summary> <b> Where can I initiate Whatsapp channel setup on the platform? </b> </summary>
<p>

You can initiate WA channel setup on the Channels page under WA logo. 

- Visit this URL after logging in on the platform: https://cloud.yellow.ai/bot/yourbotID/channels/whatsapp

- Here is the [link to the document](https://docs.yellow.ai/docs/platform_concepts/channelConfiguration/whatsapp-configuration).

</p>
</details>

<details><summary> <b> How to set up WhatsApp channel?</b> </summary>
<p>

- Requirements & Steps

You will just need a phone number and admin access to the FB business manager account to initiate the Whatsapp channel integration. 

Here is the [URL to the doc](https://docs.yellow.ai/docs/platform_concepts/channelConfiguration/whatsapp-configuration).

</p>
</details>

<details><summary> <b> Can the phone number be used for other purposes like WhatsApp, calling, and so on? </b></summary>
<p>

Yes. The same number can be used for calling but can't be used for personal WA usage as the number would be connected to the platform. 

</p>
</details>

<details><summary><b> Can we use the platform and mobile WhatsApp application to reply to users? </b></summary>
<p>

No. We cannot use the WA application or the phone number once the Whatsapp Business API integration is completed.

</p>
</details>


<details><summary><b> Limitations of Whatsapp? </b></summary>
<p>

Pre-Onboarding:

If onboarded with a WhatsApp Business API solution provider (like WATI):
- The previous chats cannot be seen.
- The number cannot be used on any other WhatsApp apps, including the WhatsApp and WhatsApp Business mobile app.

Post Onboarding:

Businesses can send messages to customers only after a customer initiates a message. These messages are called session messages and can be sent by businesses to customers until 24 hours of the customer sending a message. After 24 hours, the session expires, and businesses can only send "template messages" to their users.
Template messages must be pre-approved by WhatsApp and can be done from the WATI dashboard. All template messages must adhere to WhatsApp Commerce Policies.
- WhatsApp Group Feature is not supported.
- WhatsApp voice or video calls are not supported. Voice notes are supported.
- WhatsApp Message Forwarding Feature is not supported.
- WhatsApp apps cannot be used with the same number if using WhatsApp Business APIs.
- WhatsApp messages cannot be replied to in a thread.

</p>
</details>

<details><summary><b> What is the duration taken for migration? </b></summary>
<p>

It generally takes 24 hours to migrate a number, as the infrastructure setup has to be done at our end.

</p>
</details>

<details><summary><b> Can you still use their notification engine if 2 FA is disabled? </b></summary>
<p>

Yes.

</p>
</details>

<details><summary><b> Will the approved template be moved and used after migration? </b></summary>
<p>

Yes. Once migrated, templates will be moved and used on the same day.

</p>
</details>

<details><summary><b> What is the difference between a WA business application and WA business API? </b></summary>
<p>

WA business application is an Android app that businesses can download but has limited functionality. WA business API is the service provided by the Yellow.

</p>
</details>

<details><summary><b> Can I track the count of users clicking on "Send Message" and landing on the WhatsApp bot when redirecting from Instagram?</b></summary>
<p>

Yes, you can track the count of users clicking on "Send Message" and landing on the WhatsApp bot from Instagram. Follow these steps:<br/>1. Include UTM parameters in the URL that redirects users from Instagram to the WhatsApp bot. For example `http://sample.com?utm_campaign=testcamp&utm_medium=social&utm_source=instagram`.<br/> 2. After users have landed on the WhatsApp bot, navigate to the Insights section of your platform.<br/> 3. Access the Data Explorer or a similar feature that provides analytics and tracking capabilities.<br/> 4. Look for the <b>Message Events</b> section within the Insights or <b>Data Explorer</b>. Here, you will find relevant metrics and data related to user interactions and events within the WhatsApp bot.<br/><img src="https://i.imgur.com/UC4de37.png"/><br/>Make sure to set up the appropriate UTM parameters and utilize the Insights or Data Explorer tool to track user engagement and measure the success of your Instagram to WhatsApp bot redirection.<br/> If you have any further questions or need assistance, reach out to our <a href="mailto:support@yellow.ai">support team</a>.

</p>
</details>


<details><summary><b> Where can I see the verification status of my WhatsApp Business Account (WABA)? </b></summary>
<p>

You can check the verification status of a WABA in the Facebook Business Manager (FBM) account.

</p>
</details>

<details><summary><b> What does the status "Available_Without_Review" indicate for a WhatsApp Business Account (WABA) in Yellow platform?</b></summary>
<p>

The status "Available_Without_Review" indicates that the account has not yet been verified. In this state, the WABA can only be used for testing purposes, as it will have a very low messaging limit.<br/><img src="https://i.imgur.com/YSh18DN.png"/>

</p>
</details>


### Whatsapp Business account setup 


<details><summary><b> What is the character limitation for WhatsApp display name? </b></summary>
<p>

The display name must contain a minimum of 3 characters. There is no such upper case at this moment. 

</p>
</details>


<details><summary><b> About WhatsApp account display name approval? </b></summary>
<p>

WhatsApp has some guidelines to be followed for display name.
The guideline is once display name is changed, it cannot be changed for 30 days.

</p>
</details>

<details><summary><b> About Display name rejection </b></summary>
<p>

Facebook has some guidelines to be followed for display name to be approved. A display name must have consistent branding with external sources(for example, a company's website or marketing).
If they don't feel the display name is abiding all these rules, then they will approve the display name.

- For instance, the Facebook account of the client is in the name of "Tolaram Group" and display name "Colgate" is rejected by Facebook saying there is no link between the two names. So the client has to apply for a new account under the name "Colgate Nigeria."

</p>
</details>

<details><summary><b> How long will it take for the infra setup? </b></summary>
<p>

After you have completed three steps, WhatsApp has to approve your display name, which takes 24 hours to be approved. After that, the infra setup process begins at our end, which takes a maximum of 24 hours to complete.

</p>
</details>

<details><summary><b> About getting stuck at OTP verification </b></summary>
<p>

User is getting stuck at OTP verification probably for two reasons:
1. You already have a WhatsApp business API account with another BSP.
2. If the WhatsApp business account is active, please delete it and retry OTP verification after 5 minutes.

</p>
</details>

<details><summary><b> How can I check if WhatsApp Business API is enabled?</b></summary>
<p>

To check if WhatsApp Business API is enabled for a number, verify if the number is aligned under any BSP (WhatsApp Business Service Provider).

</p>
</details>

<details><summary><b> Is it possible to delete a number from the WABA when switching it to a different bot?
</b></summary>
<p>

No, you should not delete a number from the WABA when switching it to a different bot, as the number is already owned by the WABA. Deleting it can cause errors like "Account not connected". Instead, you should use the admin portal to disconnect the number from the current bot and to connect the number to the new bot.

</p>
</details>

### WhatsApp Configuration


<details><summary><b> How to get the green tick? </b></summary>
<p>

To get a green tick, we have to raise a support ticket on WhatsApp. In this case, please reach out to your POC and share your website and Facebook link with them.

</p>
</details>

<details><summary><b> Can we have multiple numbers added to the WABA account? </b></summary>
<p>

Yes. Multiple numbers can be added to the same WABA account.

</p>
</details>


<details><summary><b> Will the services be affected?</b></summary>
<p>

For 24 hours, the service will remain broken during the migration.

</p>
</details>


<details><summary><b> Can the display name be changed? </b></summary>
<p>

Yes. The display name can be changed after 30 days. 
To change, go to Facebook business manager account and apply for a display name change and then inform your POC about the same.

</p>
</details>

<details><summary><b> Can we use our WhatsApp bot number with another app like lSuperLemon to send abandoned cart notifications?</b></summary>
<p>

No. Once you connect a WhatsApp number with the bot, you cannot use it with other apps at the same time.

</p>
</details>


<details><summary><b> About migrating whatsApp account setup from cloud to app </b></summary>
<p>

Once infra is created, you can connect it to any bot on the platform.

</p>
</details>


<details><summary><b> Where can I add or edit my profile in the bot? </b> </summary>
<p>

To edit the profile picture and description:
1. Go to Channel.
2. Click on WhatsApp where it is connected.
3. Click on Edit.

You can edit all the required information on this page.

</p>
</details>


<details><summary><b> About unable to send notifications to multiple users </b></summary>
<p>

A business starts with 1,000 business-initiated conversations per phone number when it completes business verification.

</p>
</details>

<details><summary><b> How to upgrade my Whatsapp messaging Tier? </b></summary>
<p>

To upgrade your Whatsapp tier and messaging limit, click [here](https://developers.facebook.com/docs/whatsapp/api/rate-limits#quality-rating-and-messaging-limits).

</p>
</details>

<details><summary><b> Can we create multiple chatbots on Whatsapp? </b></summary>
<p>

Yes. Mulitple chatbots can be created with the same WABA account.

</p>
</details>

<details><summary><b> How to get the customers to opt-in for sending notifications? </b></summary>
<p>

There are several ways to get opt-in from from the user.

The following are examples of supported opt-in methods:

- SMS.
- Webpage.
- WhatsApp thread.
- By phone(using an interactive voice response (IVR) flow)
- In person or on paper (customers can sign a physical document to opt in)

</p>
</details>

<details><summary><b>Why bot not responding when it is connected to the WA channel?</b></summary>
<p>

Ensure that you have created the bot with intents and configured the flows using the the same intent.

</p>
</details>

<details><summary><b>Can the WhatsApp bot auto-populate the OTP?</b></summary>
<p>

No, WhatsApp bot cannot automatically enter the OTP.

</p>
</details>

<details><summary><b>Is it possible to identify which user is interacting if two WhatsApp numbers are connected to the same bot?</b></summary>
<p>

Yes, you can identify which user is interacting with the bot by using this`{{{channel.whatsapp.whatsappBusinessId}}}` expression.

</p>
</details>

<details><summary><b>Can we send an attachment in WhatsApp?</b></summary>
<p>

Yes, you can send various types of attachments in WhatsApp including images, videos, and PDF files (pdf).

</p>
</details>

<details><summary><b>How do I get the WhatsApp redirection link?</b></summary>
<p>

To get the WhatsApp redirection link, contact <a href="mailto:support@yellow.ai">Support</a> team.

</p>
</details>

<details><summary><b>It is possible to end a session in WhatsApp?</b></summary>
<p>

No, it is not possible to end the session in WhatsApp.

</p>
</details>

<details><summary><b>Is it possible to hide the WhatsApp phone number in the WhatsApp channel?</b></summary>
<p>

No, it is not possible to hide the phone number. To remove phone number, you need to follow churn process, please connect with the Yellow support team.

</p>
</details>

<details><summary><b>Is it possible to send stickers in WhatsApp chatbot?</b></summary>
<p>

You cannot send stickers in WhatsApp chatbot. A WhatsApp chatbot can respond with simple text messages, images in JPEG or PNG format, audio recordings, videos, documents in PDF or docx format.

</p>
</details>

<details><summary><b>Why are WhatsApp usernames being captured in the conversation log?</b></summary>
<p>
WhatsApp usernames are captured in the conversation log to uniquely identify the user interacting with the bot. This helps in maintaining a record of the conversation and ensures that the interactions are personalized and relevant to the user.
</p>
</details>

<details><summary><b>Why is my WhatsApp chat stuck in a loop, and why are intents and entities not working?</b></summary>
<p>
If your WhatsApp chat is stuck in a loop and intents or entities are not working, follow these steps to resolve the issue:<br/>1. <b>Check configurations</b> – Ensure all WhatsApp channel settings are correctly configured.<br/>2. <b>Train Intents</b> – Verify that the bot is trained with the necessary intents and flows are correctly mapped.<br/>3. <b>Monitor network stability</b> – A stable network connection is essential to prevent message failures.<br/>4.<b> Update permissions</b> – Confirm that the Yellow.ai platform and WhatsApp integration have the required permissions.<br/>5. <b>Test the bot</b> – After making changes, test the bot on WhatsApp to ensure proper flow execution.<br/>6. <b>Debug Intents and Entities</b> – If intents and entities are not triggering correctly, re-train the bot, check confidence thresholds, ensure entity recognition is properly set up, and review conversation logs for misfired intents.<br/><b>Note</b>: If you still encounter any issues, contact the Support team (<b>support@yellow.ai</b>) with all the necessary details.
</p>
</details>

<details><summary><b>Can I connect two different phone numbers from separate WABA IDs in my bot?</b></summary>
<p>
 No, you cannot connect two different phone numbers from separate WABA IDs. To integrate both numbers into the bot, they must be registered under the same WABA ID.
</p>
</details>

<details><summary><b>Which countries support WhatsApp voice calling?</b></summary>
<p>
WhatsApp voice calling is currently supported in India and Indonesia.
</p>
</details>

<details><summary><b>Can we detect if a user has blocked the AI agent’s WhatsApp number?</b></summary>
<p>
 No, it is not possible to determine if a user has blocked the AI agent’s number. WhatsApp does not share this information to protect user privacy.
</p>
</details>

<details><summary><b>Can we detect if a user has blocked the AI agent’s WhatsApp number?</b></summary>
<p>
 No, it is not possible to determine if a user has blocked the AI agent’s number. WhatsApp does not share this information to protect user privacy.
</p>
</details>




