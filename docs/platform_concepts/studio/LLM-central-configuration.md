---
title: LLM configuration
sidebar_label: LLM configuration
---

LLM (Large Language Model) configuration allows you to centrally manage LLM models and accounts for all LLM-powered features, such as the Dynamic chat node, Conversations, Agent AI, and Knowledge Base (KB).

This centralized setup allows you to use different accounts and configurations for various LLM modules based on your requirements and eliminates the need for repeated configurations.

#### Capabilities of LLM configuration

With LLM configuration, you can:

* Create, edit, switch models, and disconnect LLM accounts.
* Associate LLM accounts at the environment level:
  * Two tier environment - Develpoment and Live
  * Three tier environment - Sandbox, Staging, and Production

The Yellow account is preconfigured with **Gpt 4o mini** account and enabled across all environments by default. The Knowledge Base (KB) uses our proprietary in-house model by default, but you can switch to a different model if needed.

### Access LMM configuration

You can access the LLM configuration in two ways:

#### **From the Settings section**

   1. Go to **Settings** > **LLM configuration**.

      ![](https://cdn.yellowmessenger.com/assets/yellow-docs/LLMi.png)
    
#### **Directly from the specific LLM-powered module**

   1. Navigate to the specific LLM-Powered module (Dynamic chat node, Conversations, Agent AI, or Knowledge Base (KB)).

   2. Click the highlighted icon that you see on that page.

      <img  src="https://i.imgur.com/RKhl6Re.png"  alt="drawing"  width="100%"/>
      
       * This will redirect you to the LLM Configuration page.
    
### Manage LLM accounts

In the LLM configuration section, Super admin can create, edit, and disconnect LLM accounts, switch models across all the environments. 

#### Add LLM account

You can view the default Yellow account before adding a new account. If needed, you can create your own LLM account to manage LLM-powered features.

To add the LLM account, follow these steps:

1. Go to **Settings** > **LLM configuration**.

2. Click **Account list**.

    ![](https://i.imgur.com/baASqg2.png)

3. Click **+ Add account**.

    ![image](https://imgur.com/mdldiG4.png)

4. In **Give account name**, enter a name for your LLM account.
5. In **LLM provider**, choose your preferred LLM provider.
6. In **API key**,  get the API key and resource from GPT 3.5 or GPT 4.

      ![](https://cdn.yellowmessenger.com/assets/yellow-docs/LLMdetails.png)

7. Click **Connect**.

#### Edit LLM account

You can update the details of an existing LLM account or provider if needed. You cannot edit/delete the default Yellow account.

1. Go to **Account list** > **Add account**.

2. Navigate to the account you want to edit and click **Edit details**.

     ![](https://cdn.yellowmessenger.com/assets/yellow-docs/editdetails.png)

3. Add the required account details and click **Save**.

     <img  src="https://cdn.yellowmessenger.com/assets/yellow-docs/editllm.png"  alt="drawing"  width="80%"/>

#### Disconnect LLM account

You cannot disconnect the default Yellow account. However, you can disconnect any other account you have created. 

Before disconnecting, ensure another account is created to handle all LLM features.

1. Select an alternative account that you want the module to use.
  
2. Go to **Account list** > **+ Add account**.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/addccount.png)

3. Navigate to the account you want to disconnect, then click **Disconnect** to remove the account.

   ![](https://cdn.yellowmessenger.com/assets/yellow-docs/disllm.png)

#### Edit LLM configuration 

By default, the Yellow account details are displayed for each environment. However, you can update the existing LLM model or account as needed for each environment.

For example, you can set GPT 4.0 model in Staging environment and GPT 3.5 model in Production.

1. Navigate to the specific feature where you want to edit the configuration.

2. Expand the drop-down menu and click the **Edit** icon corresponding to the specific environment.

    ![](https://i.imgur.com/BexB0a9.png)

2. Update the **Account name** and **Model** as needed.
 
    <img  src="https://cdn.yellowmessenger.com/assets/yellow-docs/editaccountd.png"  alt="drawing"  width="80%"/>

3. Click **Save**.

## FAQ

<details>
 <summary>Is an LLM Required to Use Yellow.ai?
</summary>
 <div>
  <div> 
     No, a Large Language Model (LLM) is not required to use Yellow.ai. The platform offers a wide range of features and functionalities that work independently of LLM integration.<br/>
     However, integrating an LLM can enhance the platform’s capabilities, particularly for handling complex queries, generating dynamic responses, and improving FAQ interactions.
</div>
  <br/>
   </div>
</details>