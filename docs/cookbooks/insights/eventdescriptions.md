---
title: Descriptions of default table columns on data explorer 
sidebar_label : Default DB table descriptions 
---




## API events 

| Field        | Description   |
|--------------|---------------|
| TIMESTAMP    | The TIMESTAMP field represents time intervals in 1-minute slots within a 24-hour day. When an event occurs, its timestamp is rounded to the nearest 1-minute interval. The first occurrence creates a new row with the timestamp, and if the same event occurs again within the same 1-minute slot, the count column value for that timestamp is incremented by 1. This allows tracking the number of occurrences of the same event within each 1-minute interval. Subsequent occurrences in the same interval contribute to the count column value. For example: Suppose an event occurs at 9:46:24, its timestamp would be 9:46, creating a new row. If the same event happens at 9:46:37, the count becomes 2 for the 9:46 timestamp. Another event at 10:13:47 creates a new row with a timestamp of 10:13. The count column tracks repeated occurrences within the same 1-minute slot. |
| BID          | Business Identifier |
| CUSTOMID1    | Custom Identifier from CDP (Customer Data Platform) |
| CUSTOMID2    | Custom Identifier from CDP (Customer Data Platform) |
| EVENTINFO    | Additional Information Stored By Platform (Not for customer customization) |
| IP           | User's IP address identified by the platform |
| NAME         | Not Applicable (NA) |
| SOURCE       | Additional Information Stored By Platform (Not for customer customization) |
| STATUSCODE   | Various Status of the API response. 200 Means Success, 404 means Server-side Failure |
| UID          | Unique Identifier of User |
| LANGUAGE     | Language identified by our platform for the ongoing interaction |
| RESPONSE_TIME| Time taken (in milliseconds) by the server to respond back to the API request |
| COUNT        | Number of API Hits |

-----



## Bot events


| Events | Description |
| -------- | -------- |
|bot_loads     | Fired when a gets bot loaded on the platform    |
|datastore-bulk-upsert|Fired when Bulk insert or update operation is performed on the datastore|
|datastore-delete| Fired when a delete operation is performed on the datastore |
|datastore-failed-delete|Fired when a delete operation fails on the datastore|
|datastore-failed-dropdata| Fired when a drop data action fails on the datastore |
|datastore-failed-find|Fired when a find request is received on the datastore and the request fails|
|datastore-failed-insert|Fired when an insert operation is performed and it fails to insert into the datastore|
|datastore-failed-search|Fired when a search operation is performed on the datastore and it fails|
|datastore-failed-searchDocuments| Fired when a step of the journey is expected or a prompt is shown to the user|
|datastore-failed-update|Fired when the update operation is performed on the datastore and it fails|
|datastore-feedback| Fired when feedback is pushed into the datastore|
|datastore-find|Fired when a find operation is performed on the datastore|
|datastore-insert|Fired when an insert operation is performed on the datastore|
|datastore-search|Fired when a search operation is performed on the datastore|
|datastore-searchDocuments| Fired when a document search operation is performed on the datastore |
|datastore-update|Fired when an update operation is performed on the datastore|
|db_node_fallback|Fired when a notification is received to the mobile widget|
|email-sent|Fired when an email is sent|
|function-execution-time| Fired when a session is created based on a USER message|
|invocation|Fired when a new session is created from a user message for the WhatsApp channel|
|otp-sent|Fired when an OTP is sent|
|otp-verified|Fired when an OTP is verified|
|pdf-convert-api|Fired when a PDF convert API is being hit|
|redis-del |Fired when the delete operation is performed on the Redis memory|
|redis-get|Fired when data is fetched from the Redis memory|
|redis-set |Fired when write operation is performed on the Redis memory|
|synonyms|Fired when a synonym is detected|
|unknown-message |Fired when an unknown message is received|
|widget_loaded|Fired when a widget is loaded|

> Click [here](https://docs.yellow.ai/docs/platform_concepts/studio/events/event-hub#2-type-of-events) to learn about events. 

-----

## Chat tickets 

| Field                                     | Description   |
|-------------------------------------------|---------------|
| USER_ID                                   | Unique identifier for the user in the given channel. |
| RECENT_USER_MESSAGE_TIME  | Time of the last user message; null if not responded. |
| CONTACT_PHONE                             | Phone number of the user collected from the bot. |
| CONTACT_EMAIL                             | Email of the user collected from the bot. |
| CONTACT_NAME                              | Name of the user collected from the bot. |
| TICKET_PRIORITY                           | Priority of the ticket (default: medium). |
| TICKET_CREATION_TIME                      | Time the ticket is created. |
| SOURCE_CHANNEL                            | Channel through which the user accessed the bot. |
| TICKET_TRANSFERS                          | List of ticket reassignments to agents or groups. |
| TICKET_TYPE                               | Type of the ticket (default: live chat). |
| VOICE_CALL_FLAG                           | Indicates if video calling is enabled for this ticket. |
| AUTO_TRANSLATE_FLAG                       | Indicates if auto-translate is enabled for this ticket. |
| RECENT_AGENT_MESSAGE_TIME                 | Time of the last agent message. |
| ADMIN_ASSIGNMENT_FLAG                     | Indicates if an admin assigned this ticket to the agent. |
| REPLY_COUNT                               | Number of aggregate responses given by the agent to the end user. |
| USER_REPLY_COUNT                          | Number of aggregate responses given by the user to the agent. |
| TICKET_ID                                 | Auto-generated reference number for each incoming ticket. |
| TAGS                                      | Categorization of tickets done with configured words/phrases in inbox settings. |
| COMMENTS                                  | Additional information about the chat ticket, including inactivity, auto-translate, etc. |
| OPEN_TIME                                 | Time the ticket was opened. |
| ASSIGNMENT_TIME                           | Time the ticket was assigned. |
| RESOLUTION_TIME                           | Time the ticket was resolved. |
| GROUP_CODE                                | Category/group to which the ticket was assigned. |
| AGENT_NAME                                | Name of the assigned agent. |
| AGENT_EMAIL                               | Email of the assigned agent. |
| REOPENED_AGENT_EMAIL                      | Email of the agent who reopened the ticket. |
| RESOLUTION_DURATION_CREATE_IN_SECONDS     | Duration between resolution time and creation time (in seconds). |
| RESOLUTION_DURATION_ASSIGNED_IN_SECONDS   | Duration between resolution time and assigned time (in seconds). |
| QUEUE_WAIT_DURATION_IN_SECONDS            | Duration between assigned time and ticket creation time (in seconds). |
| FIRST_RESPONSE_DURATION_IN_SECONDS        | Duration between First Response Time (FRT) and assigned time (in seconds). |
| FIRST_RESPONSE_TIME_CREATION_IN_SECONDS   | Duration between FRT and ticket creation time (in seconds). |
| AVERAGE_RESPONSE_TIME_IN_MILLISECONDS     | Average time taken for agents to respond to each customer reply in all tickets (in milliseconds). |
| ABANDON_DURATION                         | It measures how long a customer waited for an agent before leaving the chat without being attended. <br/> ABANDON_DURATION = Time of Abandonment – Time of Chat Initiation
| AVERAGE_RESPONSE_TIME_IN_SECONDS          | Average time taken for agents to respond to each customer reply in all tickets (in seconds). |
| CHILD_BOT_ID                              | Bot ID from which this chat was raised (for unified inbox). |
| CUSTOM FIELDS                             | Individual custom fields and their values captured from this live chat. |
| TICKET_STATUS                             | Possible statuses for a chat ticket: Open, Assigned, Missed, Resolved, and Queued. |

### Status description 

| Status   | Description                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------|
| Open     | Set when an incoming live chat has no available agents, either inside or outside working hours, to handle it.                        |
| Assigned | Set when a chat is assigned to an agent after being created.                                                                             |
| Missed   | Set as the fallback for all incoming chats that cannot be assigned to agents. This may occur if the queue is not enabled, the queue is full, or offline functionality is not enabled. |
| Resolved | Set when agents close a live chat.                                                                                                      |
| Queued   | Set when agents are busy or away, or if chat concurrency per agent is full. Incoming live chats are directed to queued chats when queues are enabled.                |


-----


## Email tickets 

| Field                                  | Description                                                                                                                   |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| AGENT_EMAIL                            | Email ID of the assigned agent.                                                                                                |
| AGENT_NAME                             | Name of the assigned agent.                                                                                                   |
| AGENT_ASSIGNMENT_COUNT                 | The current ticket concurrency assigned to the agent at the time of ticket creation.                                        |
| ADMIN_ASSIGNMENT_FLAG                  | True if the admin manually assigned this ticket to an agent.                                                                  |
| ASSIGNMENT_TIME                        | The timestamp at which the ticket was assigned to the agent.                                                                   |
| AGENT_ID                               | Unique identifier for the assigned agent.                                                                                    |
| COLLABORATORS                          | List of collaborators involved in the ticket.                                                                                |
| CONTACT_FIRST_NAME                     | First name of the customer who created this ticket.                                                                          |
| CONTACT_EMAIL                          | Email of the customer who created this ticket.                                                                               |
| TICKET_CREATION_TIME                   | The timestamp when the ticket was created within the platform.                                                                |
| CUSTOM FIELDS                          | All individual custom fields and their values captured from this email ticket.                                               |
| TICKET_DUE_DATE                        | Due date of the ticket.                                                                                                       |
| FIRST_RESPONSE_TIME                    | The timestamp of the first response provided by the agent in that ticket.                                                    |
| FIRST_RESPONSE_DUE_TIME                | Due time for the first response SLA.                                                                                         |
| FIRST_RESPONSE_DURATION_ASSIGNED_IN_SECONDS | Total time duration between the ticket being assigned to an agent and the agent providing the first response.             |
| FIRST_RESPONSE_DURATION_CREATE_IN_SECONDS | Total time duration between the ticket being created in the platform and the agent providing the first response.            |
| FIRST_RESPONSE_TARGET                  | The target timestamp by which the first response must be provided according to the SLA policy.                              |
| GROUP_CODE                             | The group to which the ticket is assigned.                                                                                  |
| RECENT_AGENT_MESSAGE_TIME              | The timestamp of the last agent message in that ticket.                                                                      |
| RECENT_BOT_MESSAGE_TIME                | The timestamp of the last bot message in that ticket.                                                                        |
| RECENT_REOPEN_TIME                     | The last timestamp when the ticket was reopened.                                                                            |
| RECENT_USER_MESSAGE_TIME               | The timestamp of the last user message in that ticket.                                                                      |
| MANUAL_ASSIGNMENT_FLAG                 | True if the ticket was manually assigned to an agent.                                                                        |
| PARENT_FLAG                            | True if other tickets are merged into this ticket (parent).                                                                  |
| PARENT_TICKET_ID                       | Ticket ID of the parent ticket to which this ticket is merged.                                                               |
| TICKET_PRIORITY                        | The priority of the ticket, set during its creation or changed by the agent (High, Medium, or Low).                          |
| REOPENED_FLAG                          | True if the ticket is reopened.                                                                                              |
| REOPENED_AGENT_EMAIL                   | Email ID of the agent to whom the ticket was reopened.                                                                       |
| REOPENED_BY                            | The agents name who reopened the ticket.                                                                                         |
| REOPEN_COUNT                           | Count of times the ticket is reopened.                                                                                      |
| REPLY_COUNT                            | Count of exchanges between the customer and the agent.                                                                       |
| RESOLUTION_DUE_TIME                    | Due time for ticket resolution.                                                                                              |
| RESOLUTION_DURATION_ASSIGNED_IN_SECONDS| Total time duration between the ticket being assigned to an agent and the ticket getting resolved.                         |
| RESOLUTION_DURATION_CREATE_IN_SECONDS  | Total time duration between the ticket being created in the platform and the ticket getting resolved.                       |
| RESOLUTION_TARGET                      | Whether the resolution SLA was achieved or breached.                                                                         |
| RESOLUTION_TIME                        | The timestamp when the ticket was marked resolved by the agent.                                                              |
| RESPONDED_FLAG                         | Indicates whether the agent has responded to the ticket.                                                                     |
| TICKET_STATUS                          | Status of the email ticket (Opened, In-progress, On-hold, Resolved, or Pending).                                             |
| TICKET_SUBJECT                         | The subject mentioned in the email ticket.                                                                                   |
| TAG_NAME                               | All the tags applied to this particular ticket.                                                                              |
| TICKET_ID                              | Auto-generated reference number for each incoming ticket.                                                                    |
| TRANSFERRED_FLAG                       | True if the ticket has been transferred at least once.                                                                       |
| USER_ID                                | Unique identifier for the user in the given channel.                                                                         |
| USER_REPLY_COUNT                       | Number of times the user has replied in the ticket.                                                                          |

-----


## Inbox call records 

| Field                     | Description                                                                                                                                   |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| BOT_ID                    | Bot ID associated with the configured inbox for handling calls.                                                                               |
| USER_ID                   | Unique identifier for the user in the given channel.                                                                                          |
| TICKET_ID                 | Auto-generated reference number for each incoming ticket related to the voice call.                                                           |
| CALL_DURATION             | Duration between the call pickup time and call end time.                                                                                      |
| CALL_SID                  | Unique identifier for the voice call.                                                                                                        |
| CALL_PICKUP_TIME          | Time at which the call is picked up by the agent.                                                                                             |
| CALL_END_TIME             | Time at which the call is ended, either by the agent, user, or due to an error.                                                               |
| CALL_WRAPUP_TIME          | Time at which the ticket status transitions to wrap-up after the call ends.                                                                   |
| CALL_WRAPUP_DURATION      | Duration between the ticket resolved time and ticket wrap-up time.                                                                            |
| CALL_RECORDING_URL        | URL link to the call recording (audio) between the agent and the customer.                                                                    |
| CALL_QUEUE_START_TIME     | Queued time of the ticket or call.                                                                                                          |
| CALL_QUEUE_WAIT_TIME      | Duration between the first time the ticket is queued and the pickup time.                                                                     |
| CALL_ASSIGNED_TIME        | Time at which the ticket is assigned to an agent.                                                                                            |
| CALL_CSAT_AGENT_SCORE     | The default Customer Satisfaction (CSAT) feedback received for the agent after the voice call.                                                |
| CALL_CSAT_TICKET_SCORE    | The default CSAT feedback received for the overall ticket after the voice call.                                                              |
| TIMESTAMP                 | Created time of this voice call on the inbox.                                                                                                |
| QUEUE_DROP_OFF_TYPE       | Indicates whether the user dropped off from the queue and the reason for the drop-off.                                                        |
| QUEUE_DROP_OFF_TIME       | Time at which the user dropped off from the queue.                                                                                           |
| REQUEUE_COUNT             | Number of times the call or ticket was requeued.                                                                                             |
| DISCONNECTED_BY           | Indicates which peer (agent or user) hung up the call.                                                                                        |

----

## Inbox events 

| Field      | Description                                                  |
|------------|--------------------------------------------------------------|
| TIMESTAMP  | The date and time when the event was triggered.              |
| AGENTID    | Unique Identifier (UID) for agents, used for internal purposes.|
| BID        | Business Identifier - a distinctive identifier for the business involved.|
| CATEGORY   | The name or code of the group to which the raised Inbox ticket belongs.|
| SOURCE     | The communication channel through which the user is engaging with the bot (e.g., Whatsapp, Facebook, Yellow Messenger).|
| UID        | User Identifier - a unique identifier assigned to each user for tracking and distinction.|
| EVENT      | Indicates the status of the event, such as assigned, missed, open, queued, reassigned, resolved, or answered.|

### Events description 

| Event Name   | Description                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| assigned     | Triggered when a chat is assigned to an agent for resolution.                                                |
| missed       | Triggered when a chat transitions into the "Missed" status.                                                   |
| open         | Triggered when a chat enters the "Open" status due to the absence of available agents.                        |
| queued       | Triggered when a chat is placed in a queue, typically due to agent unavailability or full chat concurrency. |
| reassigned   | Triggered when a chat is reassigned from one agent to another.                                                |
| resolved     | Triggered when an agent clicks "Resolve" to mark the chat as resolved or the chat is auto-closed.              |
| answered     | Triggered when the agent has responded to the ticket at least once.                                           |


-----


## Knowledge base report


| Field             | Description                                                   |
|-------------------|---------------------------------------------------------------|
| TIMESTAMP         | Time at which the query was made to the Language Model (LLM)  |
| ORIGINAL_QUERY    | Message typed out by the user  (Input)                                |
| CONV_HISTORY      | Previous user and bot messages before the user's message      |
| REPHRASED_QUERY   | True query considering context from conversational history   |
| DOCUMENT_TAGS     | Document tag values, if any, passed                            |
| WAS_SUMMARY_GIVEN | True or false value stating if the response was summarized    |
| ANSWER            | Copy of the answer provided by the bot to the asked query     |
| LINKS             | Copy of the web links provided by the bot                      |
| SITE_KEY          | Website domain based on which the answer was retrieved        |
| UID               | Unique user ID of the user having the conversation             |
| TRACE_ID          | Unique ID of the query for further analysis on search          |


-----

## Knowledge base articles 

| Field           | Description                                                                                                     |
|-----------------|-----------------------------------------------------------------------------------------------------------------|
| ARTICLE_ID      | Identity number assigned to the article during its creation.                                                      |
| ARTICLE_TITLE   | Title of the published article.                                                                                 |
| VISIBILITY      | Visibility status selected during article creation, either Internal or External.                                |
| SUBCATEGORY     | The immediate folder or subcategory under which the article is organized.                                       |
| PARENT_CATEGORY | The name of the top-level category under which the article is classified.                                       |
| VIEWS           | The number of views received by this particular article.                                                         |
| LIKES           | The number of likes received on this particular article.                                                          |
| DISLIKES        | The number of dislikes received on this particular article.                                                       |
| LANGUAGE        | The language selected during article creation; the article is visible on the website in this specified language. |
| PUBLISHED_AT    | The timestamp indicating when the article was published.                                                          |

------

## Message events 

| Field                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIMESTAMP            | The TIMESTAMP field represents time intervals in 1-minute slots within a 24-hour day. When an event occurs, its timestamp is rounded to the nearest 1-minute interval. The first occurrence creates a new row with the timestamp, and if the same event occurs again within the same 1-minute slot, the count column value for that timestamp is incremented by 1. This allows tracking the number of occurrences of the same event within each 1-minute interval. Subsequent occurrences in the same interval contribute to the count column value. For example: Suppose an event occurs at 9:46:24, its timestamp would be 9:46, creating a new row. If the same event happens at 9:46:37, the count becomes 2 for the 9:46 timestamp. Another event at 10:13:47 creates a new row with a timestamp of 10:13. The count column tracks repeated occurrences within the same 1-minute slot. Ex: 00:00:00 UTC. |
| CITY                 | User's city retrieved from the IP address. String data type.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| COUNTRY              | User's country retrieved from the IP address. String data type.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| DEVICE               | User's device type, such as Desktop, Tablet, or Mobile. String data type.                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| IP                   | User's IP address. Integer data type.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| MESSAGETYPE          | Type of the message sender, e.g., BOT, USER, AGENT, NOTIFICATION.                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PLATFORM             | User's device operating system, e.g., Windows, Linux, etc. String data type.                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| REGION               | User's state retrieved from the IP address. String value.                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| SOURCE               | Channel in which the user is chatting with the bot. Example: Whatsapp, Facebook, yellowmessenger.                                                                                                                                                                                                                                                                                                                                                                                                                     |
| UID                  | Unique Identifier of the User.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| SESSIONID            | Unique Identifier per session.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| SESSION_SUM          | Seconds since the last message. The time is stored in seconds from the previous User/Bot/Agent message.                                                                                                                                                                                                                                                                                                                                                                                                              |
| CUSTOMID1            | Custom Identifier from Customer Data Platform (CDP).                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| CUSTOMID2            | Custom Identifier from Customer Data Platform (CDP).                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| UTM_CAMPAIGN         | Associated with the campaign's name from the Engage module.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| UTM_MEDIUM           | Associated with the campaign's medium from the Engage module.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| UTM_SOURCE           | Associated with the campaign's source from the Engage module.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| LANGUAGE             | Language identified by our platform during the ongoing interaction.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| BID                  | Business Identifier.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| INTERACTIONTYPE      | User input classification, e.g., user chose a quick reply or typed the input.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| COUNT                | Rolled-up value of that event where data was exactly the same, just a difference in time. Associated with timestamp description.                                                                                                                                                                                                                                                                                                                                                                                        |
| identificationStatus | Denotes if a user message was identified/unidentified.                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| lastMessageType      | Denotes if the last message in the chat was from the Bot/User/Agent.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |


------

## Notifications report 

| Field       | Description                                                                    |
|-------------|--------------------------------------------------------------------------------|
| NAME        | Name of the campaign                                                            |
| CAMPAIGNID  | Unique ID assigned to the campaign.                                              |
| REPORTID    | Unique ID assigned to the campaign report.                                       |
| SENDERID    | Alphanumeric or numeric string that identifies the sender of a message         |
| USERID      | Unique ID for each User present in the User360 Table                             |
| CDPUSERID   | Unique ID of the user (in User360) to whom the campaign was sent                |
| TEMPLATEID  | Unique ID of the template used in the campaign                                   |
| MESSAGEID   | Unique ID assigned to the message within the campaign sent to the user.         |
| STATUS      |                                                                                  |
| SOURCE      | Channel through which the campaign message was sent. Example: Whatsapp, Facebook, yellowmessenger |
| SMSUNITS    | The number of SMS units consumed for a single message in the campaign.          |
| SCHEDULEDAT | Date and time when the campaign was scheduled to send.                          |
| SENTAT      | Date and time when the campaign was sent                                         |
| DELIVEREDAT | Date and time when the campaign was successfully delivered.                     |
| READAT      | Date and time when the recipient read the campaign message                      |
| REPLIEDAT   | Date and time when the recipient replied to the campaign                        |
| REPLY       | Content of the reply received from the recipient                                 |
| ERRORMESSAGE| Any error message generated during the campaign delivery process.               |

<!--

## Platform user events

| Events | Description |
| -------- | -------- |
|unidentified-utterance|Fired when a user message is not understood by the Bot|
|agent-transfer|Fired when a chat conversation is transferred to a live agent|
|feedback|Fired when a user gives feedback after completing the chat|
|first-message|Fired when a new profile of a user is created|
|first-message-bid|Fired when a user profile is updated with the bid for the first time|
|home-button-click|Fired when a user clicks on the home button in the chat widget|
|journey-started|Fired when a journey starts for the user|
|journey-completed|Fired when a journey gets completed for the user|
|journey-switched|Fired when a journey is switched by NLP System for the user due to an utterance matching another journey|
|step-expected|Fired when a step of the journey is expected / prompt is shown to the user|
|step-recorded|Fired when input is given by the user for a step (step value is recorded) of a journey|
|user-visited|Fired when a user is visiting the chat widget for the first time (chatting for the first time)|
|user-revisited|Fired when a user is revisiting the chat widget (chatting again)|
|optin|Fired when a WhatsApp opt-in is added|
|optout|Fired when a WhatsApp opt-out is added|
|otp-sent|Fired when an OTP is sent from the bot using the platform function|
|otp-verified|Fired when an OTP verified from the bot using platform function|
|notification-received|Fired when notification received to the mobile widget|
|new-session|Fired when a new session is created|
|user-session|Fired when a session is created based on a user message|
|user-initiated|Fired when a new session is created from a user message for the WhatsApp channel|
|business-initiated|Fired when a new session is created by notification from the business side for the WhatsApp channel|

-->

-------

## User engagement events

Following are the fields tracked on the user engagement events table: 

| Field            | Description                                                                                                          |
|------------------|----------------------------------------------------------------------------------------------------------------------|
| TIMESTAMP        | The TIMESTAMP field represents time intervals in 30-minute slots within a 24-hour day. When an event occurs, its timestamp is rounded to the nearest 30-minute interval. The first occurrence creates a new row with the timestamp, and if the same event occurs again within the same 30-minute slot, the count column value for that timestamp is incremented by 1. This allows tracking the number of occurrences of the same event within each 30-minute interval. Subsequent occurrences in the same interval contribute to the count column value. For example: Suppose an event occurs at 9:46, its timestamp would be 9:30, creating a new row. If the same event happens at 9:59, the count becomes 2 for the 9:30 timestamp. Another event at 10:13 creates a new row with a timestamp of 10:00. The count column tracks repeated occurrences within the same 30-minute slot. |
| BID              | Business Identifier, a unique identifier for the business associated with the event.                                  |
| CATEGORY         | An umbrella term for journeys; certain journeys can be grouped under this category.                                    |
| CITY             | Approximate city location identified by the platform.                                                                  |
| COUNTRY          | Approximate country location identified by the platform.                                                               |
| CUSTOMID1        | Custom Identifier from Customer Data Platform (CDP).                                                                   |
| CUSTOMID2        | Custom Identifier from Customer Data Platform (CDP).                                                                   |
| DEVICE           | Approximate user device value identified by the platform, such as mobile or desktop.                                   |
| EVENT            | The specific event that occurred.                                                                                     |
| EVENTINFO        | Additional information stored by the platform (not for customer customization).                                       |
| JOURNEY          | The flow name under which this event was generated.                                                                    |
| PLATFORM         | Approximate underlying platform of the user device (e.g., Desktop can have Windows, Linux).                            |
| STEP             | Step name in the Automation flow under which this event was generated.                                                     |
| REGION           | Geographical location (state) identified where the bot is being used.                                        |
| SOURCE           | Different channel integration from where the user triggered the event, such as Yellowmessenger, WhatsApp, etc.        |
| TARGETINFO       | Used for storing additional information for some events, such as journey switched.                                     |
| UID              | Unique Identifier of the User.                                                                                        |
| SESSIONID        | Unique Identifier of the User for a 24-hour timeframe from the first event triggered by the user.                     |
| LANGUAGE         | Language identified by the platform during the ongoing interaction.                                                    |
| INTERACTIONTYPE  | User input classification, for example, whether the user chose a quick reply or typed the input.                       |
| COUNT            | Rolled-up value of the event where the data was exactly the same, with differences only in time (this is associated with the timestamp description). |
| VALUE            | The VALUE field is used for pushing a numerical value associated with an event. By default, if no specific value is provided, it is set to 0. This field allows you to convey a quantitative aspect related to the event, providing additional context or information.      |


### Events description

Following are the events tracked on the user engagement events table: 

| Event                   | Description                                                                                                         |
|-------------------------|---------------------------------------------------------------------------------------------------------------------|
| agent-session           | Fired when a live agent actively participates in a conversation. An agent session starts when the agent sends the first response to a ticket and continues for 24 hours from that point. Any additional tickets created during this 24-hour window are counted as part of the same agent session. If a ticket is closed without any agent response, no agent session is created. Therefore, the number of agent sessions will always be less than or equal to the number of tickets created. |
| agent-transfer          | Fired when a chat conversation is transferred to a live agent                                                       |
| banner-cta-clicked      | Fired when the User clicks on the link configured in the callout banner                                            |
| bot-closed              | Fired when the Bot is closed by the user (close button)                                                             |
| bot-icon-clicked        | Fired when the Bot avatar (in title bar) is clicked by the user                                                     |
| bot-icon-loaded         | Fired when the Bot avatar is displayed to the user (on load)                                                        |
| bot-loaded              | Fired when the Bot script is loaded on the website                                                                  |
| bot-opened              | This occurs when a user clicks on the chat bubble to open the bot.                                                   |
| bot-session             | Fired when a session is created based on a bot message (first message sent by the bot). It has a session time window of 24hrs for a given UID and source |
| business-initiated      | Fired when a new session is created by notification from the business side for the WhatsApp channel               |
| card-cta-clicked        | Fired when the User clicks on the link configured in the card buttons                                               |
| condition-recorded      | Fired when a condition node is executed in a flow                                                                   |
| feedback                | Fired when a user gives feedback after completing the chat                                                          |
| first-message           | Fired when a new profile of a user is created                                                                      |
| first-message-bid       | Fired when a user profile is updated with the bid for the first time                                                 |
| home-button-click       | Fired when a user clicks on the home button in the chat widget                                                       |
| invalid-response        | Fired when an invalid response other than the provided option is selected/entered by the user                      |
| journey-completed       | Fired when a journey gets completed for the user                                                                   |
| journey-started         | Fired when a journey starts for the user                                                                           |
| journey-switched        | Fired when a journey is switched by NLP System for the user due to utterance matching another journey              |
| message-hyperlink-clicked | Fired when the User clicks on the link configured in the text message                                               |
| new-session             | Fired when a new session is created                                                                               |
| notification-received   | Fired when a notification is received on the mobile widget                                                          |
| optin                   | Fired when a WhatsApp opt-in is added                                                                             |
| optout                  | Fired when a WhatsApp opt-out is added                                                                            |
| otp-sent                | Fired when an OTP sent from the bot using the platform function                                                    |
| otp-verified            | Fired when an OTP is verified from the bot using the platform function                                              |
| page-loaded             | Fired every time the client website page is loaded/reloaded where our script is running                             |
| pwa-loaded              | Fired when the PWA version of the bot script is loaded                                                             |
| pwa-opened              | Fired when the PWA bot is opened by the user                                                                       |
| step-expected           | Fired when a step of the journey is expected / prompt is shown to the user                                          |
| step-recorded           | Fired when input is given by the user for a step (step value is recorded) of a journey                               |
| unidentified-utterance  | Fired when a user message is not understood by the Bot                                                             |
| user-initiated          | Fired when a new session is created from a user message for the WhatsApp channel (this is only when user messages the business through WhatsApp channel) |
| user-revisited          | Fired when the chat widget loads for the user's IP address on subsequent visits. This event is specific to bots hosted on websites. |
| user-session            | Fired when a session is created based on a USER message.  Value gets incremented only when user sends the first message.|
| user-visited            | Fired when the chat widget loads for the user's IP address for the first time. This event is triggered once for the lifetime of the user's unique ID. It is specific to bots hosted on websites |

**Other events**:

- inbound-overlay-closebtn
- inbound-overlay-conversion
- inbound-overlay-impression
- inbound-widget-closebtn
- inbound-widget-conversion
- inbound-widget-impression

---------


## User feedback 

| Field             | Description                                                | Value Format                                      |
|-------------------|------------------------------------------------------------|--------------------------------------------------|
| BOTID             | Bot ID assigned by the platform.                            | Integer (e.g., x1657623696077)                   |
| UID               | User ID generated by the platform.                          | Integer (e.g., 1836013421788526118418800767619) |
| SESSIONID         | Session ID generated by the platform.                       | String (e.g., 65a8d2971e1a2100011a2433)          |
| SURVEYTYPE        | Type of feedback collected in the Feedback card.            | String (e.g., Star, Thumbs)                      |
| NODETYPE          | Type of node, indicating PROMPT_FEEDBACK or MESSAGE_FEEDBACK.| String                                       |
| JOURNEYNAME       | Journey/Flow name where the feedback card is configured.    | String                                          |
| JOURNEYSLUG       | Journey slug where the feedback card is configured.         | String (e.g., new-feedback-flow_ysdkao)         |
| STEPSLUG          | Step slug where the feedback card is configured.            | String (e.g., ae4c7ac271f37ccd)                 |
| SOURCE            | Channel from which the user has visited (always yellowmessenger). | String                                   |
| RATING            | Rating given by the user in the Feedback card (1 to 5).     | Integer (e.g., 1, 2, 3, 4, 5)                    |
| SCALE             | Scale in the Feedback card (2 for Thumbs, 5 for Star).      | Integer                                          |
| FEEDBACKS         | Text feedback given by the user.                            | String (e.g., ["Quick resolution"])              |
| CUSTOMTAG         | Placeholder for custom tags (Not Applicable).               | Not Applicable                                   |
| RESPONSE          | Feedback quality given by the user (Positive: 3/4/5 in star, Negative: 1/2 in star). | String                    |
| CREATEDAT         | Feedback submission date & time.                           | Date (e.g., Thu Jan 18 2024 12:56 PM)            |
| LASTBOTMESSAGE    | Last message sent by the bot before collecting feedback.   | String                                           |
| LASTUSERMESSAGE   | Last message sent by the user before collecting feedback.  | String                                           |


-----

## Video chats 

| Field                     | Description                                                                                                                   |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| TICKET_ID                 | Auto-generated reference number assigned to each incoming ticket.                                                            |
| CHILD_BOT_ID              | Bot ID of the child bot if orchestrator parent bot and unified inbox are enabled.                                             |
| AGENT_NAME                | Name of the Inbox Support Agent handling the ticket (e.g., Amudhan S).                                                        |
| AGENT_USERNAME            | Email of the Inbox Support Agent without special characters (e.g., amudhanyellowai).                                          |
| CLIENT_EMAIL              | Customer's email ID if provided.                                                                                             |
| CLIENT_NAME               | Customer's name if provided.                                                                                                |
| CALL_DURATION_IN_SECONDS  | Duration of the video call in seconds (difference between start and end time).                                               |
| START_TIME                | Timestamp indicating the start time of the video call.                                                                      |
| END_TIME                  | Timestamp indicating the end time of the video call.                                                                        |
| MEETING_ID                | Unique identifier assigned to each meeting.                                                                                 |
| MEETING_NAME              | Internal string for meeting identification (e.g., `${ticket.botId}_${ticket.ticketId}_${ticket.assignedTo}_${ticket.uid}`).   |
| MEETING_END_REASON        | Reason for the completion of the meeting, typically when all the participants leave.                                               |
| DID_AGENT_JOIN            | Indicates whether the agent joined the call.                                                                                |
| DID_CLIENT_JOIN           | Indicates whether the user joined the call.                                                                                 |
| WHO_HUNG_UP               | Specifies who initiated the call hang-up.                                                                                  |
| RECORDING_ID              | Identifier number assigned to each recording.                                                                              |
| RECORDING_STATUS          | Processing status of the recording (e.g., pending, completed).                                                             |


## Analytics (Custom table)

Analytics table can be found under custom tables in which the following data is captured. 

| Fields                   | Description  |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------|
| CHATURL                  | Link to Chat Transcript: e.g. https://app.yellow.ai/public/messages/a9c9844ad89bb7aeb6a3918ad57623c37616acfc6c094e3b529ad0a763323f9e687450946280f5eca561274bdc0d6360510eff61eb0b24d55cb5c1e7092c/660a37f54a1f6800016fd072 |
| TIMESTAMP                | Date and Time when event was triggered: Sun Mar 31 2024 11:28 PM                                                          |
| AEVENT                   | Event triggered upon an action. This includes both OOB, and custom events configured in the bot: e.g. welcome_message, kb_question_not_answered, booking_done |
| MESSAGEID                | Unique ID set in backend for each message: e.g. 123456789                                                                  |
| PROFILE_PLATFORM         | Platform through which user accessed the chatbot: e.g. Web, SDK                                                           |
| PROFILE_BROWSER          | Browser through which user accessed the chatbot: e.g. Safari, Chrome, Mozilla                                            |
| PROFILE_CITY             | City of user accessed the chatbot (fetched from IP address): e.g. San Francisco, New York City                             |
| PROFILE_COUNTRY          | Country of user that accessed the chatbot (fetched from IP address): e.g. India, Abu Dhabi                                 |
| PROFILE_COUNTRY_CODE     | Country code of user that accessed the chatbot (fetched from IP address): e.g. US, CA, IN                                   |
| PROFILE_DEVICE           | Type of device from which the user accessed the chatbot: e.g. Mobile, Desktop, Tablet                                     |
| PROFILE_IP               | IP address of the user: e.g. 192.168.1.1                                                                                  |
| PROFILE_LATITUDE         | Latitude value of user's location: e.g. 39.73915                                                                          |
| PROFILE_LONGITUDE        | Longitude value of user's location: e.g. -104.9847                                                                        |
| PROFILE_NAME             | (User) Profile name set up in backend. This will be random values so that user privacy is maintained: e.g. John Doe, Jane Smith |
| PROFILE_OS               | Operating system through which user accessed the chatbot: e.g. Windows 10.0, macOS 10.15.7                                 |
| PROFILE_PAGEURL          | URL of the page from which the user accessed the chatbot. e.g. https://yellow.ai                                    |
| PROFILE_DEVICETYPE       | Type of device from which the user accessed the chatbot: e.g. Microsoft Windows, Apple Mac                                |
| PROFILE_REGION           | Region of user that accessed the chatbot (fetched from IP address): e.g. California, Florida                               |
| PROFILE_SOURCE           | Device, OS, and Browser details of the user: e.g. Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/123.0.0.0 Safari/537.36 |
| PROFILE_TIMEZONE         | Timezone of user's location: e.g. -04:00, +05:30                                                                         |
| PROFILE_USERAGENT_BROWSER | Browser used by the agent to whom the user is connected to: e.g. Safari, Chrome, Mozilla                                  |
| PROFILE_USERAGENT_DEVICE | Device used by the agent to whom the user is connected to: e.g. Mobile, Desktop, Tablet                                   |
| PROFILE_USERAGENT_OS     | OS of the device used by the agent to whom the user is connected to: e.g. Windows 10.0, macOS 10.15.7                      |
| PROFILE_USERAGENT_PLATFORM | Platform used by the agent to whom the user is connected to: e.g. Web, SDK                                                |
| PROFILE_USERAGENT_SOURCE | Device, OS, and Browser details of the agent to whom the user is connected to: e.g. Microsoft Windows, Apple macOS       |
| PROFILE_WIDGETVERSION    | Version of the chat widget accessed by the user: e.g. V1, V2                                                             |
| SOURCE                   | Channel in which the user is chatting with the bot: e.g. Whatsapp, Facebook, yellowmessenger                              |
| UID                      | Unique Identifier of User: e.g. 10182708542979041342360504723                                                             |
| VALUE                    |                                                                                                                           |
| MESSAGEID                |                                                                                                                           |
| PROFILE_END_IP           |                                                                                                                           |
| PROFILE_START_IP         |                                                                                                                           |
| PROFILE_TITLE            |                                                                                                                           |
| PROFILE_UTM_CAMPAIGN     |                                                                                                                           |
| PROFILE_UTM_MEDIUM       |                                                                                                                           |


---------------

 
## Contained resolution analysis

These KPIs are tracked for data generated in the Analyze module (**Analyze > Topics**). 

| Fields                  | Description                                                                                                                                   |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Chat URL                | URL link of the conversation (transcript) between the user and bot/agent                                                                      |
| Topic                   | A conversation topic is the primary subject or query the user seeks assistance or information about |
| Topic Description       | Summary of the topic discussed                                                                                                                |
| User Query              | Summary of the query the user asked the bot or agent |
| Resolution              | Summary of the resolution provided by the bot or agent from the conversation                                                             |
| Contained               | Indicates if the chat was solely handled by the bot or transferred to an agent. If True, the query was handled/contained by the bot. If False, both bot and agent handled the query |
| Analysis Type           | This value states whether the conversation that was analyzed was between user & bot, or user & agent |
| Automation              | Indicates if the resolution can be added to the bot's knowledge base and if it can be automated. For user-bot conversations, the value is empty. For user-agent conversations, it can be either True or False |
| Automation Reason       | Reason provided by the model for marking automation as True or False |
| Resolution Status       | Indicates whether the user’s query was successfully addressed by the bot/agent (Possible values: Resolved or Unresolved) |
| Resolution Status Reasoning       | Reason provided by the model for generation of resolution status |
| User Sentiment          | Overall sentiment of the user (Possible values: Positive/Negative/Neutral)                 |
| User Sentiment Reasoning         | Reason provided by the model for generating user sentiment value|
| User ID                 | Unique ID for each user |
| Session ID              | Session ID generated by the platform for each session     |
| Source                  | Channel where the conversation happened (e.g., WhatsApp, Facebook, yellowmessenger, etc.)                                                                      |
| Conversation Start Time | Time at which the conversation started                                                                                                        |
| Conversation End Time   | Time at which the conversation ended                                                                                                          |
| Timestamp               | The date and time when the report was generated and added to data explorer |

:::note

Use Conversation Start Time & Conversation End Time  as the primary reference for when the conversation occurred, as the analysis report is generated after the session ends and may not be on the same day.

:::








-----------

## LLM usage metrics

| **Field**          | **Description**                                      | **Value**            |
|--------------------|------------------------------------------------------|----------------------|
| TIMESTAMP          | Time                                                |             Datetime         |
| SENDER             | Sender ID/UID of the user                            | String               |
| SESSION_ID         | Session ID of the user                               | String               |
| TRACE_ID           | Trace ID of the message                              | String               |
| SOURCE             | Source of the message (YM/WhatsApp/etc.)             | String               |
| SUCCESS            | Whether the API call returned a response or not      | Boolean              |
| PROVIDER           | LLM Service Provider (Open AI, Azure Open AI, etc.)  | String               |
| MODEL              | Name of the model                                    | String               |
| RESOURCE           | Name of the resource (only in the case of Azure Open AI) | String          |
| EXECUTION_TIME     | Time taken by the LLM API call                       | Milliseconds         |
| PROMPT_TOKENS      | Number of tokens in the input prompt                 | Number               |
| COMPLETION_TOKENS  | Number of tokens in the generated response           | Number               |
| TOTAL_TOKENS       | Sum of PROMPT_TOKENS and COMPLETION_TOKENS           | Number               |
| CUSTOM_LLM_KEY     | True if the client is using their own credentials; otherwise False | Boolean   |
| WORKFLOW           | Workflow ID of the flow where the node is present    | String               |
| NODE_ID            | Node ID of the node                                  | String               |


------

## WhatsApp consumption

| **Field**                             | **Description**                                                                                                                                                               |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIMESTAMP                             | The day the count is calculated                                                                                                                                    |
| WABA_ID                               | Unique WhatsApp Business Account ID provided by Meta                                                                                          |
| PHONE_NUMBER                          | WhatsApp business phone number linked to the customer                                                                                                                      |
| BUSINESS_INITIATED_AUTHENTICATION     | Conversations for authenticating users with one-time passcodes, such as account verification, recovery, or integrity challenges |
| BUSINESS_INITIATED_MARKETING          | Conversations for marketing purposes like new product announcements, targeted promotions, or cart abandonment reminders |
| BUSINESS_INITIATED_UTILITY            | Conversations for follow-ups on user actions or requests, such as order updates, account alerts, or feedback surveys |
| USER_INITIATED_SERVICE                | Conversations for resolving customer inquiries                                                                                                                     |
| CONVERSATION                          | 24-hour message threads between you and your customers, opened and charged when your messages are delivered |




<!--

| **Field**          | **Description**                                                                                                                                       |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIMESTAMP       | The date the message activity was recorded.                                                                                                          |
| WABA_ID          | The unique WhatsApp Business Account ID associated with your Meta account.                                                                           |
| PHONE_NUMBER     | The WhatsApp-enabled business phone number used for sending messages.                                                                                |
| MESSAGE_TYPE     | Type of message sent. Supported values include: <br/>• Marketing <br/>• Marketing Lite <br/>• Utility <br/>• Authentication <br/>• Authentication International <br/>• Customer Service <br/>• Entry Point |
| MESSAGE_CATEGORY | Indicates whether the message is billable (`Paid`) or non-billable (`Free`).                                                                         |

-->

---------

## Call Details Report (CDR)

If you are using voice bots, you can schedule reports to be sent to your email. This report includes metrics like the number of distinct calls attended by the bot and the total billing duration for the selected timestamp. 

Learn about CDR in detail [here](https://docs.yellow.ai/docs/cookbooks/voice-as-channel/reporting/cdr). 

-------


:::info
Time is mentioned in milliseconds.
:::


