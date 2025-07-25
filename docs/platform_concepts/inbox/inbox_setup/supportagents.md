---
title: Add Inbox admin/Inbox agent/Inbox group supervisor 
sidebar_label : Add inbox support agents
---

In this article, you will learn how to accept/add inbox roles. 


:::note
- **Admin** (of the AI Agent) can give access to **Inbox Admin/Agent** to any user (or themselves).     
- Users with **Inbox Admin** access can add **Inbox Agents** (these agents can become **Suprevisors** of a particular group).
- Any user provided with **Inbox Agents** invite can join as a inbox agent. 
- Users with only **Inbox Admin/Agent** roles can access only **Inbox module** on the yellow.ai platform.
:::



-----


- There are two major roles to access the inbox module, **Inbox Admin** and **Inbox Agent**. **Inbox Supervisor** role can be provided to an inbox agent based on the industry requirement. 
- Incoming live chats and email tickets (from the customers) are assigned only to the **Inbox agents** (support agents).
- **Inbox agents** will have access to their **chats/tickets/analytics/performance** to help understand and resolve queries in Inbox.
- Other modules in the yellow.ai platform such as **Automation**, **Channels**, etc. will not be visible to the **Inbox Admin/Agent**.
- If you have **Admin** access(to the AI Agent), you can give yourself the **Inbox Agent/Inbox Admin** access to explore the Inbox functionalities. From settings, click **Access control** > **Edit** your row to add **Inbox agent** access along with **Inbox admin** access.

![image](https://imgur.com/qdviCKa.png)


> Supporting document to add/accept AI Agent access for different roles: [Access control](https://docs.yellow.ai/docs/platform_concepts/get_started/add-bot-collaborators).




------

## <a name="provideaccess"></a> 1. Provide inbox agent/admin/supervisor access


To add an inbox role, follow the below steps: 

1. Open **Settings** > **Access Control** from the overview page. 

![image](https://imgur.com/7oBCZXR.png)

2. On **Users** tab, click **+Invite users**.
3. Enter **Email ID** of the use you want to invite. From the **Access control** dropdown menu select the required role (**Inbox (Agent)**/ **Inbox (Admin)**). Click **Invite**. 
    
    ![image](https://imgur.com/Xi7y0iZ.png)

:::note

- Email tickets are assigned only to an **Inbox agent** (although **Inbox admin** will have the permission to see and contribute to  the [operations](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox_setup/roleaccess) in Inbox).
    - For an inbox admin, all the chats/tickets will be accessible.  
    - For an inbox agent, only the chats/tickets assigned to them will be accessible.

- Each **Role** will have different permissions to use Inbox features, you can select a suitable role based on the access you want/want to provide. click [here](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox_setup/roleaccess) to know more. 
:::
 

#### Add Inbox supervisor to groups

4. **Supervisor** role can be added for agents.
    - You can make your agents supervisors to a group where they can monitor & supervise the group's incoming chats as well as the agents.
    - When you share **Inbox agent** access, you will get an additional option to make them the supervisor for a respective group.
    - From the dropdown, select the **Group** that you want them to be a supervisor. 
    > Click [here](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/team/groups) to configure a Group.   

       
    <img src="https://i.imgur.com/RNsGTzx.png" alt="drawing" width="50%"/>    




5. You can open the **Invites tab** and **Resend/Revoke** the invite. 

    ![image](https://imgur.com/I6QXFiT.png)

6. Once the agent accepts the request, their information will be listed in the **Users tab**. 
7. You can **Edit** or **Delete** the users from the **User tab** (if required).

------



## <a name="acceptaccess"></a> 2. Accept invite to join as a Inbox admin/agent/supervisor

To join the inbox team, follow the steps below:

1. If you don't have an account on [Yellow.ai Platform](https://cloud.yellow.ai), you will receive an email from Yellow.ai to Sign Up on the platform and accept the invite to join the platform as a support agent once the admin has provided you the access.

    ![](https://i.imgur.com/T1kacbw.png)


2. If you already have an account on the Yellow.ai platform, check the notification icon on the overview page. 

    ![image](https://imgur.com/6xnvUTl.png)


3. Click on the tick mark to accept the invite.

    <img src="https://imgur.com/z0ZmIx4.png" alt="drawing" width="50%"/>  



:::note
If the user has access to the agent role, they will log out after 8 hours of inactivity from the last time the `session?refresh=true` API is called for the user.
:::


------

## <a name="login"></a> 3. Managing multiple logins for agents

In a dynamic customer support environment, agents often need to access their accounts from multiple devices or sessions. To facilitate this, the **Allow multiple logins using the same agent credentials** option can be enabled under **Settings > Inbox > Multiple logins - security**.

Enabling this feature allows you to log in to the platform using the same credentials across different browsers or devices. This improves productivity, ensures continuity, and provides flexibility for agents working across various platforms.

If you do not want to use your credentials on another system or environment, you can disable this option. Disabling it helps enhance security by preventing unauthorized access and reducing the risk of credential misuse in different environments.

![image](https://imgur.com/xEIiRYv.png)
