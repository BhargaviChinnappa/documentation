---
sidebar_label : Notification API
title : Notification API
---

## 1. Introduction

Yellow.ai's Notification API lets you send business-initiated messages from the various supported channels directly from your CRM or internal Systems.

The API supports different channels (SMS, email, and WhatsApp) and makes it easier for developers to integrate it anywhere in less time.

:::note
Starting from August 1, 2023, access to Notification APIs has been shifted to an on-demand model. This means that these APIs will no longer be available by default for bots created on or after August 1, 2023.

For a more efficient approach, we strongly recommend adopting [Flow campaigns](https://docs.yellow.ai/docs/platform_concepts/engagement/flow-campaigns-intro) and User Event APIs. Rest assured, bots that were created before August 2023 can still use Notification APIs without any interruptions.
:::

**To view Notification API collections for each channel**, see

[![](https://i.imgur.com/adPhuBf.png)](https://documenter.getpostman.com/view/9982063/UzBvGPGB#6b08f300-6405-457e-aaf7-7df822e258c8)

### 1.1 Features of the Notification API

*   Single endpoint for multiple channels
*   Enable a range of API services with one-click
*   Real-time reports on the YM Platform with the basic features of the BI tool to visualize your data
*   Callback Webhook Configuration support to receive delivery updates directly on your system

### 1.2 IPs Whitelisting

Additionally, our outbound IPs given below must be whitelisted for the reports callback to flow into your system.

*   13.71.52.164
*   13.71.49.46


### 1.3 Enable Notification API

To use notification APIs, you first need to enable this 

To use the Notification API you have to enable it on the platform as explained here:

1.  Go to the **Engage** module.
2.  Navigate to **Preferences**.
3.  Click **Enable API Access**.
    
  ![](https://i.imgur.com/h40gmOZ.png)


:::note
If notification API is not enabled for the bot, you will get a `400` error (API access is not enabled).
:::

### 1.4 Send delivery status to Webhook

You can add your webhook to receive delivery status updates in real time along with the custom payload from yellow.ai.

To enable receiving delivery status updates to your webhook:

1. Go to the **Engage** module,
2. Navigate to **Preferences**.
3. Enable **Postback URL**.

   ![](https://i.imgur.com/vV8neaA.png)

3. In **Send the delivery status to (applicable only for notifications API)**, enter the Webhook URL to which the delivery updates need to be pushed. 

   To know what the sample webhook payload looks like, see [Sample webhook payload](#22-sample-webhook-payload).

:::note
Ensure that no authentication is required to push data to the Webhook URL.
:::

### 1.5 Send notification API reports

You can send reports of notifications sent through API to your preferred users. The report is sent as a CSV file for the chosen duration.

To send Notification API reports to your preferred recipients:

1. Go to the **Engage** module,
2. Navigate to **Preferences**.
3. Enable **Notification API reports**.

   ![](https://i.imgur.com/tcwOzpL.png)

4. In **Send notification API reports to**, enter the email IDs of each recipient to whom you want to send reports. Press Enter after entering each email ID.

   ![](https://i.imgur.com/dEHh91d.png)

5. In **for time period between**, set the duration (**Start date** and **End date**)for which you want to send the report.
6. To also send the report of WhatsApp notification API, enable **Whatsapp v1 Notification API**.





## 2. Notification API Details


### 2.1 Request Information

**Base URL**

`https://cloud.yellow.ai/api/engagements/notifications/v2/push?bot={botId}`

| Region Code | Region | Host |
| --- | --- | --- |
| R0 | India | `https://cloud.yellow.ai` |
| R1 | MEA | `https://r1.cloud.yellow.ai` |
| R2 | Jakarta | `https://r2.cloud.yellow.ai` |
| R3 | Singapore | `https://r3.cloud.yellow.ai` |
| R4 | USA | `https://r4.cloud.yellow.ai` |
| R5 | Europe | `https://r5.cloud.yellow.ai` |

**Headers**

| **Header** | **Description/Value** |
| --- | --- |
| `Content-Type` | application/json |
| `x-api-key` | **For** `https://app.yellow.ai` **platform**: Get the API key from the path **Configuration** > **Access Control** > **Bot API Key**. <br/>  <br/>**For** `https://cloud.yellow.ai` **platform**: Click on the **Access control** icon on top-right > Go to **API Keys** (you can see this option only if you are a bot admin). > Click +Generate API key**. [Click here for detailed help](https://docs.yellow.ai/docs/platform_concepts/Getting%20Started/api-keys). |

:::note
Only users with a Super Admin role can [create a Bot API key](https://docs.yellow.ai/docs/platform_concepts/Getting%20Started/api-keys).
:::

#### Request Query Parameter

| **Parameter** | **Data type** | **Description** |
| --- | --- | --- |
| botId* | String | Unique ID of the bot. Login to the Platform and navigate to the bot . You can find the bot ID in the URL Eg: x16387123456 |

#### Request Body Parameters

| **Parameter** | **Type** | **Required** | **Description** |
| --- | --- | --- | --- |
| `userDetails` | Object | Yes | Details of the user to be notified. E.g. Phone Number for WhatsApp. |
| `notification`  (fields: `params`) | Object | Yes | Template details |
| `media` | Object | Optional | Template Media URL, Quick Reply Payload can be passed here |
| `config` fields: (`customPayload`, `postbackUrl`) | Object (Obj, String) | Optional | Configuration details for the API.<br/> <br/>`customPayload` - Custom information will be sent back with delivery updates.  <br/><br/>`postbackUrl` - Used to receive delivery updates on the client's webhook. <br/>To receive delivery updates on the client's webhook, enable **Postback URL** in **Engage** > **Preferences** and enter the Webhook URL. See [Send delivery status to webhook](#14-send-delivery-status-to-webhook). <br/> <br/> `apiPreference`: The MM Lite API is an intelligent delivery enhancement that leverages Meta’s infrastructure to optimize the timing of message delivery. <br/>To explicitly choose MM Lite for message delivery, set the `apiPreference` to `MM_Lite` in your API request,


##### `userDetails` Object

This object contains all relevant information about the user. It needs to have at least one contactable information and any number of additional parameters. For a WhatsApp notification, the `number` field is mandatory.

``` json
  "userDetails": {
       "number": "919090909090", //mandatory for SMS, WhatsApp, Voice     //country code to be added without space // if not added default 91
       "email": "abc@xyz.com", //mandatory for email channel
       "cc": "cc@xyz.com", //applicable only for email // array of string or string
       "bcc": "bcc@xyz.com", //applicable only for email // array of string or string
   }

```

##### `notification` Object

This contains the message template details that need to be sent as a notification. `templateId` is mandatory.

``` json

{
    "notification": {
        "templateId": "template_name",
        // The name of the template as defined in the template manager. Mandatory for WhatsApp and SMS (wherever applicable).
        "params": {
            // Renderable parameters defined in the template.
            "emiValue": "15000",
            // Variable parameter names as shown in the template manager. Dynamic values can be passed,
            "balance": "79999",
            "media": [
                {
                    // Applicable for WhatsApp.
                    "title": "title",
                    // Optional for document media types.
                    "mediaLink": "https://URL.com.jpeg",
                    "quickReplies": [
                        {
                            "type": "quick_reply",
                            "value": "payload 1"
                        },
                        {
                            "type": "quick_reply",
                            "value": "payload 2"
                        }
                    ]
                }
            ],
            "quickReplies": {
                "ctaUrlParam": {
                    "buttonText": "pricing-ai-chatbot" 
                    // "buttonText" represents the text that will be displayed on the button.
                    // "pricing-ai-chatbot" represents the extension of the URL after the domain (as configured in the template.
                }
            }
        }
    }
}


```

##### `quickReplies` Object

You can use the quickReplies object in the Notification API to define dynamic Call-To-Action (CTA) buttons in your outbound campaigns. These buttons map directly to placeholder variables in your approved message templates.
Purpose of quickReplies

The `quickReplies` object lets you:

* Insert dynamic button text into predefined template variables
* Define one or more CTA buttons for a message
* Support personalization and interaction through button-based replies

**Example with One CTA Button**

If your template uses a single placeholder for a button:

```json
"quickReplies": {
  "ctaUrlParam": {
    "buttonText": "pricing-ai-chatbot"
  }
}
```

buttonText: The placeholder variable defined in the template and its value if the label (or URL segment) rendered in the message.


**Example with Multiple CTA Buttons**
If your template supports multiple placeholders, define each one separately under quickReplies:

```json
"quickReplies": {
  "button1Text": "pricingPage",
  "button2Text": "paymentPage",
  "button3Text": "featuresPage"
}
```

:::note
Each key (e.g., button1Text) should exactly match the variable name in your template. The corresponding value is what users will see on the button or what gets appended to the URL.

:::





##### `config` Object

This contains the list of available pre-configuration that will be validated before sending the messages to the user.

By default, Yellow.ai uses the value defined in the global settings. To override this behavior, include the apiPreference field under the config object in your API request.

:::note
The MM Lite API is an intelligent delivery enhancement that leverages Meta’s infrastructure to optimize the timing of message delivery.
:::

``` json
"config": {
            
        "apiPreference": "MM_Lite" //Applicable for WhatsApp marketing messages
        "customPayload": {
            "firstName": "Wasim",
            "phone": "91999999999",
            "UID" : "Got the details"
        },
       "postbackUrl": "https://webhook.url"
   }

```


---

#### MMLite preference support in Notifications API for WhatsApp

Yellow.ai supports MM Lite as a delivery preference for notifications. By default, the system uses the delivery mechanism defined in your global settings. However, you can override this at the API level using the `apiPreference` field within the `config` object.


To explicitly choose MM Lite for message delivery, set the `apiPreference` to `"MM_Lite"` in your API request, as shown in the example below:

```json
"data" {
  "userDetails": {
    "number": "9xxxxxxxxxx"
  },
  "config": {
    "apiPreference": "MM_Lite"
  },
  "notification": {
    "type": "whatsapp",
    "sender": "9180xxxxxxxx",
    "templateId": "new"
  }
}
```

> ⚠️ Note:
> MM Lite is only available for onboarded customers and is currently supported only for **Meta-approved MARKETING templates**.

---




### 2.2 Sample Webhook Payload

As soon as we receive a callback from the downstream services, we will post that data to the configured Webhook if available. Webhooks will be called with the request body.

``` json
{
  "event": {
    "status": "delivered"
  },
  "userId": "919999999999",
  "source": "whatsapp",
  "campaign": "apiNotifications",
  "templateId": "video_button1",
  "msgId": "3Yp8jdIUj8jNeoFOP1ZLT",
  "workflowId": null,
  "firstName": "Wasim",
  "phone": "91999999999",
  "UID": "Got the details"
}

```



### 2.3 Postman Collections

To access the entire Postman documentation and run collections, click the following button.

[![](https://i.imgur.com/adPhuBf.png)](https://documenter.getpostman.com/view/9982063/UzBvGPGB#6b08f300-6405-457e-aaf7-7df822e258c8)

For API details of a specific channel, click the respective channel.

1. [WhatsApp](https://documenter.getpostman.com/view/9982063/UzBvGPGB#5961e189-e9cb-40ad-8ba6-7bada77acc06)
2. [SMS](https://documenter.getpostman.com/view/9982063/UzBvGPGB#c5013846-87a9-4062-9c1a-055eb7806f38)
3. [Email](https://documenter.getpostman.com/view/9982063/UzBvGPGB#5fea5e39-8168-4c9e-977c-fc667dfba0e2)
4. [Bulk messaging API](https://documenter.getpostman.com/view/9982063/UzBvGPGB#6b08f300-6405-457e-aaf7-7df822e258c8)

:::note
When you raise any support ticket, include `msgId` or `traceId` in the request.
:::

### 2.4 Response Codes

On successful queueing of the notification, you will receive a 202 status code with the relevant `msgId`. This confirms that the message details have been received by us and will be queued for sending on the relevant channel. The downstream service will pick the queue and will start sending it and updating the delivery status on the webhook, and the reports under Data Explorer on the platform.

#### HTTP Response Codes



| Status code | Description                                                                                                                              |
|------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 200         | Indicates general success of an API call.                                                                                             |
| 201        | Indicates successful resource creation.                                                                                  |
| 202 | Message queued successfully. You will receive a msgId for acknowledgement and tracking. |
| 204        | Response payload is empty.                                                                                        |
| 301        | Should be used to relocate resources. New URI should be used in the Location header of the response.                                    |
| 400 | Bad request. Request structure is not formed correctly. Please check the `message` field for more information. |
| 401 | Unauthorised or invalid access token. Please check your auth token. Only Super Admin Auth tokens are accepted for using API. |
| 403        | Unauthorized user.                                                                                             |
| 404        | Resource not found.                                                                                   |
| 405        | HTTP method not supported for the API.             |
| 406        | Must be used when the requested media type cannot be served by the API.                                                                  |
| 415        | Rquest body does not contain content type.                                                              |
| 422 | Invalid inputs. The request structure is evaluated to be correct but the parameter values are not within the expected range. Channel not configured. |
| 429 | Rate limited. Occurs when there are too many requests sent to the API within a short time. Once a rate limit error is captured, the rate of the API call should be decreased to honour the limits.  *Default Rate Limit is 2000 requests/min per Bot.* |
| 500 | Internal server error. TraceId will be sent back for tracking. |
| 503        | Downstream service is temporarily unavailable. Please try again later.                    |


#### API Error Codes


| Error Code    | Description  |
|---------------|--------------|
| 100 - Parameter is invalid |  One or more parameters are invalid. Please check the error message to learn more about how to fix it.
| 190 - Access token has expired | [Generate a new access token](https://developers.facebook.com/docs/whatsapp/cloud-api/get-started#get-access-token)
| 1004 - mediaUploadError  | Failed to upload media to WhatsApp (wa tier - cloud-api/onprem)  |
| 1400 - authException | If no sub-code is present, the login status or access token has expired, been revoked, or is otherwise invalid. Get a new access token. If a sub-code is present, see the subcode. (wa tier - cloud-api/onprem) |
| 1401 - apiUnknown | Possibly a temporary issue due to downtime. Wait and retry the operation. If it occurs again, check that you are requesting an existing API. See Authentication and Authorization Errors for debugging information. (wa tier - cloud-api/onprem)    |
| 1402 - apiService  |  Temporary issue due to downtime. Wait and retry the operation. See Troubleshooting, Error 2 for debugging information. (wa tier - cloud-api/onprem)  |
| 1403 - apiMethod  | Capability or permissions issue. Make sure your app has the necessary capability or permissions to make this call. (wa tier - cloud-api/onprem)  |
| 1404 - apiTooManyCalls | Temporary issue due to throttling. Wait and retry the operation, or examine your API request volume. (WA tier - cloud-api/onprem) |
| 1405 - apiPermissionDenied | Permission is either not granted or has been removed. Handle the missing permissions. (WA tier - cloud-api/onprem) |
| 1406 - parameterIsInvalid | One or more parameters are invalid (wa tier - cloud-api/onprem)      |
| 1406 - invalidUser  | The recipient WhatsApp number is invalid / The user doesn't have a WhatsApp Account (wa tier - cloud-api/onprem) |
| 1407 - accessTokenExpired  | Get a new access token. (WA tier - cloud-api/onprem)  |
| 1408 - contactsError  | Client-side rate limit has been hit. Unable to deliver message. Reasons can include: <br/>The recipient phone number is not a WhatsApp phone number. <ol><li>Recipient has not accepted our new Terms of Service and Privacy Policy.</li><li> Recipient using an old WhatsApp version; must use the following WhatsApp version or greater: <br/> * - Android: 2.21.15.15<br/> *  - SMBA: 2.21.15.15 <br/> * - iOS: 2.21.170.4 <br/> * - SMBI: 2.21.170.4  <br/> *  - KaiOS: 2.2130.10 <br/> * - Web: 2.2132.6 </li> <li>The message was not delivered to create a high quality user experience. See [Per-User Marketing Template Message](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates/#per-user-marketing-template-message-limits)</li></ol>
| 1409 - phoneNumberNotAllowed | You are not allowed to onboard this phone number in Cloud API, please contact us for more information (wa tier - cloud-api/onprem)  |
| 1410 - temporaryBlockForPolicyViolations | The WhatsApp Business Account associated with the app has been restricted or disabled for violating a platform policy (wa tier - cloud-api/onprem).    |
| 1411 - duplicatePost | Duplicate posts cannot be published consecutively. Change the content of the post and try again. (wa tier - cloud-api/onprem)     |
| 1412 - platformRateLimit  | You hit platform rate limits, please refer to the Rate Limit section for more information. (wa tier - cloud-api/onprem)  |
| 1413 - Media download error  | Message failed to send because there were one or more errors related to your payment method.<br/>- Payment account is not attached to a WhatsApp Account.<br/>- Credit line is over the limit.<br/>- Credit line (Payment account) not set or active.<br/>- WhatsApp Business Account is deleted.<br/>- Account has been suspended by us.<br/>- Timezone not set.<br/>- Currency not set.<br/>- MessagingFor request (On Behalf Of (OBO)) is pending or declined.<br/>- Check your payment setup in WhatsApp Manager and try again. (wa tier - cloud-api/onprem)                       |
| 1414 - paymentIssues  | There is some issue with the payment method of the Account. Please check on WhatsApp Business Manager.
| 1415 - Message expired | Message failed to send during its Time To Live (TTL) duration. | 
| 1416 - Rate limit error | Message failed to send because there were too many messages sent from this phone number in a short period of time. Please resend the failed messages.
| 1417 - Unsigned certificate | Message failed to send because there was an error related to your certificate. Please contact support to investigate.
| 1418 - Reengagement message | Message failed to send because more than 24 hours have passed since the customer last replied to this number. Use a message template to respond.
| 1419 - Messaging limit reached | Failed due to WhatsApp 24-Hour Limit restrictions. Please check the [link](https://developers.facebook.com/docs/whatsapp/api/rate-limits#messaging) to know more about the restrictions.
| 1420 - Generic error | WhatsApp was unable to send the message. Please try again.
| 1421 - Unsupported message type | Message type is not supported. Please use the right message type.
| 1422 - Message too long | Message length exceeds the limit of 4096 characters. Please shorten the message and try again.
| 1423 - Invalid recipient type | - | 
| 1424 - Access denied | Number is already registered on WhatsApp. See [Migrating a Phone Number](https://developers.facebook.com/docs/whatsapp/cloud-api/get-started/migrate-existing-whatsapp-number-to-a-business-account) for information on moving a phone number from WhatsApp to the WhatsApp Business API.
| 1425 - Resource not found | File or resource is not found.
| 1426 -  Parameter is missing | Required parameter is missing.
| 1427 - parameterTypeError | The value entered for a parameter is of the wrong type or there is another problem.
| 1428 - badUser | You will receive this message when you send a message to yourself. To resolve this, please send the message to a number that is not your own.
| 1429 - parameterMissing | Number of parameters passed does not match the expected number of variable parameters.
| 1432 - parameterTypeError | The format of the parameter does not match with the format in the created template.
| 1443 - Template error | Template name does not exist in the translation or would have been paused from Meta’s end.
| 1444 - System overloaded	| WhatsApp cloud API system is overloaded.
| 1500 - messageExpired | The message failed to send due to some issue with the WhatsApp Business Account. It may be down or disconnected for more than 1 day.
| 1501 - ttlLimitReached | The message failed to send during its Time To Live (TTL) duration. Please resend the message.
| 1503 - userPartOfExperiment | Failed to send message because this user's phone number is part of an [experiment](https://developers.facebook.com/docs/whatsapp/on-premises/guides/experiments). |
| 1504 - waCompatibility | There could be any of the following reasons: <ul><li>Unable to deliver message due to software/device compatibility.</li><li> The recipient's phone number is not a WhatsApp phone number.</li><li> Recipient has not accepted our new Terms of Service and Privacy Policy.</li><li> Recipients using an old WhatsApp version; must use the following WhatsApp version or greater: <br/> * - Android: 2.21.15.15<br/> *  - SMBA: 2.21.15.15 <br/> * - iOS: 2.21.170.4 <br/> * - SMBI: 2.21.170.4  <br/> *  - KaiOS: 2.2130.10 <br/> * - Web: 2.2132.6</li></ul> For more details, refer to the [Meta doc](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)
| 1520 - WA Tier - Cloud-API-Webhook | The WhatsApp message was not delivered by Meta to ensure compliance and maintain a healthy messaging environment. <br/>It is due to a limit, avoid immediately resending the template message, as it may result in another error. Instead, retry sending the message at progressively longer intervals until it is successfully delivered. For more details, see refer to the [Meta doc for the Error Code 131049](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits) |
| 14271 - invalidParameter | One or more parameters are invalid. (WA tier - cloud-api/onprem).   |
| 14272 - Invalid user | The recipient WhatsApp number is invalid, or the user doesn't have a WhatsApp account. |


:::note
When using Notification APIs, you may encounter the following error message if a WhatsApp template receives a low rating.

```json
{ 
    success: false, 
    message: "Template:<template-name> has reached low quality and cannot be used"
}
```

:::

---

## 4. Reports

You can view data regarding the campaigns you execute through the **Insights** module.

1.  Within **Insights**, select the **Data Explorer** tab on the left.
2.  In the **Data Explorer** section, select **Notification Reports** under **Default Datasets.**
3.  To begin experimenting with **Campaign Reports**, you can select **Filters**, and use filters such as **BOTID**, **CAMPAIGNID**, and **TEMPLATEID** individually, or in different combinations to pull data.
4.  Once you have generated a data set that you find useful, click on **Summarise**. With this, you can group and summarise this data set in different ways.
   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/notification.png)

    | **Field**               | **Description**                                                            |
    | ----------------------- | -------------------------------------------------------------------------- |
    | `name`                  | Name of the campaign.                                                      |
    | `campaignId`            | Unique identifier for the campaign.                                        |
    | `reportId`              | Unique identifier for this report entry.                                   |
    | `senderId`              | Identifier of the number or channel used to send the message.              |
    | `userId`                | Internal identifier for the user or recipient.                             |
    | `sessionId`             | Identifier for the messaging session to which this message belongs.        |
    | `cdpUserId`             | Identifier for the user in User 360.               |
    | `templateId`            | Identifier of the WhatsApp message template used.                          |
    | `messageId`             | Unique ID generated for the message sent to the user.                      |
    | `status`                | Current delivery status of the message (e.g., sent, delivered, failed).    |
    | `source`                | Channel through which the notification is sent (e.g., whatsapp, email, sms).       |
    | `sessionConversationId` | Identifier linking messages within the same conversation session.          |
    | `sessionStart`          | Timestamp indicating when the session started.                             |
    | `sessionType`           | Type of session (e.g., marketing, utility).                       |
    | `smsUnits`              | Number of SMS units consumed (if applicable).                              |
    | `scheduledAt`           | Timestamp when the message was scheduled to be sent.                       |
    | `sentAt`                | Timestamp when the message was actually sent.                              |
    | `deliveredAt`           | Timestamp when the message was delivered to the recipient.                 |
    | `readAt`                | Timestamp when the message was read by the recipient.                      |
    | `repliedAt`             | Timestamp when the recipient replied to the message.                       |
    | `reply`                 | The actual reply message content (if applicable).                          |
    | `errorMessage`          | Details of any error that occurred during delivery.                        |
    | `comments`              | Additional notes or annotations for internal reference.                    |
    | `apiPreference`         | Indicates the API used for delivery: `CLOUD`, or `MM_LITE`. |


## 5. Examples
### 5.1 Normal Text Notification
#### 1. CURL request

```json
curl --location --request POST 'https://app.yellowmessenger.com/api/engagements/notifications/v2/push?bot=BOT_ID_HERE' \
--header 'x-auth-token: TOKEN' \
--header 'Content-Type: application/json' \
--header 'Cookie: ym_xid=TOKEN' \
--data-raw '{
   "userDetails": {
       "number": "USER_PHONE_NUMBER"
   },
   "notification": {
       "type": "whatsapp",
       "sender": "SENDER_PHONE_NUMBER",
       "templateId": "TEMPLATE_ID",
       "params": {
           "1": "var1",
           "2": "www.yellow.ai"
       }
   }
}'
```

#### 2. Sample
<img src="https://i.imgur.com/YwkQ7Xr.png" alt="drawing" width="70%"/>


### 5.2 Image Notification
#### 1. CURL request
```json
curl --location --request POST 'https://app.yellowmessenger.com/api/engagements/notifications/v2/push?bot=BOT_ID_HERE' \
--header 'x-auth-token: TOKEN' \
--header 'Content-Type: application/json' \
--header 'Cookie: ym_xid=TOKEN' \
--data-raw '{
   "userDetails": {
       "number": "USER_PHONE_NUMBER"
   },
   "notification": {
       "type": "whatsapp",
       "sender": "SENDER_PHONE_NUMBER",
       "templateId": "TEMPLATE_ID",
       "params": {
       "media": {
           "mediaLink": "MEDIA_URL"
           },
           "1": "var1",
           "2": "www.yellow.ai",
           "3": "test"
}
 
   }
}'
```

### 5.3 File Notification
#### 1. CURL request
```json
curl --location --request POST 'https://app.yellowmessenger.com/api/engagements/notifications/v2/push?bot=BOT_ID_HERE' \
--header 'x-auth-token: TOKEN' \
--header 'Content-Type: application/json' \
--header 'Cookie: ym_xid=TOKEN' \
--data-raw '{
   "userDetails": {
       "number": "USER_PHONE_NUMBERs"
   },
   "notification": {
       "type": "whatsapp",
       "sender": "SENDER_PHONE_NUMBER",
       "templateId": "TEMPLATE_ID",
       "params": {
       "media": {
           "mediaLink": "MEDIA_URL"
           },
           "1": "var1",
           "2": "www.yellow.ai",
           "3": "test"
}
 
   }
}'
```

#### 2. Sample
![](https://i.imgur.com/YLbGCo7.png)

