---
title: Default reports 
sidebar_label : Default reports 
---

## Default reports overview

Yellow.ai offers pre-built reports with filters, summaries, and visualizations, allowing quick access to essential insights.


### Access default reports

1. Navigate to the **Insights** section.
2. Click on **Data explorer** to enter the data analysis interface.
3. Default reports are displayed at the top of the page in the Default tab. Click on the report name to open it.

![image](https://imgur.com/Jgj7gLQ.png)


### Customization options 

- **Add Filters/Summarization/Visualization**: While viewing a report, you have the flexibility to further refine it by adding filters, adjusting summarizations, or changing visualizations to suit your specific requirements.
- **Save custom reports**: If you make modifications to a default report and wish to save your changes, you must save it as a new report with a custom name. This custom report will then be accessible under saved custom reports. Click on the **Custom** tab to access these customized reports.

## List of default reports 

Here are the default reports available on the Data Explorer page, along with the applied operations (original dataset, filters, summarization and visualization applied):

### Based on user traffic

You can see it under default dashboard: **User traffic**

| Report | Description | Tables | Filter | SummarizeBy | GroupBy | Visualization |
|--------|-------------|---------|--------|------------|----------|--------------|
| Unique Users | Number of distinct users | Message Events | Message Type is User | Distinct count of UID | | Count |
| New Users | Number of new users | User Engagement Events | Event is first-message | Count| | |
| User Traffic Channel | Number of users per traffic source | Message Events | Message Type is User Source is not empty| Distinct count of UID | Source | Bar |
| Platform/Medium | Number of users per platform/medium  | Message Events | Message Type is User Platform is not empty| Distinct count of UID | Platform | Bar |
| Unique Users By Country | Number of users per country | Message Events | Message Type is User Country is not empty| Distinct count of UID       | Country |              |
| User by device | Number of users per device | Message Events | Message Type is User Device is not empty| Distinct count of UID | Device | Pie chart     |
| Messages | Number of messages | Message Events | Interaction Type is not welcome | Sum of count | | |
| Average Session duration | Average duration of user sessions | Message Events | Message Type is User | Average of session sum | | |
|**Upcoming reports** |||||
| Returning User | Number of returning users | Message Events User Engagement Events | Message Type is User Event is first-message | Distinct count of UID Count | | |
| Users per minute/hour/day/week/month | Number of users per time interval| Message Events | Message Type is User | Distinct count of UID minute/hour/day/week/month| | |
| Average Session per user | Average number of sessions per user | Message Events User Engagement Events | Message Type is User event is user-session | Distinct count of UID Count | | |
| Business initiated conversations | Number of conversations initiated by the business | | | | | |
| User initiated conversations  | Number of conversations initiated by users | | | | | |
| Referral Initiated | Number of conversations initiated by   | | | | | | 
| Messages - `User <>  Bot` | Number of messages between users and  bot | | | | | | 
| Messages - `User <> Agent` | Number of messages between users and agents | | | | | |
 

### Based on Bot performance

You can see this under **Bot performance**.


| KPI | Description |
|-----|-------------|
| Flow visits | Number of visits completed through journeys. Table: User Engagement Events. Filter: Event is journey-completed. Summarize By: Sum of count. Group By: Journey. |
| Flow completion rate | Rate of completion for initiated journeys. Table: User Engagement Events. Filter: Event is journey-started and journey-completed. Summarize By: Sum of count. Group By: Event. Visualization: Pivot. Custom Formula: `(journey-completed/journey-started)*100`. |
| Bot Accuracy | Accuracy of bot identification in messages. Table: Message Events. Filter: IDENTIFICATIONSTATUS Not empty. Summarize By: Count. Group By: IdentificationStatus. Visualization: Pivot. Custom Formula: `Identified/(Identified+Unidentified)`. |
| Deflection Rate | Rate of deflection in user-agent sessions. Table: User Engagement Events. Filter: Event is user-session and agent-session. Summarize By: Count. Group By: Event. Visualization: Pivot. Custom Formula: `(User-Agent/User)*100`. |
| Bot Feedback | Feedback provided for bot performance. Table: User Feedback Table. Summarize By: Average on rating. |
| Unidentified utterances | Number of messages with unidentified status. Table: Message Events. Filter: Identificationstatus is unidentified. |
| API usage by status code | Usage of API services categorized by status. Table: API Events. Filter: API name. Summarize By: Sum of count. Group By: Status code. |


**Upcoming reports**

Report | Description
------ | ----------
| Agent Feedback | Feedback provided for agent performance | | | | | | |
| Avg time in each flow | Average time spent in each flow of interaction | | | | | | |
| Missing bot response | Number of interactions without bot responses  | | | | | | | |
| Validator limit exceeded | Instances where validator limits were exceeded| | | | | | |
| Feedback limit exceeded  | Instances where feedback limits were exceeded | | | | | | |
| API request Rate | Rate of API requests made | API Events | API Name | Sum of count  | Day | Bar | |
| API response rate | Rate of API responses | | | | | | | 
| Step wise interactions    |The stepwise journey shows the number of interactions within each journey step and drop-off rate in a flow. To check for a drop-off step, the user can select the journey from the dropdown.| User Engagement Events  | Journey | Count | Step | | |

----

### Based on chats

Visualised under default dashboard: **Support chats**

| KPI | Description |
|-----|-------------|
| Total Chats | Total number of chat tickets. Table: Chat Tickets. Summarize By: Distinct values of ticket_id. |
| Open Chats | Number of open chat tickets. Table: Chat Tickets. Filter: ticket_status is OPEN. Summarize By: Distinct values of ticket_id. |
| Queued Chats | Number of queued chat tickets. Table: Chat Tickets. Filter: Queue wait duration greater than 0. Summarize By: Distinct values of ticket_id. |
| Assigned Chats | Number of assigned chat tickets. Table: Chat Tickets. Filter: ASSIGNMENT_TIME is previous 7 days. Summarize By: Distinct values of ticket_id. |
| Resolved Chats | Number of resolved chat tickets. Table: Chat Tickets. Filter: ticket_status is Resolved. Summarize By: Count. |
| Deflection Rate | Rate of deflection in chats. Table: User Engagement Events. Filter: event is user-session and agent-session. Summarize By: Count event. Visualization: Pivot. |
| Missed Chats | Number of missed chat tickets. Table: Chat Tickets. Filter: ticket_status is MISSED. Summarize By: Distinct values of ticket_id. |

