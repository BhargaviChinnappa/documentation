---
sidebar_label: Segment users using events
title: Create user segments using user events
---


Segmenting users based on user property filters is a powerful technique that allows you to categorize and target specific groups of users within your system.

Event-based user segments allow you to categorize and target specific groups of users based on their interactions with events. These are dynamic segments and help you send targeted messages, offers, or content to users who have shown particular behaviors or engaged with specific events. This improves the relevance of your interactions and drives better engagement and conversions.

You can apply time period based filter for Event-based segments. This offers a powerful way to target users based on their interactions with your system over specific time periods. Here are some sample use cases for event-based segments with time:

1. **Recent Activity**: Create a segment of users who have performed a specific action (e.g., logged in, made a purchase) within the last 24 hours. Use this segment to send them timely updates, reminders, or special offers.

2. **Inactive Users**: Identify users who haven't engaged with your platform for an extended period (e.g., 30 days). Re-engage them with a targeted email campaign, encouraging them to return.

3. **Onboarding**: Segment users who signed up within the last week. Send them a series of onboarding emails or in-app messages to help them get started and maximize their usage of your platform.

4. **Event Anniversary**: Celebrate milestones with your users. Create a segment of users who have been with your platform for a year or more and offer them loyalty rewards or exclusive content.

5. **Subscription Renewal**: For subscription-based services, target users whose subscriptions are about to expire in the next 7 days. Send them renewal reminders and incentives to continue their subscriptions.

6. **Seasonal Campaigns**: Plan campaigns around specific seasons or holidays. Create segments for events such as Christmas shopping, summer vacations, or back-to-school promotions.

7. **Abandoned Carts**: Segment users who added items to their shopping carts but didn't complete the purchase within the last 48 hours. Send them cart abandonment emails with incentives to finalize their orders.

8. **Product Updates**: Target users who have interacted with specific product features or categories in the past month. Inform them about recent updates, improvements, or new features related to their interests.

9. **Feedback Requests**: After users have completed a significant action (e.g., finished a course, booked a trip), send them a survey or feedback request to gather valuable insights and reviews.

10. **Event Registrations**: Segment users who have registered for an upcoming event, such as a webinar or conference. Send them event reminders and updates leading up to the event date.

These use cases demonstrate how event-based segments with time can help you tailor your communication and engagement strategies to suit the behavior and preferences of different user groups within specific timeframes.

:::note
Segments can be created only on user or custom events.
:::

To create event-based segments:

1. Navigate to **User 360**.
2. Click **Add Segment**.
   <img src="https://i.imgur.com/4VkOMSW.png" width="40%"/>
3.  In **Segment name**, enter a unique name for the segment.
4. Click **+Add condition** > Navigate to the **Events** tab.

   <img src="https://i.imgur.com/q073Soh.png" width="70%"/>

5. Choose the event based on which you want to create the segment. Search by event name to easily find the desired event.

6. You will see the following configuration options.

   | Purpose | Options | Description
   | ------- | ------ | -----------
   | Include/Exclude | <ul><li>Occurance</li><li>Didn't occur</li></ul> | Choose **Occurence** to include users who performed the chosen event; choose **Didn't occur** to exclude users that did not perform the chosen event.
   | operator | <ul><li>is</li><li>isn't</li><li>is greater than</li><li>is less than</li></ul> | Choose the desired operator for comparison.
   | No. of times | text box | Number of times the event has occurred. For instance, users who have performed the event "Product Purchase" at least three times in the last current month.
   Duration |  <ul><li>today</li><li>yesterday</li><li>last week</li><li>this month</li><li>last month</li><li>on</li><li>after</li></ul> |  This allows you to apply time-based filters to events based on their duration to get a more specific set of users.<br/> For example: <ul><li>Today: Users who signed up on the current day (user create event). It's dynamic, so the user list refreshes daily, giving you a fresh list every day.</li><li>Yesterday: Users who purchased products from the brand the previous day. As it's dynamic, you get the list of users who performed the specific event the previous day.</li><li>Last week: Users who visited your website in the last two weeks. Whenever you refresh the list, you will see users in the last two weeks from that day.</li><li>This month: Users who signed up to the newsletter in the current month. Whenever you refresh the user list, you will see users who performed the event in the current month, regardless of the segment creation date.</li><li>Last month: Users who renewed their subscription in the previous month. When you refresh the user list, you will consistently see users from the previous month, regardless of the segment creation date.</li><li>On [date]: Users who registered for an event on May 15th.</li><li>After [date]: Users who submitted tickets after June 1st. </li></ul>

7. Click **+Add another condition** to add multiple conditions if needed. 
8. Click **Add**. The segment is created in 20 minutes.

:::note
* You cannot create a segment that uses an event-based condition and combine it with a segment based on user properties, and vice versa.
* After creating an event-based segment, it may take up to 20 minutes for it to be visible on the user interface.
:::

***

**What next?**

* Once you've created a segment, [view users in the segment](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/user_data_segments/manage_segments#view-segment-users) and know how to use the segment to [run targeted campaigns](/docs/platform_concepts/engagement/outbound/outbound-campaigns/run-campaign).
* [Edit segment condition or name](/docs/platform_concepts/engagement/cdp/user_data_segments/manage_segments#edit-user-segment) if needed. If you want to delete, check out [Delete segment](https://docs.yellow.ai/docs/platform_concepts/engagement/cdp/user_data_segments/archive-user-segment#manually-delete-user-segment).