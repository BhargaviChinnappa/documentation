---
title : Chat widget Text formatter
sidebar_label : Text formatter
---

You can style the text on the Chat Widget as per your needs using the Markdown syntax to enhance the user experience. With the Markdown syntax, you can emphasize important information and capture the reader's attention within specific parts of the conversation.

Use the following syntax for styling the text in the bot conversation:

* **Bold**: Use asterisks to enclose text when you want to emphasize or highlight its importance. (`*text*`).
* **Strikethrough**: Achieve a strikethrough effect by enclosing the text with tildes. (`~text~`)
* **Italic**: Italicize specific words or phrases by using underscores. (`_text_`)
* **Bulleted Lis**t: Organize information in a structured manner by starting a statement with a hyphen and a space. (`- text`)
* **Highlight text**: To highlight specific text, enclose it with colons. (`:text:`)

Input | ouput
-----|-------
`*Welocme to web widget world*` | **Welcome to web widget world**
`1.(press space) This is a normal list` | 1. This is a normal list.
`-(press space) This is a bullet list` | • This is a bullet list 
`-Why is this text cut?:p~`| ~~Why is this text cut?:p~~
`_This is italic_` | *This is italic*
`Oh i'm in the <<highlight>>` |  Oh i'm in the highlight

  <img src="https://i.imgur.com/6sw5Pb0.png" alt="drawing" width="60%"/>


   
## Enable text formatting

To enable text formatting, follow these steps:

1. On the module switcher, click **Channels**.

    ![](https://i.imgur.com/UuFZ2eR.png)

2. Click on **Chat widget**.

    ![](https://i.imgur.com/1KzP77W.png)
	
3. Navigate to the **Settings** tab and enable **Text formatting**.

    ![](https://i.imgur.com/9dAwqbd.png)
    
4. Click **Save changes**.

5. Navigate to **Studio**, select the required flow, and in the respective node format the text.

     ![](https://i.imgur.com/irymScC.png)
     
6. Navigate to **Channels** > **Chat widget** > **Deploy** > **Web** > **Experience on a Website**.

     <img src="https://i.imgur.com/r3eNUCT.png" width="70%"/>
     
* You can view the formatted text in the widget.

    <img src="https://i.imgur.com/x1ENb7y.png" width="40%"/>