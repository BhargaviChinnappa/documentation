---
sidebar_label : Create Outbound campaign
title : Create outbound campaign
---


This article provides how to create campaigns for any channel. The process for creating a campaign remains same for all channels. However, certain steps change in *Step 2: Message template* depending on the channel and variables used in the selected template.

## 1. Prerequisites

**For WhatsApp**

* You need to have [Whatsapp channel](https://docs.yellow.ai/docs/platform_concepts/channelConfiguration/whatsapp-configuration) configured with a business number.
* Add only whitelisted templates (approved templates) in the [templates](https://docs.yellow.ai/docs/platform_concepts/engagement/outbound/templates/overview) module.


## 2. Create Outbound campaign

1. On the left navigation bar, go to  **Engage** > **Outbound**.
2. Click **+ Create Campaign**.

   ![](https://i.imgur.com/TRatt3E.png)
  

3. Provide **Basic information**.

   a. Enter a suitable **Campaign name** that resonates well with the purpose of the campaign.

   b. Select your preferred channel through which you want to send communication in active channels.

   c. Click **Next**.
  
   ![](https://i.imgur.com/kKua9g9.png)

  

4. Select your preferred **Message template** using the respective radio button. For more details, see [Templates overview](/docs/platform_concepts/engagement/outbound/templates/overview).

   * [WhatsApp](https://docs.yellow.ai/docs/platform_concepts/engagement/outbound/templates/whatsapptemplate)
   * [Email](/docs/platform_concepts/engagement/outbound/templates/email-template)
   * [SMS](/docs/platform_concepts/engagement/outbound/templates/sms-template)
   * [Mobile push](/docs/platform_concepts/engagement/outbound/templates/mobilepush)
   <!-- * [Google Business Message](/docs/platform_concepts/engagement/outbound/templates/gbm-template) -->
   * [Viber](/docs/platform_concepts/engagement/outbound/templates/viber-template)
   * [Microsoft Teams](/docs/platform_concepts/engagement/outbound/templates/teams-template)

:::note
To view details of a template, click on the respective template. You can also see the preview of the template once you select it.
:::




You will see template configuration slide screen where you need to configure details like variables mapping, user identifier and so on.


5. Configure each template details and click **Next** to continue. 

      ![](https://i.imgur.com/0Dl7IUi.gif)


   * For SMS, choose the user's phone number variable and map the variables used in the template to the user property variable.For more details, [see here](#31-sms-campaign).
   * For Email, choose the variable that contains email Id, select the sender ID (email ID), and map the user variables used in the template. For more details, [see here](#32-email-campaign).
   * For WhatsApp or Viber, choose the variable containing WhatsApp number, sender ID, and map the user variables used in the template. For more details, [see here](#33-whatsapp-campaign).
   * For Microsoft Teams, choose the variable containing **Users contact details**, sender ID, and map the user variables used in the template same as [WhatsApp or Viber template](#34-viber-campaign).  

:::note
* You can select Recipient and other contact details from the user data stored in the **User 360** module.
* To update your audience list, save your campaign as a draft and go to the **User 360** module. you can return and finish it anytime.
:::


  

6. In the **API reference**, select your preferred delivery method. This setting applies only to WhatsApp campaigns.
   * Choose **Default** to apply the organization level setting configured in [WhatsApp API preference](https://docs.yellow.ai/docs/platform_concepts/engagement/engage-settings).
   * Choose **Meta Cloud** to send campaigns exactly at the scheduled date and time, or 
   * Choose **MM Lite** to let Meta optimize and control the actual delivery time after the API call—based on user engagement potential (applicable only for WhatsApp marketing campaigns)
   
   :::note
   * This option is only available for customers who are onboarded to MM Lite and is supported only for WhatsApp MARKETING templates.
   * By default, it applies the configured [Org level setting](https://docs.yellow.ai/docs/platform_concepts/engagement/engage#set-mm-lite-preference-at-org-level).

   :::

7. Select your **Target Audience** and click **Next** to proceed to scheduling the message (**Schedule**).

   ![](https://i.imgur.com/E3dcdyV.png)

   * You can either choose audience from the list of segments that you already created [OR]

   * Create a new segment using **+ Add new segment**. For more details, see [Users module and segment creation](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/overview).

8.  **Schedule** your Campaign: Define when to send the campaign (Timezone: Asia/Kolkata). For detailed procedure, see [Schedule message](#4-schedule-message).  From the options, select 

    * **Once** to run the campaign for one occurrence.
    * **Now** to run after 10 min once you schedule the campaign.
    * **Later** to send out the campaign message on a specific date and time. Use the Calendar box to set your preferred date and time.
    * **Run multiple times** to configure a recurring campaign.

   ![](https://i.imgur.com/ID2pfbl.png)

9. In **Set a goal**, set the objective that you want to track for the campaign. For more details, see [Campaign goals](#6-campaign-goal).

   [](https://i.imgur.com/mdxwOmG.png)

   i. Select and configure your desired goal - [Delivery](#1-delivery-goal), [Conversion](#2-conversion-goal) or [Response](#3-response-goal).

   ii. Set the duration (in hours/days) for which you want to track the goal in **Track the goal for**. For example, if there is a sale in a couple of days, you can set it to track for two days to get the count of messages delivered before the sale ends.

10. Use **Test Campaigns** to test it with internal team members before sending out actual audience. You can add up to five recipients. For a detailed procedure on how to test campaigns, see [Test campaign](#7-test-campaigns-recommended).

11.  **Review and Launch** the campaign. Preview all the campaign details on this page. You can go back to previous steps if you want to make any changes.

   :::note
   Click **Save as draft** to save all your changes. You can resume from here anytime.
   :::

   i. Once you have reviewed all the details and is good to go, click on **Launch Campaign** to schedule.

   ![](https://i.imgur.com/6C7Kpu2.png)

   The system prompts you with a pop-up screen to convert the outbound campaign to a Flow campaign, mentioning all the benefits post-conversion.

   ii. Click Not interested to proceed with creating outbound campaign. [OR] Click **Explore flows** to convert the Outbound flow to a [Flow campaign](https://docs.yellow.ai/docs/platform_concepts/engagement/flow-campaigns-intro).

   ![](https://i.imgur.com/37cuqAw.png)

   You can find the created campaign on the campaign dashboard page.

   ![](https://i.imgur.com/Jc2pmIG.png)
  


***


  
## 3. Configure templates for different channels

This appears in the *Basic information* screen once you select a channel template. You need to configure some settings depending on the channel and template. For example, setting up the sender ID, and mapping variables used in the template.

This section guides you on how to configure template for each channel - 

### 3.1 SMS campaign

1. In **Choose the field that contains users contact or number where they can receive the campaign**, select the variable that contains the user's phone number.
 
   <img src="https://i.imgur.com/pndA2y7.png" width="40%"/>

2. In **Map variables**, associate each variable mentioned in the template with the user variables. You can map a variable or provide a bot link 

   <img src="https://i.imgur.com/12hci2Z.png" class="center" width="60%"/>

3. To monitor URL clicks, select **URL click tracking** for variables that contain URLs. 

   <img src="https://i.imgur.com/QkqZcQr.png" class="center" width="60%"/>

   :::note
   When URL tracking is enabled, the CTA button type changes from STATIC to DYNAMIC. This ensures URL tracking requires a dynamic CTA template.
   :::


### 3.2 Email campaign

1. In **Choose the field that contains users contact or number where they can receive the campaign**, select the variable that contains the user's email address.

   <img src="https://i.imgur.com/Y1h9Ui3.png" width="350" height="auto"/>

2. In **Select the email address from which you want to send the campaign**, choose the email address from which you want to send the campaign. To know how to add email accounts, see [Email channel](/docs/platform_concepts/channelConfiguration/email-outbound)

3. In **Map variables**, associate each variable mentioned in the template with the user variables. You can map a variable or provide a bot link 

 

### 3.3 WhatsApp campaign 

1. In **Choose the field that contains users contact or number where they can receive the campaign**, select the variable that contains the WhatsApp number (mobile number) of the user.

   <center><img src="https://i.ibb.co/V0hcZLTc/image.png" width="40%"/></center>

2. In **Sender ID**, choose the WhatsApp business number from which you want to send the campaign.
   
   <img src="https://i.imgur.com/sNtatZX.png"/>

3. In API preference, choose your preferred delivery method for sending WhatsApp messages.
   * **Default**: Uses your organization-level WhatsApp API preference and applies it automatically based on the selected template category.
   * **MM Lite**: Uses Meta’s smart delivery to optimize message timing, helping you reach customers when they are most likely to engage.
   * **Meta Cloud**: Sends messages through the standard Meta Cloud API without delivery-time optimization.
   <center><img src="https://i.ibb.co/pvqss4Hx/4.png" width="40%"/></center>
4. In **Map variables**, associate each variable mentioned in the template with the user variables. You can map a variable or provide a bot link.

4. To monitor URL clicks, select **URL click tracking** for variables that contain URLs.

   <center><img src="https://i.imgur.com/QkqZcQr.png" class="center" width="60%"/></center>

5. Use **Media** to configure personalized media for the campaign.
   *  **Static** media: Select to send a common media file to all the recipients. Use **Browse** to upload the media file.
   *  **Dynamic** media: Select this option to send personalized media to each user. Map the column from the database where you have included these details. For instance, you can send WhatsApp campaigns with personalized video media to your customers.<br/> <br/>To insert a property dynamic URL:<br/>a. [Create a user property](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/user_data/user_properties#custom-user-properties) with the data type set as URL.<br/><center><img src="https://i.imgur.com/l1CSdNF.png" width="60%"/></center><br/>b. [Store the image URL for each user to that user property](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/user_data/store_conv_data).<br/>c. Associate the media with this user property when scheduling the campaign.<center><img src="https://i.imgur.com/umvqXL4.png" width="50%"/></center>

### 3.4 Viber campaign 

1. In **Choose the field that contains users contact or number where they can receive the campaign**, select the variable that contains the user's WhatsApp number (mobile number).

   <center><img src="https://i.ibb.co/JFKy4x31/image.png" width="350"/></center>

2. In **Sender ID**, choose the WhatsApp business number from which you want to send the campaign.
   
   <center><img src="https://i.imgur.com/sNtatZX.png"/></center>

3. In **Map variables**, associate each variable mentioned in the template with the user variables. You can map a variable or provide a bot link.

***

## 4. Schedule message

As explained in the Step 6, you can choose when to run your campaign. However, there are advanced options to customize scheduling your message and make your campaign more effective.

### 4.1 How many times you want to run the campaign

Choose whether to run the campaign only once or on a recurring basis.

  

##### Run once

* Select **Now** to run after 10 min once you schedule the campaign.

* Select **Later** to send out the campaign message on a specific date and time. Use the Calendar box to set your preferred date and time.

   ![](https://i.imgur.com/WbcjAKS.png)

  

##### Run multiple times

Select this to schedule a recurring campaign.

   ![](https://i.imgur.com/ui1kPCZ.png)


*  **Repeat**: Select the frequency of running the campaign.

*  **Daily**: Set your preferred date and time.

*  **Weekly**: Select the day of the week (Sun-Sat) when you want to run the campaign and set your preferred **Time**.

*  **Monthly**: Select the date of the month (1-31) when you want to send out the message and set your preferred **Time**.

*  **Ends**: Choose when you want to end the campaign.

  

| Option | Description |
| -------- | -------- |
| never | To run the campaign for ever |
| on | To end on a specific date and set the desired date and time. |
| after | to end after n number of occurrences and configure the respective options

  
  


  
  

### 4.2 Business hours

  

This lets you honor DND timings, so that you can prevent users from receiving campaigns during specific periods, such as late nights.

  

You can set business hours for each day of a week so that your campaign message will be sent out only during the configured business hours.

  

1.  **Enable Business hours**.

   ![](https://i.imgur.com/mCl051T.png)

  

2. Click on **+ Add business hours setting** > **Add new business hour**.

3. Click on each day of the week and configure business hours for that particular day. Enable **Business hours same every day** to set a common timeframe for all days.

   <img src="https://i.imgur.com/eKA9G36.png" width="80%"/>

  
  
  

4.  **Message handling during DND hours**

   You can configure what to do with the messages after the configured business hours using the following options.

   ![](https://i.imgur.com/POhWjum.png)

*  **Discard the message**: The message will not be sent and will be marked failed.

*  **Postpone to next day**: The campaign will be paused and will resume the next business hours.

  
   ![](https://i.imgur.com/63KYDaH.png)

  
:::note
You can Pause a scheduled campaign and Resume it when required using the respective options from the Outbound campaign homepage.

   ![](https://i.imgur.com/BlRcStg.png)


:::

## 5. Segments

  

Segment is grouping of users based on certain condition sets. Segmentation can be based on city, tags, names, or any another user property.

* You can add multiple condition sets as required.

* In the below example, a segment is created with users whose country is mentioned as "india" from the User module.

   ![](https://i.imgur.com/pAxeftX.png)

  

* When you select a segment, you can see the number of users in it.


   <img src="https://i.imgur.com/EvsUIXd.png" width="80%"/>

:::note
If you upload a CSV while the campaign is still executing, it will cause additional users to enter the segment. This will result in an audience size larger than initially planned for the campaign.
:::


***

## 6. Campaign goal

The campaign goal represents a specific objective that you want to achieve through the campaign. Campaign goals can vary depending on the purpose of the campaign and the desired outcome. 

Tracking the progress of campaign goals is important to ensure the effectiveness of the campaign in meeting its objectives. This could include the template used, user segment targeted, scheduled time, or any other parameter.

Goals are categorized into three types depending on the purpose of the campaign:

#### 1. Delivery goal

The delivery goal helps you track the messages delivery status and assess the campaign reach. For example, for promoting a new outlet, your goal could be the number of messages delivered. 

Currently, there are three delivery statuses supported - sent, delivered, and read. However, not all channels support all three statuses. For example, the message read cannot be tracked for SMS.

  ![](https://i.imgur.com/KAEGKoJ.png)
   
   * In **What do you want to track**,  select the delivery status to track.
   
  

#### 2. Conversion goal 

This refers to the process of identifying a specific user action or interaction that indicates a successful completion of a predefined objective or desired outcome.

When users perform the conversion event, it signifies that they have taken the intended action or achieved the goal you have set for the campaign. This could be anything from making a purchase, signing up for a newsletter, filling out a form, or any other action that aligns with the campaign's objectives.

   ![](https://i.imgur.com/2jDXx4C.png)


In **Select event**, choose the event that you want to track.

#### 3. Response goal

This goal assists in tracking the reactions or clicks received for the campaign. However, CTA events from WhatsApp are not captured, and button clicks are not included in the tracked events by default. This option will be enabled only if there are CTAs present in the message template.

![](https://i.imgur.com/ozLtuBo.png)

   * **Select Any response**: Tracks all types of responses received for the campaign.
   * **Button clicks**: This records when users click on a specific button within the campaign.


***

## 7. Test campaigns (Recommended)

It is recommended to test your campaign with internal or test users before launching to ensure the campaign notifications are flawless. Especially, verify if images, buttons, deep links, and elements of personalization are working or rendering as expected.

The following are the benefits of testing a campaign before launching -

* Prevent sending wrong content to the customers.
* Enables viewing the notification messages as and how the end-users receive.
* Ensures the variables are mapped to the right user properties.
* Reduces campaign failures due to mismatch in parameters or issues with images size.

#### Prerequisites for adding test user details

* Test users data should be available in the *User 360* module
* Test users should have all the data which will be mapped to the variables used in the template.

#### Test campaign


1. Once you Schedule a campaign, you will see an option to Test campaign in Step 8 of [Create campaign](#2-create-outbound-campaign), Review and launch.

   ![](https://i.imgur.com/CzxSZrO.png)





2. Click on **Test campaign**.

   ![](https://i.imgur.com/Xfxyepv.png)



3. Search for test users.

* A wizard will be opened to add test user details.

* You can search users by name, email, phone number or userID. You will see auto-suggestions in the drop-down as you type.

   ![](https://i.imgur.com/UqXJZ3h.gif)

  
  

4. Add test users

   a. Click on the relevant user to populate all values like recipient ID and other parameters if any.

   b. Check whether all the parameters are mapped correctly to the desired user columns.

   c. Ensure all the values are available for the user. If not, use a different user use whose required details are available.

   ![](https://i.imgur.com/mPC8ArU.png)


   d. To add more users (up to 5 test users) click on **+Add Users** and repeat the process.

   
   ![](https://i.imgur.com/OFDwZvH.gif)

  

5. Click on **Send test campaign** to trigger campaign to the selected users.

   ![](https://i.imgur.com/AV194YX.png)


You will see the *Sending* status. You can see the actual delivery status after a while (about 15 seconds) - Delivered or Failed.

   <img src="https://i.imgur.com/Sm9nuYW.png" width="90%"/>


* To send the test campaign to more users, click on **Send new test campaign**.

   <img src="https://i.imgur.com/UsOTzmX.png" width="80%"/>


For Failed messages, you can also see the reason for failure.

:::note
* It takes 15 seconds to update the sent status of messages.
* If there is any mismatch in the data, save the campaign using **Save as draft**. Then, navigate to templates step, correct your mappings and test again.
:::

***

## 8. Campaign errors

Here are some common errors that you may encounter when working with campaigns:

:::note
For API related error codes and descriptions, see [Notification API response codes](https://docs.yellow.ai/docs/platform_concepts/engagement/outbound/notification-engine#24-response-codes).
:::

## 9. Notifications on Campaign status & progress

You can get notified via email for critical campaign status and progress alerts. For broader awareness and efficient resolution of campaign-related concerns, you can specify preferred users to receive notifications in case of any issues with the campaign. By default, email alerts are sent automatically to the template creator for critical template statuses and to the campaign creator for campaign failures due to template disablement.


To enable email alerts:

1. On the left navigation bar, click **Engage** > **Preferences**.
2. Toggle the **Enable campaign alerts**.

   <img src="https://i.imgur.com/RNSylY5.png"/>

3. Check **Send alerts on campaign progress** to receive campaign progress related updates. By default, **Send alerts when campaigns are paused/failed** is enabled, you cannot uncheck it.
4. In **Sending email alerts** enter your preferred email addresses separating each with comma (,).

   <img src="https://i.imgur.com/jaGOOCM.png" width="60%"/>

5. Click **Add**.



**What next**

* See how your campaign is performing using [Outbound campaign report](/docs/platform_concepts/engagement/outbound/outbound-campaigns/outbound-report).