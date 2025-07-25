---
title : Test WhatsApp bot
sidebar_label : Test WhatsApp bot
---

You can test your bot on WhatsApp without connecting it to a WhatsApp Business Account (WABA) through Yellow.ai platform. The platform offers a dedicated testing environment where you can test and refine your bot before deployment. 

:::note
You can add up to 10 phone numbers to test your bot flow.
:::

The following table provides a list of supported and unsupported message formats for testing:

Supported message types | Unsupported message types
------------ | ------------
Text | Single/Multi Product Message
Media - image, document, video | Cart Events for SPM/MPM
WhatsApp Quick Replies | WhatsApp Pay
WhatsApp List Messages | WhatsApp template Quick Replies


To initiate testing, follow these steps:

1. Enter the testing number provided by Yellow.ai or use your personal number.
2. [Build your bot](https://docs.yellow.ai/docs/platform_concepts/get_started/createfirstbot) with the required conversational flows based on your use case.
3. Test the WA bot using either Automation or Channels module. 

    * Use the Preview section of the Automation module.
    * Use the WhatsApp messenger page in the Channels module.


##  Test Whatsapp bot using Automation module

To test WA bot from Automation module, follow these steps:

1. Navigate to **Automation** > **Build** > **Flows** and select the flow that you want to test.

     ![](https://imgur.com/CSXypXJ.png)
     
2. In the **Preview** section, select **WhatsApp** from the website drop-down.

      <img src="https://i.imgur.com/BMwV6fr.png" alt="drawing" width="80%"/>
      
3. Enter **Tester name** and **WhatsApp number**, then click **Test**. 

    <img src="https://i.imgur.com/X93DHJ1.png" alt="drawing" width="30%"/>
    
* Watch the video on how to test the WA on your device or read the instructions. 

   ![](https://i.imgur.com/akMjiEq.gif)
   
   
4. Once your number is added to test your bot, you can scan the **QR code** or **copy the link** to test your WhatsApp chatbot.

    <img src="https://i.imgur.com/ECZpafd.png" alt="drawing" width="60%"/>

5. Alternatively, a notification link is displayed on your device. Click it to open the WA app.

   <img src="https://i.imgur.com/tfySZdj.jpg" alt="drawing" width="40%"/> 
   
   * The WhatsApp app will display a generic template containing your flow's name and the steps for testing the bot.

6. Enter the pre-configured utterance to trigger the flow. 

    <img src="https://i.imgur.com/LOrpZMZ.jpg" alt="drawing" width="40%"/>  
    
### Test WhatsApp bot using Channels module

1. On the left navigation bar, click **Extensions** > **Channels** > **Messaging** > **WhatsApp messenger** > **Test bot**.

   ![](https://imgur.com/kJ0NqTE.png)
   
* Follow the steps outlined in the testing section of the [Automation module](#test-whatsapp-bot-using-studio-module).


