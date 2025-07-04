---
title: SMS template
sidebar_label: SMS template
---




## 1. Create SMS template

:::note 
* For Indian phone numbers, ensure that the information provided here exactly matches the details entered in the DLT portal. Any discrepancy may result in rejection.
* In certain countries, details like entity ID and template ID may not be applicable. In such instances, you're only required to provide the Sender ID and the template message you wish to send.
:::


1. In the left navigation bar, go to **Engage** > **Templates**.  

2. Click **Create new template** > **SMS**.

   ![](https://i.imgur.com/RRqVdTX.png)
  

3. Create the template using the available options. For descriptions, refer to the following table.

   ![](https://cdn.yellowmessenger.com/xUABq9rVRsiP1649260093253.png)

   Option | Description
   -------- | ---------
   Template name | Name the template. Name should be in lower case, and you can only use underscore as a special character. Example: sms_name
   Sender ID | Provide the number from which you want to send the SMS. For example, you can use a numeric ID like 12345 or a custom name such as MYSHOP. For example, this could be a numeric identifier like 9876543210 or a custom alphanumeric ID such as MYSHOP.
   Template ID | Template ID associated with the SMS message. <br/>For Indian numbers, this identifier is mandated by the DLT (Distributed Ledger Technology) platform to comply with local regulations. It is a numeric value with length between 12 and 19 characters. You can find this against the template from the DLT portal of the brand. <br/> However, for numbers in other regions, such as the US, this may not apply. In such cases, you can input any value or leave it blank, depending on the provider's specifications. Requirements may vary across geographies, so it's best to confirm with the Engage/Channels team for region-specific guidelines.
   Language | Choose the language of the message.
   Body text | Enter the message body. To add variables such as verification code, payment links, or first name, use {{ }}. For Example: {{CustName}}<br/>To create a new variable, use the structure {{*variable_name_comes_here*}} - i.e., the variable name between double curly brackets.

   ![](https://cdn.yellowmessenger.com/VfiEBNhwk6IM1649261672637.png)

4. In **URL click tracking**, select the URLs for which you want to track clicks. Learn more about [URL click tracking](#11-track-url-clicks-in-sms-campaigns). URL click tracking is available only for Premium users.

   ![](https://i.imgur.com/1W8LlCr.png)


:::note
When URL tracking is enabled, the CTA button type changes from STATIC to DYNAMIC. This ensures URL tracking requires a dynamic CTA template.
:::



### 1.1 Setup URL clicks tracking in SMS campaigns

URL click tracking in Campaigns allows you to monitor user clicks on links used in messages.  Before sending out the actual message, the URLs in the template are shortened, and each user is provided with a unique identifier. This allows you to track individual clicks on the links, providing valuable insights into user engagement and campaign performance.

:::note
URL click tracking is currently
* Supported for SMS and WhatsApp campaigns. If you need it for URLs in other channels, please contact us.
* Available only for Premium users.
:::


You can track URL clicks in three different elements of your template - Template body, CTA, and variable.

#### Sample use cases:
1. **E-commerce**: Track how many users clicked on the link to a specific product or offer in your online store.
2. **Surveys**: Measure the response rate by tracking the number of users who clicked on the survey link.
3. **Event invitations**: Monitor the interest level by tracking clicks on event registration links.


To set up URL clicks tracking:
1. Create your marketing campaign with the URLs.
2. Navigate to the **URL click tracking** section and select the URL(s) that you want to track. You will see all the URLs used in the template in the respective sections - this includes URLs in Body text, variables and CTAs.

   <img src="https://i.imgur.com/1W8LlCr.png"/>

3. Click **Create template**.    

4. [Send out the campaign](https://docs.yellow.ai/docs/platform_concepts/engagement/outbound/outbound-campaigns/run-campaign) to users with the template. The URLs in the tracked list are shortened, and a unique identifier is provided to each user before sending.


### 1.2 Track URL clicks in SMS campaigns

To track URL clicks:
1. Go to **Engage** > **Outbound** > Click on the respective **Campaign analytics** icon.
   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/outcamp.png)

2. Scroll down to the bottom of the report.

   <img src="https://cdn.yellowmessenger.com/assets/yellow-docs/templatename.png"/>

   * **Total clicks**: Represents the total number of times the CTA was clicked, including repeated clicks by the same user.
   * **Unique clicks**: Represents the number of distinct users who clicked the CTA. Multiple clicks by the same user are counted only once.


If CTA URL tracking is enabled for a single CTA button, you will see the details of CTA link. If CTA URL tracking is enabled for variable and CTA button, you will see both the metrics as shown below.
   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/CTAlink.png)





***

## 2. DLT compliance for Indian users

Distributed Ledger Technology (DLT) is an account which brands need to create by giving relevant business info. The DLT account is in place to prevent customers from being SMS-spammed.


Template content will undergo review by the DLT portal to ensure message quality. The template can be approved or rejected which you can check from the DLT portal itself.

DLT account is mandatory for the brands to communicate with the customers with transactional & promotional messages.

DLT registration can be done via one of the Telecom operators (in no particular order - Jio, Vodafone, Airtel, BSNL, Tata, PingConnect). Yellow.ai does not recommend any DLT vendor here.

Common details that will be expected during the DLT registration are:

1. Business PAN Number
2. GST number (GST certificate)
3. Business Established Certificate
4. Complete Business Address
5. Business Identity proof (PAN Card)
6. GST registration
7. Letter of Authorization

[LOA Template.docx](https://res.craft.do/user/full/a59774be-e9f6-fe9e-e9df-69fe0168e698/doc/951018E8-27FC-43A5-867B-8A70A19747D8/850ACCCC-8233-46E9-8A3A-85865583C67B_2/LOA%20Template.docx)

### 2.1 Register as an enterprise/business entity/principle entity

You can create the DLT account with your preferred telecom provider.

Search Google for <_telecom_name DLT registration_> (e.g, Airtel DLT registration) or refer to relevant link below. Follow the steps as directed by the selected telecom operator.

1. [Airtel](https://dltconnect.airtel.in/signup/)
2. [Jio](https://trueconnect.jio.com/#/home/entity-registration)
3. [Vodafone](https://www.vilpower.in/signup/)
4. [BSNL](https://www.ucc-bsnl.co.in/signup/)
5. [Tata](https://www.tatatelebusiness.com/regulatory-guidelines/)
6. [PingConnect](https://pingconnect.in/entity/register-with)

Upon successful creation of the DLT account, your brand will be assigned with the 19-digit Entity ID.

### 2.2 Find the Entity ID

**On Airtel DLT**: 👇

![dlt_airtel.png](https://res.craft.do/user/full/a59774be-e9f6-fe9e-e9df-69fe0168e698/doc/951018E8-27FC-43A5-867B-8A70A19747D8/45ADABFB-1828-4E65-BEAF-C67E24A04221_2/dlt_airtel.png)

**On Jio DLT**: 👇

![dlt_jio.png](https://res.craft.do/user/full/a59774be-e9f6-fe9e-e9df-69fe0168e698/doc/951018E8-27FC-43A5-867B-8A70A19747D8/65F4BE38-3B05-4776-A5FA-A1AA5903F674_2/dlt_jio.png)

**On Vodafone DLT**: 👇

![dlt_vodafone.png](https://res.craft.do/user/full/a59774be-e9f6-fe9e-e9df-69fe0168e698/doc/951018E8-27FC-43A5-867B-8A70A19747D8/E2A06110-D90B-44A2-9A87-984640C350F3_2/dlt_vodafone.png)

**On Tata DLT**: 👇

![dlt_tata.png](https://res.craft.do/user/full/a59774be-e9f6-fe9e-e9df-69fe0168e698/doc/951018E8-27FC-43A5-867B-8A70A19747D8/176C7FB2-F52E-43D5-953B-7F1CF07F4385_2/dlt_tata.png)

On PingConnect DLT: 👇

![dlt_pingconnect.png](https://res.craft.do/user/full/a59774be-e9f6-fe9e-e9df-69fe0168e698/doc/951018E8-27FC-43A5-867B-8A70A19747D8/6836B950-8515-4E11-9E5A-D1CA0FC8B516_2/dlt_pingconnect.png)

#### Charges involved 
* Subject to the Telcom operator.

#### Turn around time

* 2 to 5 days (subject to Telecom operator).

:::note
Please use the brand’s email ID for the DLT registration.
:::


### 2.3 Sender ID (or) Header creation & approval

SMS Sender ID or SMS Header should be created in the DLT portal as follows:

1. For Jio DLT → Refer this: [https://messaging.kaleyra.com/support/solutions/articles/3000102267-jio-s-header-senderid-registration-process](https://messaging.kaleyra.com/support/solutions/articles/3000102267-jio-s-header-senderid-registration-process)
2. For Airtel DLT → Refer this: [https://messaging.kaleyra.com/support/solutions/articles/3000102282-airtel-s-header-senderid-registration-process](https://messaging.kaleyra.com/support/solutions/articles/3000102282-airtel-s-header-senderid-registration-process)
3. For Tata DLT → Refer this: [https://messaging.kaleyra.com/support/solutions/articles/3000102289-tata-s-header-senderid-registration-process](https://messaging.kaleyra.com/support/solutions/articles/3000102289-tata-s-header-senderid-registration-process)
4. For BSNL DLT → Refer this: [https://messaging.kaleyra.com/support/solutions/articles/3000102292-bsnl-s-header-senderid-registration-process](https://messaging.kaleyra.com/support/solutions/articles/3000102292-bsnl-s-header-senderid-registration-process)
5. For Vodafone → Refer this: [https://messaging.kaleyra.com/support/solutions/articles/3000102265-vodafone-idea-s-senderid-header-registration-process](https://messaging.kaleyra.com/support/solutions/articles/3000102265-vodafone-idea-s-senderid-header-registration-process)
6. For PingConnect → Refer this: [http://hexasupport.kaleyra.io/support/solutions/articles/3000102269-videocon-s-header-senderid-registration-process](http://hexasupport.kaleyra.io/support/solutions/articles/3000102269-videocon-s-header-senderid-registration-process)

**Other information**

| | |
|- | - |
Turn around time | The Turnaround time (TAT) for successful/unsuccessful registration of Sender ID/Header will vary vendor wise and will be mentioned in the respective links. On an average, 2 days will be taken for approval or rejection of the Sender ID.
Template creation & approval | Once the Sender ID/Header has been approved, next step is to proceed with template creation
TAT for approval or rejection | 3–5 days



### 2.4 Steps to create template

:::note
The User interface may slightly differ for DLT portal from one telecom operator to others. Follow the specific steps as directed by the portal during registration. Below points are for overall understanding of the process.
:::

1. Choose the **Template type** as SMS
2. Choose the **Type of communication** as Promotional or Transactional as needed
3. Choose the appropriate **Category** of the business
4. Choose from one or more already created headers
5. Give an appropriate name to the template
6. Write the exact message content with or without variables as per need
7. Send for approval



### 2.5 DLT Limitations

1. Promotional are for non-customers.
2. Service-explicit, Service-inferred/service implicit, transactional for customers.
3. There is no limit on number of variables inside a template.
4. A Maximum of 30 characters can be passed as a variable.
5. Brand name should be mentioned in the message template.

### 2.6 Run campaigns

Once the SMS channel configuration is successful, next is to send notifications.

Two types of notifications can be achieved with yellow.ai platform.

1. Blast campaigns to a large audience using the Campaign manager
2. 1-o-1 transactional updates to the customers

**For bulk outbound campaign:**

**If the bot is on the app platform**, use the Engagement module to send blast campaigns. For transactional updates, it should be handled by the bot developer at the bot level.

Sending blast campaign from the engagement platform:

1. Upload the CSV in the audience
2. Create a segment based on the desired tags
3. [Schedule campaign](/docs/platform_concepts/engagement/outbound/outbound-campaigns/run-campaign)

**If the bot is on the cloud platform**, to run blast campaigns:

1. Go to **Engage** > **Templates** > Select **SMS** > Create the same template that you created and got approved in the DLT portal. Ensure you add the exact details as added in the DLT portal - without any changes in the line space, case (upper/lower case) and 
2. Add the [audience CSV](https://docs.google.com/document/d/1RCPeDiS4Hv_n0thHRpICK0kQ1RjUpzET365cEEnxpQM/edit)
3. Schedule the campaign as explained in [Create outbound campaign](https://docs.yellow.ai/docs/platform_concepts/engagement/outbound/outbound-campaigns/run-campaign).

**For transactional 1-o-1 updates 👇**

**If the bot is on cloud platform**

1. **Go to Engagement > Templates > Select SMS > Create the same template** that you created and got approved in the DLT portal. Add the exact details as added in the DLT portal. Make sure the message content is JUST THE SAME without any changes in the line space, case (upper/lower case) and such
2. Make use of the V2 Notification API and/or [Workflow campaign](/docs/platform_concepts/engagement/flows_campaign) as per need.


***

**What next?**

After creating an SMS template, create an SMS campaign as explained [here](https://docs.yellow.ai/docs/platform_concepts/engagement/outbound/outbound-campaigns/run-campaign)