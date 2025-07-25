---
title: Chat transcript security with IP whitelisting
sidebar_label : IP whitelisting (chat transcript)
---

IP whitelisting is a security practice that involves creating a list of approved IP addresses or ranges that are allowed to access a particular network, system, application, or service. This approach helps enhance security by restricting access only to authorized entities to chat transcripts. 

This feature is available on the app and cloud platform. 

:::note
- Only **Super admins(owners)** can access this option.
- Currently, only IPV4 addresses are supported for whitelisting.
- We rely on Cloudflare (CF) to protect our internal IP address. As a result, the public-facing IP address is provided by Cloudflare. For additional information, you can refer to [cloudflare’s official IP ranges](https://www.cloudflare.com/en-in/ips/).
:::

Chat transcripts are vital records of interactions between users and AI-agent, whether they are [conversation logs](https://docs.yellow.ai/docs/platform_concepts/analyze/chat-logs) or [chats with agents](https://docs.yellow.ai/docs/platform_concepts/inbox/inbox-settings/workflows/chattranscript). By enabling IP whitelisting, the platform allows access to the conversations only from specified IP addresses.

Chat transcript visibility for different permissions:            
- **Users with AI-agent Access**: If the user already has access to the AI-agent, they can seamlessly view the chat transcript links without the need to whitelist their IP address. However, users must have an active session (logged into the platform) to access the chat transcript links. If not logged in, they will be prompted to log in before viewing the links.                   
- **Users without AI-agent Access**: Users who do not have access to the AI-agent can access the chat transcript links only by whitelisting their IP address.                      
    ![](https://imgur.com/WwmmYyn.png)                       
- **Users without AI-agent access and without whitelisted IP addresses**: The chat transcript link will not be accessible.                       
    ![](https://imgur.com/c6T900o.png)                      


------

## Enable IP whitelisting on cloud 

To enable IP whitelisting on the cloud platform, follow these steps:

1. Log in to the platform. Open settings. Search and select **IP whitelisting**. 
2. Click on the toggle button to enable IP whitelisting. This which will reveal an option to add IP addresses.
3. Click **+Add IP Range** to include the IP address range. After adding the IP range, it will be displayed on the dashboard. You can **edit/delete** these details. 

**Demo**: 
   
   ![](https://imgur.com/CkQrHTU.gif)


---

## Enable IP whitelisting on app

You can enable IP whitelisting from the security settings on the app platform. Follow these steps:

1. Navigate to **Configuration**.
2. Click on the **Security** tab located at the top of the page.

**![](https://lh3.googleusercontent.com/9YDa7L8_bAYG6gV0qUhk6c9c1WQukW1Ijr3OA5Yl9Zxm06_ghYeaAgZMDXLy-SN-uy0dpC5CE8x6zrBaoOgWkE1_GLB1ReHSN_n-dpF7vnc_4AHoXOm4IEeln3t81Vmsq2RWsoQ4uNB3yhJAIo3i6OU)**

3. Enable the **IP Whitelisting** by clicking the toggle button.

**![](https://lh4.googleusercontent.com/9MP2TNgB2vh36HWlhrdUKKMZa2BZcIV1GF5lhsoESB8Hxuh9B7UqjegKhiSGjXa9OEEZyoZukvI2oxrpd1NjAEETFhgjfwEKf1m_7eG-bRnLBUAgHahBE1my9VyXy10L8cRFQwI22lsev-2NkrP7FLs)**

4. To add IP addresses, click **Add IP Range**.

**![](https://lh5.googleusercontent.com/4hf7_bb-Nt7eoY5_zSHF64JyCXmK_VGNG6I6H-3whjrXkS8tgP7ycFF_yAvuhFfAYBb92qWb0K6SEdiq3arPu1rd5oUWttpTFvbtwbPzs2mstILK3BE-j8zx-lEQyYYDD8KBWMrf0hX4Rmudj7tbpjg)**

After adding the IP range, it will be displayed on the dashboard.

**![](https://lh6.googleusercontent.com/oEkxbpjkai3lVHnu00neRQGVowdXovE8ENIOR5P_EqkQnezCtiQpNfpDUAoc0GBRjRImBl6tA30UEADJTYr6PRK603Kcc0tqe-tQx5anJYIkdwmNt4n_yLmgR4mb_BmuYZpws1vLmGcpSzp3q7ZYOnA)**

> If you wish to whitelist only one IP address, add the same IP address in both the **Start IP Range** and **End IP Range** fields.


-------


:::note

If you wish to whitelist only one IP address, add the same IP address in both the **Start IP Range** and **End IP Range** fields.

:::

