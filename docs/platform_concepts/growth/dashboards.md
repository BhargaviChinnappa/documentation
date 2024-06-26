---
title: Insights Dashboard
sidebar_label: Dashboards
---

Dashboards are useful for organizing and analyzing data based on common themes. For example, if your company has three different types of products and you want to check the analytics for each product separately but in the same place, you can create dashboards for each product and add relevant metrics to each dashboard. This allows you to view all the connected values under one view.

You can have multiple dashboards, and each dashboard can contain multiple widgets.


:::note
Actions in Dashboard must be configured separately for **Live and Production** environment.
:::



## Default dashboard

In Insights > Dashboard, you can see the default dashboards created by yellow.ai for common business scenarios. Yellow.ai curates these dashboards, and they cannot be modified.

To view the Dashboards page, on the left navigation bar, click  **Insights** > **Dashboards**. 


#### Filter data by date range

To filter data by duration, navigate to **Insights** > **Dashboard** and use the Date filter to select your preferred date range. This date range selection will apply to all the reports of the dashboard.


   ![](https://i.imgur.com/NztrxaE.png)
   
In addition to the default filter, each dashboard offers various other filters. Refer to the respective section for more details on these additional filters.


:::note
You can duplicate a dashboard by clicking the **Duplicate** button, allowing you to save the default dashboard as a custom dashboard with new changes and name.
:::

### Inbox chats

The Inbox Chats report offers a comprehensive overview of ticket management and activity within the system. It includes detailed metrics such as Ticket Status Split by Day, providing insights into the daily evolution of ticket statuses. 

The Ticket Status Split section offers a snapshot of the distribution of ticket statuses across all tickets. Users can also monitor real-time ticket activity with Active Open Tickets in the Last Hour. Open Tickets by Day provides a trend analysis of open tickets over time, while Tickets Created by Day offers insights into ticket creation patterns. 

Additionally, the report includes the Deflection Rate, measuring the effectiveness of self-service options in resolving customer issues without agent assistance.


   <img src="https://i.imgur.com/QZjlUeo.png"/>


**KPI Descriptions for Inbox Chat Report**

| KPI                           | Description                                                                                          |
|-------------------------------|------------------------------------------------------------------------------------------------------|
| **Ticket Status Split by Day**       | Displays the status of support tickets on a daily basis. It helps in monitoring the progress and resolution of tickets over time, identifying trends, and managing workload. |
| **Ticket Status Split**       | Categorizes tickets based on their current status (e.g., open, in-progress, closed). It provides a snapshot of the overall status distribution of tickets, aiding in resource allocation and prioritization. |
| **Active Open Tickets in the Last Hour** | Shows the number of tickets that are currently open and were active within the last hour. It helps in assessing the immediate workload and urgency of issues needing attention. |
| **Open Tickets by Day**       | Tracks the number of open tickets each day. It helps in understanding daily ticket volume and trends, which can inform staffing and process improvements. |
| **Tickets Created by Day**    | Displays the number of new tickets created each day. It provides insights into the volume of incoming issues and helps in forecasting support demand. |
| **Deflection Rate**           | Measures the percentage of user inquiries that are resolved by automated systems or self-service options, preventing the creation of a ticket. A higher deflection rate indicates effective use of self-service resources, reducing the load on support staff. |


#### Data Filtering options in Inbox Chat Dashboard

You can filter Inbox Agent Performance Data with two filters: date and ticket priority. 

* **Date filter**: This allows you to focus your analysis based on specific date ranges 
* **Ticket priority filter**: This allows you to customize the dashbord based on ticket priority according to urgency or importance. 




### Voice

Gain insights into interactions conducted through voice channels such as phone calls or voice assistants. Monitor call volume, average call duration, call resolution rates, and customer feedback. Understand how customers engage with your business through voice channels and identify opportunities to enhance the voice experience.

![](https://i.imgur.com/Y65DRMB.png)

#### KPI descriptions for Voice bot report

| KPI Title                               | Description                                                                                                     |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| **Call Disconnect Split by Day**        | This KPI displays the number of call disconnections on a daily basis. It helps in identifying patterns or anomalies in call disconnections over time. |
| **Call Disconnect Split**               | This KPI categorizes call disconnections into various time intervals (e.g., <1 minute, 1-3 minutes, 60-90 minutes, 90-120 minutes). It provides insights into the duration before calls are disconnected, helping to understand user behavior and potential issues. |
| **API Status Split by Day and API Name**| This KPI tracks the number of API errors by day and API name. It provides a detailed view of API performance, highlighting error counts in each region for specific APIs. |
| **API Status Split by API Name**        | This KPI provides a breakdown of API statuses for each API name, such as "agent check" and "get access token." It helps in monitoring the performance and reliability of individual APIs. |
| **Call Hangup Reason Split by Day**     | This KPI shows the reasons for call hangups on a daily basis. It helps identify trends and common reasons why calls are being terminated. |
| **Call Hangup Reason Split**            | This KPI categorizes the reasons for call hangups, providing a comprehensive view of the factors leading to call termination. It aids in diagnosing and addressing call quality issues. |
| **Call Engagement Split by Day**        | This KPI measures daily call engagement levels. It tracks user interaction with the voice bot, helping to assess user interest and engagement over time. |
| **Call Engagement Split**               | This KPI provides an overall view of call engagement, categorizing engagement levels. It helps in understanding how effectively the voice bot is engaging with users. |
| **Average Ring Duration by Day**        | This KPI calculates the average duration of the ring time before a call is answered, measured on a daily basis. It helps in evaluating the responsiveness of the system. |
| **Average Call Duration by Day**        | This KPI measures the average length of calls on a daily basis. It provides insights into the typical duration of user interactions with the voice bot, aiding in performance analysis. |

#### Filtering data in Voice dashboard

You can refine Voice Data analysis using multiple filters:

- **Date Filter**: Focus your analysis on specific date ranges.
- **Call Status**: Filter calls based on their current status, such as "Answered," "Missed," or "Voicemail".
- **Hangup Reason**: Filter calls by specific reason for call termination. Use the operator to define the reason.
- **Hangup Source**: Determine where the call hangup originated, such as "Agent," "Customer," or "System."
- **Call Direction**: Differentiate between inbound and outbound calls to analyze performance based on call direction.



### Inbox agent performance

This lets you evaluate the performance of your support agents to ensure high-quality customer service. Track metrics such as average response time, number of resolved tickets, customer satisfaction ratings, and agent activity levels. Identify top-performing agents and areas where additional training or support may be needed to improve performance.





![](https://i.imgur.com/eAxXhdy.png)


| KPI                                | Description                                                                                              |
|------------------------------------|----------------------------------------------------------------------------------------------------------|
| **Average Handling Time by Agent** | Measures the average time each agent spends handling tickets. It helps in evaluating individual agent efficiency and performance. |
| **Average Handling Time**          | Shows the overall average time taken to handle tickets. It provides a general benchmark for handling times across the team. |
| **Average Handling Time by Day**   | Displays the average handling time for tickets on a daily basis. It helps in identifying daily trends and potential issues affecting handling times. |
| **Average FRT by Agent**           | Tracks the average first response time (FRT) for each agent. It helps in assessing how quickly agents respond to new tickets. |
| **Average FRT**                    | Shows the overall average first response time for tickets. It provides a general benchmark for response times across the team. |
| **Average FRT by Day**             | Displays the average first response time for tickets on a daily basis. It helps in identifying daily trends and potential issues affecting response times. |
| **Average Chat Response Time by Agent** | Measures the average response time for chat interactions for each agent. It helps in evaluating individual agent performance in real-time communication. |
| **Average Chat Response Time**     | Shows the overall average response time for chat interactions. It provides a general benchmark for chat response times across the team. |
| **Average Chat Response Time by Day** | Displays the average response time for chat interactions on a daily basis. It helps in identifying daily trends and potential issues affecting chat response times. |
| **Average Queue Time**             | Measures the average time tickets spend in the queue before being handled. It helps in understanding delays in ticket processing. |
| **Average Queue Time by Day**      | Displays the average queue time for tickets on a daily basis. It helps in identifying daily trends and potential bottlenecks in ticket processing. |
| **Agent Transfers by Day**         | Tracks the number of ticket transfers between agents on a daily basis. It helps in understanding collaboration and potential inefficiencies in ticket routing. |

Learn more about [Chat reports](https://docs.yellow.ai/docs/platform_concepts/growth/default_reportss#based-on-chats)

#### Inbox agent performance data Filters
You can filter Inbox Agent Performance Data with two filters: date and ticket priority. 
* **Ticket priority filter**: This allows you to customize the dashbord based on ticket priority according to urgency or importance. 


## Generative AI

### Generative AI (Bot) Dashboard

The Generative AI (Bot) Dashboard provides insights into the performance of your AI-powered chatbot. It enables you to track key metrics related to knowledge base interactions and bot responses, allowing you to optimize bot performance and enhance user experience.

#### Reports:

1. **KB Questions by day:**
   This report displays the number of questions asked to the bot from the knowledge base on each day. It helps you understand the volume of interactions over time, facilitating trend analysis and resource planning.

2. **KB Questions by channel:**
   This report categorizes knowledge base questions based on the communication channel through which they were asked, such as website chat, mobile app, or social media platform. It provides insights into user engagement across different channels.

3. **KB Questions Answered:**
   This report shows the total number of knowledge base questions answered by the bot. It allows you to gauge the effectiveness of your bot in providing responses to user queries and measure user satisfaction.

4. **KB Questions Answered by Channel:**
   This report breaks down the number of knowledge base questions answered by the bot according to the communication channel. It helps you assess the performance of the bot across different channels and identify areas for improvement.



### Bot performance

This provides insights into the effectiveness and efficiency of your chatbot. Track key performance indicators such as response time, conversation completion rates, user satisfaction scores, and frequently asked questions. Identify areas for improvement and optimize your chatbot to provide better customer service and support.

   <img src="https://i.imgur.com/rXZ6dn4.png" width=""/>
            


#### KPI Descriptions for Bot Performance Report

KPI | Description
--- | -----------
**Flow Visits** | This KPI tracks the number of times users enter a specific flow within the bot. It helps measure the popularity and usage of different bot flows.
**Bot Accuracy**  | This KPI measures the accuracy of the bot in understanding and responding to user queries. High accuracy indicates effective natural language processing and a well-trained bot.
**Bot Feedback** | This KPI gathers user feedback on their interactions with the bot. It helps in assessing user satisfaction and identifying areas for improvement.
**Flow Completion Rate** | This KPI calculates the percentage of users who successfully complete a flow from start to finish. It is an indicator of how effectively the bot guides users through a process.
**Deflection Rate** | This KPI measures the percentage of user inquiries handled by the bot without needing to escalate to a human agent. A higher deflection rate indicates that the bot is effectively resolving issues.
**Utterance Status Split** | This KPI categorizes user utterances based on their status (e.g., recognized, unrecognized, ambiguous). It helps in understanding how well the bot processes different types of user input.
**API Usage by Status Code** | This KPI tracks the status codes returned by API requests made by the bot. It provides insights into the performance and reliability of the APIs used by the bot.
**API Requests by Day** | This KPI shows the number of API requests made by the bot on a daily basis. It helps in monitoring the bot's activity levels and identifying trends or spikes in API usage.


Learn more about [bot performance reports](https://docs.yellow.ai/docs/platform_concepts/growth/default_reports#based-on-bot-performance)




### User traffic 

This provides user traffic metrics such as Unique Users, New Users, User Traffic Channel, Platform/Medium, Unique Users By Country, User by Device, and Messages to understand user traffic trends.

   <img src="https://i.imgur.com/MK4YWr3.png"/>
   


> Learn more about [User Traffic dashboard](https://docs.yellow.ai/docs/platform_concepts/growth/metrics#-user-traffic).

**KPI descriptions for User Traffic report**

| KPI                             | Description                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| **Unique Users**                | Tracks the number of distinct users who visit or interact with the system. It helps in understanding the reach and audience size. |
| **New Users**                   | Measures the number of users who visit or interact with the system for the first time. It provides insights into user acquisition and growth. |
| **Average Session Duration per Day** | Displays the average length of user sessions on a daily basis. It helps in analyzing user engagement and interaction patterns over time. |
| **Average Session Duration**    | Shows the overall average length of user sessions. It provides a general benchmark for user engagement and interaction time. |
| **Sessions per User**           | Calculates the average number of sessions per user. It helps in understanding user retention and repeat visits. |
| **Messages by Day**             | Tracks the number of messages sent or received each day. It provides insights into daily user activity and engagement levels. |
| **User Traffic by Channel**     | Categorizes user traffic based on different channels (e.g., social media, email, direct). It helps in identifying the most effective channels for user acquisition. |
| **User Traffic by Platform**    | Categorizes user traffic based on different platforms (e.g., web, mobile). It helps in understanding user preferences and optimizing platform-specific strategies. |
| **Unique Users by Device**      | Measures the number of unique users categorized by device type (e.g., desktop, mobile, tablet). It helps in understanding device usage trends and optimizing for different devices. |
| **Unique Users by Country**     | Tracks the number of unique users categorized by their country. It provides insights into geographic distribution and helps in targeting specific regions. |


Learn more about [User traffic reports](https://docs.yellow.ai/docs/platform_concepts/growth/default_reports#based-on-user-traffic)

#### Filters available for User traffic dashboard

- **Channel:** Filter user traffic data based on the communication channel used, such as website, mobile app, or social media platform.
- **Device:** Filter user traffic data based on the device type used by users, including desktop, mobile, or tablet.
- **Country:** Filter user traffic data based on the geographic location of users, allowing you to analyze traffic trends by country.


### Email tickets


### Email Tickets Dashboard

The Email Tickets Dashboard provides comprehensive insights into email ticket performance and status. It allows you to monitor various metrics and track trends over time to optimize email support operations effectively.

#### Reports:

1. **Email Ticket Status split by day:** This report displays the status of email tickets over different days, allowing you to track changes in ticket statuses over time.

2. **Email Ticket Statuses:** This report provides an overview of the current status of email tickets, enabling you to quickly identify the distribution of ticket statuses.

3. **Average FRT for Email Tickets by day:** This report calculates the average First Response Time (FRT) for email tickets on each day, helping you assess the efficiency of response times over time.

4. **Average Email Ticket Handling Time by day:** This report calculates the average handling time for email tickets on each day, providing insights into the efficiency of ticket resolution processes over time.

5. **Average Email Ticket Response Time by day:** This report calculates the average response duration for email tickets on each day, allowing you to evaluate the timeliness of responses over time.

6. **Email Ticket FRT SLA Split:** This report splits email tickets based on compliance with the First Response Time (FRT) Service Level Agreement (SLA), helping you identify areas where SLAs are met or missed.

7. **Email Ticket Resolution SLA Split:** This report splits email tickets based on compliance with the Resolution Time SLA, allowing you to evaluate the effectiveness of resolution processes against SLA targets.


## Create Custom dashboards


In addition to the default dashboards, you can create custom dashboards for a more tailored view of your bot data. A custom dashboard offers a dedicated page where you can configure and display information from a linked database. Select the specific data you want to monitor and visualize it through various charts and graphs, providing a comprehensive and easily accessible overview of your bot's performance and metrics.


Here are the features of the insights dashboard:
- You can create multiple dashboards, each of which can include multiple widgets (reports).
- **Widgets** are the saved reports that are present on the [data explorer page](https://docs.yellow.ai/docs/platform_concepts/growth/dataexplorer/savedreportsactions#2-add-report-to-dashboard). The dashboard helps the analysts to add multiple widgets to the single page layout. 
- Widgets can be directly added to the Dashboard from the **data explorer**.

   ![](https://i.imgur.com/LJz5RoC.png)









You can create a dashboard using either of the following methods:


:::note
You can also duplicate the default dashboard by going to the **Default** tab and clicking **Duplicate**. You cannot modify or edit the Default Dashboard directly.
:::

### <a name="1"></a> Method 1: Create a dashboard from the dashboard page

1. On the left navigation bar, go to **Insights** > **Dashboard**.
2. Click on the **Custom** tab, then click **+ New dashboard**. 

   ![img](https://i.imgur.com/gmxIYqM.png)

3. On the Dashboard details pop-up, enter **Name** and **Description**. 
4. Click **Save**.




### <a name="2"></a>  Method 2: Create a dashboard from Data explorer (Saved reports)

> Prerequisites: [Data explorer](https://docs.yellow.ai/docs/platform_concepts/growth/dataexplorer/savedreportsactions)

1. On the left navigation bar, click **Insights** > **Data explorer**. 
2. Click and open any of the saved reports. 
    ![](https://i.imgur.com/Sy9bmBJ.png)
3. From **Actions** dropdown, select **Add to dashboard**.
4. Select **New dashboard**. Add **Name** and **Description** (the saved report that you have selected is going to be the widget inside a dashboard. You can choose to add this widget to an existing dashboard or you can create a new dashboard and add this widget to it).
5. Click **Save**. You can view this on the dashboard page. 
    ![](https://i.imgur.com/o3ila14.png)

:::note
All the changes made in the Saved reports are automatically updated on the Dashboard.
:::


### <a name="3"></a> Add new widget to the custom dashboard

You can add new widgets to the custom dashboard using the reports that were saved. To add a saved report as a widget to your dashboard, follow these steps:

:::note
To learn more about creating a saved report, refer to [custom tables](https://docs.yellow.ai/docs/platform_concepts/growth/dataexplorer/customtables).    

<!-- img  src="https://i.imgur.com/MFgmkwk.png"  width="70%"/> -->
:::



1. On the **Dashboard** page, navigate to the **Custom** tab.
2. Click **+Add widget**. You will be prompted to create a new widget.

   ![](https://imgur.com/9xatiMR.png)

3. To create a new widget, click **+ Create new widget**.
 
   <img src="https://i.imgur.com/oyDuwuQ.png" width="80%"/>

4. Select **Custom query** and choose your preferred table from the drop-down box. Click **Next** to proceed.
5. Apply filters, summarize, and visualize the data as per your need.

   ![](https://i.imgur.com/vuvy6kf.png)


------




## Manage dashboard

### Access dashboards

To view the Dashboards page, on the left navigation bar, click  **Insights** > **Dashboards**. 

### Edit dashboard

To edit a dashboard:

1. Click **Edit** dashboard at the top right corner.
2. You can change the **Name**, **Description** of the dashboard and create filters.
3. Add more widgets to the dashboard or delete existing widgets.
4. Rearrange the widgets by dragging and dropping them.
5. Click **Save** to apply the changes.

   ![](https://i.imgur.com/8tNItnb.png)

### Add filters to custom dashboards


Adding filters to custom dashboards enhances your ability to analyze and visualize data tailored to your specific needs. Filters allow you to refine your dashboard views, focusing on the most relevant information for your analysis. Follow the steps below to create filters for your custom dashboard:

1. On the **Custom** dashboard page, navigate to the dashboard where you want to add filters.
2. Click the **Edit** button to enter edit mode.

   ![Custom Dashboard](https://i.imgur.com/Vq2ujGC.png)

3. Click on the **Create filter** button. This action will display a list of all available reports within the dashboard.

4. Provide a descriptive name for your filter to easily identify its purpose in **Enter Filter Name:**.

5. For each widget where you want to apply the filter, select the relevant column using the available drop-down list. On the right side, you will see the status as mapped for each widget, confirming the column selections.

6. Click the **Create** button to finalize the filter creation process. 
7. Repeat the above steps to add more filters as needed.
8. After adding all desired filters, click **Save** to save your changes.
   Once saved, you will see all the filters for the custom dashboard displayed, as shown here.

   ![img](https://i.imgur.com/CxjQijp.png)

#### Delete custom filter

To delete a custom filter:

1. Click on the **Edit** icon.
2. Select the filter you want to remove.
3. Click on **Delete filter**.

   ![Delete Filter](https://i.imgur.com/niZ34hU.png)

### Apply filters to Custom dashboard data

You can drill-down data using the date filter and custom filters customized to meet your specific requirements.

To filter dashboard data:

1. Open the custom dashboard and locate the filter dropdown menu at the top
2. Click on the dropdown, configure your filter settings, and click **Apply** to refine your data.

   <img  src="https://i.imgur.com/BSvI4Do.png"  width=""/>




### Delete custom dashboard

If you want to delete a dashboard, click **Actions** at the top right corner of the dashboard and select **Delete**.

<!--    ![](https://hackmd.io/_uploads/H1Yyz-pt3.png) -->

   <img src="https://i.imgur.com/4BBP5oJ.png"  width="50%"/>