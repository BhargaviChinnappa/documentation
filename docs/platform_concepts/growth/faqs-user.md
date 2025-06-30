---
title: Insights FAQs
sidebar_label: Insights FAQs
---

<details>
<summary> How are sessions calculated? </summary>
<div>
A session can be a user session (when there’s user interaction with the bot) or bot session (when there’s a bot message but not necessarily any user message). A session window is of 24 hours. A user can have any number of interactions with the bot within this 24 hours window from the start of a session and it will be considered a single session. A new session starts after 24 hours.
    
</div>
</details>


<details>
<summary> What is the timestamp format displayed in reports and dashboards? </summary>
<div>

The timestamp is displayed in milliseconds.
    
</div>
</details>

<details>
<summary> What are the formats in which a report can be downloaded? </summary>
<div>

Reports that get downloaded are only available in CSV format. 
    
</div>
</details>

<details>
<summary> How to schedule reports of default table? </summary>
<div>

To schedule a default table report, follow these steps : <a href="https://docs.yellow.ai/docs/cookbooks/insights/scheduledefaultreports"> Flow completion rate </a>

</div>
</details>

<details>
<summary> Difference between a new user and a unique user? </summary>
<div>
New users are first-time visitors.
</div>
<div>
Unique users are the total number of users visiting within any time range (new + repeat users). If a user has visited before, irrespective of the timeframe, they will be considered returning users. New vs returning users are identified based on UIDs. If a UID exists in the database, the user is classified as a returning user (UID remains same for a user, unless they log in from different channel or browser).
</div>
</details>

  
  

<details>
<summary> How to check for the percentage of self-serve? </summary>
<div>
    Deflection rate under <b>Bot Performance</b> on the <b>Overview</b> page.
</div>
</details>



<details>
<summary> What is the meaning of 'switched' in the user journey visualization page? </summary>
<div>
When the user moves to a different journey at any point in time it is termed as <b>Switched</b>.
</div>
</details>


<details>
<summary> Why is my user count not matching the numbers displayed on the flow chart? </summary>
<div>
The number displayed in the flow chart is the number of hits and not the number of users.
</div>
</details>


<details>
<summary> Is <b>dropped</b> inside Steps considered as a final drop or can the user continue? </summary>
<div>
<b>Dropped</b> means the user has dropped out of the bot.
</div>
</details>


<details>
<summary> How are users tracked in the mobile app? </summary>
<div>
Closing the chat window/app or leaving the chat in the middle of the conservation for a long time implies the user has dropped off.
</div>
</details>


<details>
<summary> When can we decide if a flow (journey) is completed?</summary>
<div>
It depends on the step structure and how many steps are required to complete a flow. After all the steps are completed, the journey is completed.
    
</div>
</details>

  
<!-- <details>
<summary> How do you differentiate between Poor performance and Good performance based on the visualization insights? </summary>
<div>
Based on <a href="https://docs.yellow.ai/docs/platform_concepts/growth/funnels"> Flow completion rate </a> (in user journey visualization).
</div>
</details> -->


<!-- <details>
<summary> Why are flow completion rates low?</summary>
<div>
There can be multiple reasons for <a href="https://docs.yellow.ai/docs/platform_concepts/growth/funnels"> Flow completion rate </a> . You can find a list of them along with recommended next steps under <b>User Journeys</b> > <b>Funnels</b> > <b>Flow Summary</b>.
    
</div>
</details> -->



<details>
<summary> Can I automate(schedule) my report generation? </summary>
<div>
You can schedule any saved report on <b>Data Explorer</b> as an email alert. Open any <b>Saved report</b> > click <b>Actions</b> > <b>Schedule Reports</b> > configure all details > <b>Save</b>.  Click <a href="https://docs.yellow.ai/docs/platform_concepts/growth/dataexplorer/savedreportsactions#1-schedule-a-report"> here </a> for more details.
</div>
</details>

  
  
  
  

<details>
<summary> Why are the values not getting auto updated on the dashboard page (overview/ user journey/ metrics)? </summary>
<div>
All the Insights widget pages (<b>Overview, Metrics, User Journeys, Doc cog, Dashboards, Data explorer</b>) must be refreshed to see the updated data (pages do not get auto-refreshed).
</div>
</details>

  

<details>
<summary> How to capture analytics when the user clicks on the Home and Cross buttons? </summary>
    <div> You can find these Events in the <b>User engagement</b> > events table in <b> Data Explorer</b>. </div>
<div> <b>home-button-click</b>: When a user clicks on the home button in the chat widget. </div>
<div> <b>bot-closed</b>: When a user clicks on the cross icon of the chat widget. </div>
</details>

    
<details>
<summary>  On the Data explorer - User engagement table, the timestamps increase by 30 mins. What is the reason for that?
</summary>
<div>
On the user engagement events table, similar records are rolled up at 30 mins interval. You can refer to the Count column to check how many records are rolled up for a particular row event. The distinct count functionality uses <a href="https://en.wikipedia.org/wiki/HyperLogLog">hyperloglog</a> algorithm which gives an approximate number and not the exact count.
</div>
</details>
    
<details>
<summary> How can I <b>download chat transcripts</b> for the last year? 
</summary>
<div>
Open <b> Insights</b> > <b>Metrics</b>. You can apply 31 days custom time filter of any month before 6 months(or a year) and click <b>Export</b> and select <b>Chat transcripts</b>. 
or  from the **Data export** module. 
</div>
</details>


<details>
<summary> 
When is my raw data export sent to my email and when does it get downloaded directly?
</summary>
<div>
How a table is exported depends on the file size. If the count of records is greater or equal to 500, we do an export from backend (email). For less than 500 records, the export happens directly.
</div>
</details>


<details>
<summary> How do you identify a returning user? </summary>
<div>
If a user has visited the bot before, irrespective of the timeframe, they’ll be considered a returning user. New vs returning users are identified based on UIDs. If a UID exists already, it’s marked as returning user.
</div>
</details>


<details>
<summary> Why can't I find certain column fields in the filters? </summary>
<div>

Only the columns which are searchable will be available to be filtered. Columns can be marked as searchable while creating a custom database. 
    
</div>
</details>

<details>
<summary> What is the difference between Data Explorer > Notification Report and Data Export Notification Report? </summary>
<div>

In Data Explorer > Notification Report, only entries where the source is WhatsApp or SMS are shown. However, in Data Export Notification Report, an additional source, YellowMessenger, is also included for the same data source.

</div>
</details>


<details>
<summary>Impact of Non-Searchable Columns in Custom Tables</summary>
<div>
<p>When columns are not marked as searchable during custom table creation, several limitations arise:</p>

<ul>
<li><strong>Filter visibility:</strong> The non-searchable columns won't appear in the filter options, limiting users' ability to refine their data queries.</li>

<li><strong>Summarisation and visualization:</strong> Users cannot summarize or visualize data based on non-searchable columns.</li>

<li><strong>Dashboard creation:</strong> The absence of searchable columns impedes the creation of dashboards using the query option, as dashboards rely on searchable data for dynamic visualizations and insights.</li>
</ul>

<p>By ensuring columns are marked as searchable during creation, users can maximize the functionality and analytical capabilities of custom tables.</p>
</div>
</details>



<details>
 <summary>Why do the assigned and resolved ticket counts in DE and Inbox Analytics sometimes differ?
</summary>
 <div>
  <div> 
The chat tickets table updates each row in place, meaning that when a ticket moves from the Assigned state to the Resolved state, the same entry is updated with the new status. This decreases the count of Assigned tickets by 1 and increases the count of Resolved tickets by 1. To match the assigned ticket count in DE with the widget in Inbox Analytics, apply the Assignment_Time filter in the chat tickets table to the same time range as the widget in Inbox Analytics. This ensures a 1:1 match in ticket counts.</div>
  <br/>
   </div>
</details>


<details>
  <summary>What encryption method is used to secure data?</summary>
  <div>
    <p>
      If you have selected the option to secure PII data in default tables, RSA (Rivest–Shamir–Adleman) encryption is used for both encryption and decryption.
    </p>
  </div>
</details>


<details>
  <summary>Where are the recordings stored? Are they stored securely?</summary>
  <div>
    <p>
     Recordings are securely stored in Amazon Web Services (AWS) S3, specifically in the US region. We use Server-Side Encryption with Amazon S3 managed keys (SSE-S3) to ensure data security and compliance.
    </p>
  </div>
</details>

<details>
  <summary>How long are the recordings stored?</summary>
  <div>
    <p>
   All recordings are retained for a minimum of one year by default. Recording of a call—or specific portions of a call—can be disabled via bot configuration settings.
    </p>
  </div>
</details>

<details>
  <summary> Who has access to the stored recordings?</summary>
  <div>
    <p>
   Only authorized members with access to the bot can view or manage the stored recordings.
    </p>
  </div>
</details>



<details>
<summary> Is it possible to decrypt the database for specified users?</summary>
<div>
 Yes, decryption is possible for specified users if the data has already been masked and encrypted. Using the appropriate private key, the data can be decrypted as needed. For more details, refer to <a href="https://docs.yellow.ai/docs/platform_concepts/growth/dataexplorer/configure-data#secure-pii-data-on-default-tables"> Yellow.ai's documentation on securing PII data. </a>
</div>
</details>




<details>
<summary> If an update comes days after the interaction, will it be added to the previous session? </summary>
<div>
No, once the 24-hour session window is over, any new update — even if it's related to the previous interaction — will not be attached to the old session. Instead, it will start a brand new session.
</div>
</details>

