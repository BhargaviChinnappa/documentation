---
title: Insights and analytics on yellow.ai
sidebar_label: Introduction 
---

The Insights module on the yellow.ai platform actively monitors and tracks all data and metrics associated with your bot, offering comprehensive analytics for valuable insights.

---------


## 1. Explore insights module

The Insights module in Yellow.ai consists of the following sections: 

| Section | Description |
| -------- | -------- |
| [Visualisation](https://docs.yellow.ai/docs/platform_concepts/growth/visualisation/visualization) | Explore and analyze user journeys with ease using the visualization feature. You can visually track user flows and delve into detailed information, enhancing your understanding of user interactions. |
| [Data explorer](https://docs.yellow.ai/docs/platform_concepts/growth/dataexplorer/intro) | Utilize this powerful tool to build analytics for both default and custom tables. It enables you to delve deep into your data, perform data exploration, and generate meaningful insights. |
| [Data Export](https://docs.yellow.ai/docs/platform_concepts/growth/dataops) | Download the available system data. Export data from the Yellow.AI platform to your system storage. |
| [Custom alerts](https://docs.yellow.ai/docs/platform_concepts/growth/customalerts) | Monitor your bot's overall performance on alerts section. Set up custom alerts to receive email notifications regarding any issues, change or failures that may occur. This functionality ensures that you stay informed about the performance of your bot and can take prompt action when necessary. |
| [Dashboard](https://docs.yellow.ai/docs/platform_concepts/growth/Dashboards/dashboardintro) | Create multiple dashboards tailored to your specific requirements. The Dashboard feature allows you to visually display all your data using widgets. This makes it easier to track key metrics and gain a comprehensive understanding of your bot's performance. |

<!-- | [Overview](https://docs.yellow.ai/docs/platform_concepts/growth/overview) | This section provides an elaborate overview of the bot's functionality, highlighting nine common metrics such as user traffic, bot activity, and feedback. <br/> For insights specifically related to voice bots, you can refer to the [Voice overview](https://docs.yellow.ai/docs/platform_concepts/growth/voiceoverview) page.|
| [Metrics](https://docs.yellow.ai/docs/platform_concepts/growth/metrics) | In this section, you can access a comprehensive range of metrics pertaining to bot users and API usage for your bot. It enables you to gain valuable insights into user behavior and interaction patterns.| 
| [Doc cog](https://docs.yellow.ai/docs/platform_concepts/growth/doccog) | The Doc cog feature generates insights based on the documents uploaded within the [Automation](https://docs.yellow.ai/docs/platform_concepts/studio/overview) section. This functionality empowers you to extract valuable information and gain valuable insights from the content of your documents. |-->

----------

## 2. Manage access and permission to insights 


Features within the Insights module can be accessed if a bot user has either of these roles, **Insights analytics and Insights admins**. 

![](https://imgur.com/DyJzmIi.png)

> Click [here](https://docs.yellow.ai/docs/platform_concepts/get_started/add-bot-collaborators#1-share-bot-access) to learn how to provide **Insights analytics and Insights admins** permission to users in Yellow.ai. 


1. **Insights (Admin)**: Insights (Admin) role provides access to all available data and analytics.
2. **Insights (Analytics)**: Insights (Analytics) role provides access to standard analytics, bot health monitoring, dashboards, doc-cog and user journey. Access granted for each module to this role is as follows:

    | Modules | Access level| 
    | -------- | -------- | 
    |Overview dashboard |  :heavy_check_mark: **Only** if the bot subscription date is after (greater then) `2023-12-14T18:30:00.000Z` |
    | Metrics dashboard - User metrics  | :x: Chat transcript <br/> :x: User details report|
    | Metrics dashboard - API usage | :heavy_check_mark:|
    | User journeys | :heavy_check_mark: User journey visualization <br/> :heavy_check_mark: Funnels|
    | Data export | :x: |
    | Dashboard | :x: |
    | Data explorer | :x: |
    | Health | :heavy_check_mark: |
    | Doc cog  | :heavy_check_mark: |
    | Voice overview  | :x: |



--------

## 3. Watch insights demo 

<iframe width="660" height="415" src="https://www.youtube.com/embed/yAkP3imNl7Q" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>