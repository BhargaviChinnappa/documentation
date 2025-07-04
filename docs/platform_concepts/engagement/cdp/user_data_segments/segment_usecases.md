---
sidebar_label:  Segment use cases
title: Segment your user base according to different use cases
---

The segments you create should align with your specific use case. Here are some ideas to help you get started.


## Campaign specific use cases
You may frequently need to target users on specific dates or after a certain number of days from a particular date. In the following example, we will demonstrate how to create a date-based segment to accomplish such use cases.





### Use case


 ### Schedule recurring campaign based on User 360 Table updates

Schedule a recurring campaign that targets user records which have been updated in the User 360 table within the last 24 hours.


To implement the use case, follow these steps:

* In the segment filter, choose the user property property `createdAt` and set condition as in the **last 1 day(s) ** as shown in the following.

<img src="https://i.imgur.com/mUTWcrH.png"/>


### Segment based on user created date

Creating segments based on the created date can be useful in various use cases. You can use the user property `createdAt` to define your condition.

Here are a few real-time examples of user segment based on the created date:

* Onboarding Campaign: You can create a segment of customers who were recently created or onboarded within a specific time frame.
* Re-engagement Campaign: Identify customers who haven't engaged with your business for a certain period since their creation. 
* VIP Customers: Segment customers based on the date they became your customers and their purchase history.
* Churn Prevention: Monitor customers who are nearing their anniversary or renewal date. 
* Feedback Surveys: Create segments of customers who recently became your customers to gather feedback on their initial experience.

To create segment based on user added date:

1. In Segment filters, select the user property `createdAt`.

   <img src="https://i.imgur.com/JskEsA0.png"/>
2. Choose the desired operator and select the date-time accordingly.

* **Is**: Create segments with customers whose record is created on a specific date such as "Created At Is 15 June, 2023".
* **Is after**: Create segments with customers whose record is created after a specific date, such as "Created At Is Before 15 June, 2023".
* **Is before**: Create segments with customers whose record is created before a specific date, such as "Created At Was Exactly 2 days ago".
* **Was exactly**: Create segments with customers whose record was created just before a specific number of days, hours or minutes, such as "Created At was Exactly after 12 hours before".
* **Will be exactly**: Create segments with customers whose record will be created exactly after a specific number of days, hours or minutes, such as "Created At Will Be Exactly after 1 day".



### Exclude users who opted out from campaigns

You might often want to exclude users who have opted out from all your campaigns. 

Exclude users who have opted out from all your campaigns. To achieve this:

   * Ensure that your opt-in data is up to date. This can be regularly updated through  [conversational data](/docs/platform_concepts/engagement/cdp/user_data/conv_in_builder), [CSV imports](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/user_data/import_users), [REST APIs](/docs/platform_concepts/engagement/cdp/enriching_user_profiles/send_user_data_event_rest_api)  to sync with your CRM.
   * Next, include a condition in your segment [segment](/docs/platform_concepts/engagement/cdp/user_data_segments/segments_overview)  where, "Opt-in is true”. This segment will exclude all users for whom the opt-in status is false or unknown.


  <center> <img src="https://i.imgur.com/xr4X98S.png" width="70%"/></center>

### Send discount vouchers to new users


The `createdAt` date can be useful for understanding how long users have been with your product or service. For example, you could segment users into the following groups:

* **New users**: Users who have been with your product or service for less than 30 days.
* **Active users**: Users who have been with your product or service for more than 30 days and have logged in in the past 30 days.
* **Inactive users**: Users who have been with your product or service for more than 30 days but have not logged in in the past 30 days.

Create a segment with users who have been with your product or service for less than 30 days.


<center><img src="/img/cdp/createdAt.png" width="70%"/></center>



## Highly targeted segments

### Segment with multiple conditions

Segments are powerful tools for filtering users based on multiple conditions. Each condition set contains individual conditions, consisting of a user property, an operator, and a value. By combining condition sets and conditions, you can create precise segments for targeted messaging.

* **User property**: This is the specific property or attribute of the user that you want to use as a condition.
* **Operator**: The operator defines the relationship or comparison between the user property and the value.
* **Value**: The value represents the specific value or range that the user property is compared to.

:::info
Some operators might not have an associated value field. For example, `firstName is known`. <center><img src="https://i.imgur.com/3RvuVfX.png" width="50%"/></center>
:::

Click + sign to evaluate multiple values in a condition. For example, Country is India or United States. **This is applicable only for `is` and `isn't` operator**.

   <center><img src="https://i.imgur.com/bxJDJ6s.png" width="70%"/></center>


To evaluate multiple conditions,  click **+ Add condition**. These conditions are connected with the "AND" operator, meaning users will be added only if all conditions are true.

 <center><img src="https://i.imgur.com/PqeiHR7.png" width="70%"/></center>


### Create segment specific workflows

In bot conversations, you may want to display specific information to different sets of users. For example, when discussing pricing plans, you might want to show different plans based on the user's country. 


You can use the [Condition Node](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes#1-if--condition) to achieve this.

<center><img src="https://i.imgur.com/h75l167.png" width="70%"/></center>


### Customers nearing subscription expiry

 You can send personalized reminders customers to renew their subscriptions. For this, you can create a segment based on the filter "Subscription end date will be exactly 6 days later." This segment will include customers whose subscription expiration date is approaching within the next 6 days.



<center><img src="https://i.imgur.com/7dCmuHU.png" width="80%"/></center>

### Employees in a certain department 


Send training-related communications to junior employees in specific departments. Your filters for this segment might be: **Department is "Product" or "Engineering" AND Title includes "Junior" or "Associate"**.

<center><img src="https://i.imgur.com/xUR6Ve7.png" width="80%"/></center>

### Visitors who have opted in to receiving updates on email 

Create a segment of users who have opted to receive regular product updates via email. This segment will include users who have subscribed to updates and newsletters. To set up this segment, **use the filter "Email Subscription is true"**.


<center><img src="https://i.imgur.com/xUR6Ve7.png" width="80%"/></center>

### Potential leads

Create a segment of users who have visited your pricing page more than twice. This will allow you to reach out to them with offers or set up demos with your sales team.

<center><img src="https://i.imgur.com/9NYYn0L.png" width="80%"/></center>


