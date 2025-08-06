---
title: Set up inbox to handle email tickets without any code
sidebar_label : Overview
---

**No code email ticketing**

When a customer sends an email to the support team in a typical business scenario, it usually lands in the inbox of the respective email app, such as Gmail or Outlook. This process is often disorganized and difficult to streamline.     

**No code email ticketing** offers a solution to manage customer support requests or tickets through email without the need for programming. This system automatically directs incoming emails to the appropriate customer support agent or group, and utilizes an **inbox ticket section** to monitor and control the status of each ticket.

> You can enable no code email ticketing [here](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/workflows/emailticketing). 


Features offered by the tickets section: 
- The primary objective of no code email ticketing is to simplify the management of customer support requests and enhance the efficiency and effectiveness of customer service teams.
- All customer queries raised via email are compiled and listed in a unified user interface (omni-channel customer support suite).
- Admins can view all tickets sent to or received by the support email address.
- As an Agent, you will be assigned with the tickets (based on the [group](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/team/groups) or [auto-assign](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/automation/tickets-assignment-logic) settings). You can select an email that needs attention and reply to it on time. 


Once the email tickets have been set up according to the instructions provided in [configuration page](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/setupandconfig), the inbox will receive emails. From there, you can view the email support requests as tickets on the email tickets page, which can be seen in either **List view** or **Detailed view**.


:::note
Email tickets are assigned only to an **Inbox agent** (although **Inbox admin** will have the permission to see and contribute to  the [operations](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox_setup/roleaccess) in Inbox).
- For an inbox admin, all the chats/tickets will be accessible.  
- For an inbox agent, only the chats/tickets assigned to them will be accessible.
:::


**ticket-created** event ([custom event](https://docs.yellow.ai/docs/platform_concepts/studio/events/event-hub#custom-events)) gets triggered when a email ticket is created and assigned to an agent.


---------

## 1. Email tickets list view 


1. Log in to [yellow.ai](https://cloud.yellow.ai/) platform and open **Inbox** > **Tickets**.

    ![](https://i.imgur.com/W8lAIJ6.png)


2. The landing page will have a ticket list and count, Sort and filter options, manual ticket creation, SLA messages, email details (agent ID, ticket ID, subject line, ticket creation time), priority, ticket status, and assigned group/agent. 

    ![](https://i.imgur.com/JZ5SPUk.png)


:::note

An attachments icon appears on the email ticket when the last message contains any attachments
![email attachment](https://imgur.com/zVAXa2F.png)
:::


| Feature  | Description | Related links |
| -------- | -------- | -------- |
| **Tickets**      | - **My tickets**: List of tickets assigned to a particular agent. <br/> - **Collaborating tickets**: List of tickets where multiple agents have been assigned/working on a ticket. <br/> - **Unassigned tickets**: This list displays the tickets which are not yet assigned to any agent. <br/> - **Resolved tickets**: Tickets that have been resolved.|      |
| **Email details**|- Each ticket is auto-assigned with a number when created, which will be its respective **ticket ID**. <br/> - Each ticket contains the **subject** of the email under which you can find the requestor's **name** and the **created date**. <br/> - You can also see the **priority**, **status**, **agent** name, and the **group** to which the agent belongs. <br/> - You can perform **bulk actions** on these tickets. | [Ticket status](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/emailticketstatus), [Bulk actions](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/bulkaction)|
|**Sort and filter**| Last modified date is considered as the date & time when the ticket was recently modified/updated. By default, tickets are arranged based on the last modified date with their corresponding ticket ID. You can sort by **Last modified date**.|[Search and apply filters](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/searchandfilter)|
|**Manual ticket creation** |You can choose to create an email ticket manually. |[Create new tickets](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/manualticket)|


-------


## 2. Email tickets detailed view 

1. Log in to [yellow.ai](https://cloud.yellow.ai/) platform and open **Inbox** > **Tickets**.

    ![](https://i.imgur.com/W8lAIJ6.png)
2. Click on any of the ticket grids, and the detailed view of that respective ticket opens. 

    ![](https://i.imgur.com/DBidLMA.png)


### 2.1 Ticket screen elements

| Feature | Description |  Preview   |
| ---------------------- | -------------------------------------------------------------------- | --- |
| **Ticket ID & Subject**  | Ticket ID# and Subject are displayed on the top of the ticket thread |  ![](https://i.imgur.com/2ZU7m7E.png)|
|**SLA log** | Hover over SLA log to see the SLA policy applied for this ticket. Learn more [here](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/slaintro#11-view-sla-time-log).|![](https://i.imgur.com/VNgBBXf.png)|
|**Ticket status**| By selecting **Resolve ticket**, the ticket gets resolved. You can also change the ticket [statuses](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/emailticketstatus).|![](https://i.imgur.com/rKSWdnS.png)|
|**Download & share thread**|You can copy the link to the transcript or download the transcript of the email conversation in this ticket- Be mindful of the user information provided in the email thread|![](https://i.imgur.com/8kxUISP.png)|
|**Email thread**|To and from messages along with the sent/received time| ![](https://i.imgur.com/WOrxqoe.png)|

------

### 2.2 Email response screen

| Feature  | Description | Preview|
| -------- | -------- | -------- | 
|**Add template**|You can **add(change/preview/delete)** a pre built template. Learn more [here](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/productivitytools/emailtempalte). |![](https://i.imgur.com/wWwlQDS.png)|
|**Reply**| Select **Reply** from the dropdown to reply to the previous mail. To address cannot be changed.|![](https://i.imgur.com/gOFIdMc.png)|
|**Forward**|Select **Forward** from the dropdown to reply to the forward the above email thread to a new email ID.|![](https://i.imgur.com/CRyH0y9.png)|
|**Internal notes**| Select **Internal notes** from the dropdown to add internal notes that only the Inbox admin and agent to whom this ticket is transferred can see.|![](https://i.imgur.com/wgx1c9A.png)|
|**Add CC and BCC**| Click Cc/Bcc and add the mail IDs|![](https://i.imgur.com/wu1sIgu.png)|
|**Select/change email ID**|All the [emails configured](https://docs.yellow.ai/docs/platform_concepts/inbox/tickets/setupandconfig) for inbox are displayed here, you can select the email ID from which you wish to send this email.<br/> If you have received a mail on different mail ID and you send a reply using a different mail ID- the user will receive the old conversation thread in the current mail.|![](https://i.imgur.com/o46DjHM.png)|
|**Email body**|You can only send a reply when the body contains some information. To send a reply without any content, use blank spaces. <br/> You can easily copy and paste text, images, or files into the email body using keyboard controls (Ctrl + C for copy, Ctrl + V for paste) or the copy-paste option. With this you can transform information from any location to the email body interface. |![](https://i.imgur.com/ZDFEQXN.png)|

#### Formatting & action options

| **Category**        | **Icon / Label**     | **Function**                 | **Details / Description**                                                                                      |
|---------------------|----------------------|------------------------------|------------------------------------------------------------------------------------------------------------------|
| **Text Formatting** | **B**                | Bold                         | Makes selected text bold.                                                                                       |
|                     | **I**                | Italic                       | Italicizes the selected text.                                                                                   |
|                     | **U**                | Underline                    | Underlines the selected text.                                                                                   |
|                     | **S**                | Strikethrough                | Draws a line through selected text.                                                                             |
|                     | **`</>`**            | Inline Code                  | Add text between flower braces `{ }` to format as code. Can be used for a single line code.                                                        |
|                     | **¶**                | Paragraph Style              | Choose heading or normal paragraph styles.                                                                      |
|                     | **☰**                | Text Alignment               | Aligns text: left, center, or right.                                                                            |
|                     | **• / 1.**           | Bullet / Numbered List       | Organize content into bulleted or numbered lists.                                                               |
|                     | **T**                | Plain Text Block             | Insert a block of plain, unformatted text.                                                                      |
|                     | **―**                | Horizontal Ruler             | Inserts a horizontal divider line to separate sections of the email.                                            |
| **Quick Actions**   | 🤖 (Bot)              | AI assist bot               | Agent can clarify doubts or fetch information using [AI assist bot](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox_setup/agentassistbot).                                                                    |
|                     | ⚡                   | Canned responses     | Add [canned responses](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/productivitytools/canned-responses ) configured via settings. You can choose one from the dropdown while typing an email.                         |
|                     | 🧱                   | Template                     | Insert [prebuilt email templates](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/productivitytools/emailtempalte) (prebuilt & saved via settings). Clicking on this icon will open all the available templates, you can select one and update. You can also preview, change or delete template.                                                                   |
| **Insert Options**  | 📎                   | Attachment                   | Attach up to 5 files: PNG, JPG, PDF, WAV, MP3, and document formats. Each must be `<10` MB and combined attachments should be `<25` MB.                      |
|                     | 🖼️                   | Image                        | Insert image directly into email.                                                                               |
|                     | 🔗                   | Hyperlink                    | Add a clickable link.                                                                                           |
|                     | 📊                   | Table                        | Insert tables to structure data.                                                                                |
|                     | `{}`                 | Code Block                   | Insert multiline code snippets.                                                                                 |
| **Editing Tools**   | ↶                   | Undo                         | Undo the last change.                                                                                           |
|                     | ↷                   | Redo                         | Redo the last undone action.                                                                                    |
|                     | 🗑️                   | Delete                       | Delete selected content or the entire draft.                                                                    |




:::note
**Auto-save draft message**   


The draft message saving option allows the agents to save their composed messages (or private notes) automatically, ensuring that their work is preserved when switching between chats or windows, or even when accidentally closing the tab.
The ticket interface will display an indication to show that a draft has been created and these drafts will be visible only to the agent who authored it.

**Limitations**:
- **Session-based retention**: Drafts are retained only until the user session concludes. Upon session end, drafts may be cleared to maintain privacy and optimize system resources.
- **Browser compatibility**: Cross-browser compatibility is not functional in this situation. For example, when Chrome and Firefox browsers are simultaneously opened, and a cloud app is accessed on both, any draft created in one browser (e.g., Chrome) cannot be observed within the corresponding chat in the other browser (e.g., Firefox). 
- **Incognito mode**: Drafts are not compatible with incognito mode. Agents should refrain from using incognito browsing when relying on the draft feature to ensure a seamless experience.
:::


----

### 2.3 Customer contact details

| Feature  | Description | Preview|
| -------- | -------- | -------- | 
|**Contact details**| Customers name, number and email are displayed. You can view activities that are happening with this email contact by clicking the **Recent conversation**. Click **View all** to see all the details on the [Contacts tab](https://docs.yellow.ai/docs/platform_concepts/inbox/contacts#--2-send-proactive-notification-to-a-contact).|![](https://i.imgur.com/Lks0uhG.png)|

-------

### 2.4 Email ticket details

| Feature  | Description | Preview |
| -------- | -------- | -------- |
|**Email ticket details**| **Priority**: You can change the priority to low, medium, or high <br/> **Assignee**: You can assign the email conversation to a Group (which gets [auto-assign](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/automation/tickets-assignment-logic) to an agent) or you can assign this thread to an agent. Configure Email [group](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/team/groups) and [agent](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/team/agents).  <br/> **Tags**: You can tag this conversation to any of the configured [tags](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/workflows/tags).  |![](https://i.imgur.com/8q8LSvZ.png) |

------

### 2.5 Other details 

| Feature  | Description | Preview |
| -------- | -------- | -------- |
|**Ticket fields** |These are custom fields, you can configure and arrange them in [settings](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/workflows/chat_custom_fields). |![](https://i.imgur.com/d8KddGJ.png)|
|**Collaborators**| More than one agent can help to resolve a ticket (similar to a group chat). Add [collaborator](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/productivitytools/collaboration) names by selecting the names from the dropdown menu.|![](https://i.imgur.com/2pi1jhB.png)|
|**Activity log**| The activity log consists summary of all the changes/updates that have taken place on this ticket (ticket ID). For example, Change of status/priority, Transfer of ticket from one agent to another, Reopening of the ticket, Breach of SLA, etc. |![](https://i.imgur.com/3K2SyF5.png)|