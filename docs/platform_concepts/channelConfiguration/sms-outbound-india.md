---
title: Configure SMS service for Indian numbers
sidebar_label: Configure SMS service for Indian numbers
---

#### SMS Channel configuration on Yellow.ai platform

The pre-requisites for configuring the SMS outbound channel varies country-wise.

For India, the pre-requisites are as follows:

Raise a ticket with the product team with the following details:

1. Entity ID of the DLT account
2. Registered SenderIDs (or Headers)
3. Bot ID, bot URLs with environments (e.g, staging, Production), and API keys

Product team will configure the SMS channel in the platform.

**TAT:**

1-2 days


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

Search Google for `<_telecom_name DLT registration_>` (e.g, Airtel DLT registration) or refer to relevant link below. and Follow the steps as directed by the selected telecom operator.

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
TAT for approval or rejection | 3-5 days



### 2.4 Steps to create template

:::note
The User interface may slightly differ for DLT portal from one telecom operator to other. Follow the specific steps as directed by the portal during registration. Below points are for overall understanding of the process.
:::

1. Choose the ’Template type’ as SMS
2. Choose the ‘Type of communication’ as Promotional or Transactional as needed
3. Choose the appropriate ‘Category’ of the business
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

1. Blast campaigns to a large audience using the Campaigns manager
2. 1-o-1 transactional updates to the customers

**For bulk outbound campaign:**

**If the bot is on the app platform**, use the Engagement module to send blast campaigns. For transactional updates, it should be handled by the bot developer at the bot level.

Sending blast campaign from the engagement platform:

1. Upload the CSV in the audience
2. Create a segment based on the desired ‘tags
3. [Schedule campaign](/docs/platform_concepts/engagement/outbound/outbound-campaigns/run-campaign)

**If the bot is on the cloud platform**, to run blast campaigns:

1. Go to **Engage** > **Templates** > Select **SMS** > Create the same template that you created and got approved in the DLT portal. Ensure you add the exact details as added in the DLT portal - without any changes in the linespace, case (upper/lower case) and 
2. Add the [audience CSV](https://docs.google.com/document/d/1RCPeDiS4Hv_n0thHRpICK0kQ1RjUpzET365cEEnxpQM/edit)
3. Schedule the campaign as explained in [](/docs/platform_concepts/engagement/outbound/outbound-campaigns/run-campaign).

**for transactional 1-o-1 updates 👇**

**If the bot is on cloud platform**

1. **Go to Engagement > Templates > Select SMS > Create the same template** that you created and got approved in the DLT portal. Add the exact details as added in the DLT portal. Make sure the message content is JUST THE SAME without any changes in the linespace, case (upper/lower case) and such
2. Make use of the V2 Notification APIs and [Flow campaigns](/docs/platform_concepts/engagement/flows_campaign) as per required.

## FAQ

1. Does Service implicit, Service Explicit, Promotional, and Transactional  template support DND (Do Not Disturb) filtering?
* Service implicit: No, this template does not support DND filtering.
* Service explicit: Supports semi-DND. If a user blocks messages from a specific industry, they will not receive messages from that industry. Every 6 months, consent data needs to be uploaded; otherwise, templates may be blocked.
* Promotional: Supports DND filtering.
* Transactional: Does not support DND filtering.