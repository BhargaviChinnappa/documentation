---
title: Automation FAQs
sidebar_label: Automation FAQs
---

:::note
Welcome message is supported only for web and app SDK and it is not supported for any of the [Channels](https://docs.yellow.ai/docs/platform_concepts/channelConfiguration/overview).
:::


### Nodes

<details>
 <summary> Can I display a dynamic carousel without any actions in it?
</summary>
 <div>
  <div> Yes, you can use the <a href = "https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/message-nodes1/message-nodes"> carousel node from the message nodes </a> section.

</div>
  <br/>
   </div>
</details>

<details>
 <summary> What types of workflows enable you to connect goals that run in the background while maintaining control within the dynamic chat node?
</summary>
 <div>
  <div> All the actions that are possible via <a href = "https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/action-nodes-overview/api-node"> Action nodes</a> and <a href = "https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes"> Logic nodes</a> can be set in Dynamic chat node to fetch data or perform an action. Additionally, you can also enable <a href = "https://docs.yellow.ai/docs/platform_concepts/appConfiguration/overview"> integrations </a> and enable them in Dynamic chat node to send and recieve data from thrid-party applications.

</div>
  <br/>
   </div>
</details>

<details>
 <summary> How to display videos along with the AI-agent messages?
</summary>
 <div>
  <div> Use the <a href= "https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/message-nodes1/video-node"> Video node</a>.

</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why is the send OTP node not working?
</summary>
 <div>
  <div>Our out-of-the-box OTP verification is restricted only to the India region. If you’d like to avail of this functionality for international numbers, you will have to use external APIs.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Is it possible to skip triggering NLU for specific steps of a flow?
</summary>
 <div>
  <div>Yes, you can skip triggering NLU for specific flows using the <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/prompt-nodes#25-store-comment">Store comment</a> node.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>I have configured Hindi language but it is triggering fallback/different journey? What might be the reason?
</summary>
 <div>
  <div>In a flow, if you have selected "hi" (ISO code) for Hindi (button value), then it might be triggering another intent which you would have configured earlier ("hi" intent configured). To overcome this problem, set a variable, assign the variable value to Hindi language (hi), and then connect it to the Set language node.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>I have an API response through which I’m getting a product image as a .png (few kb in size) Can I pass that into a Carousel/Image node to dynamically change the image?
</summary>
 <div>
  <div>Yes, use the following code snippet in the API parse function.

```
return new Promise(resolve => {
        const imageVariable = 
        [{
            "options": {  
                "caption": { "type": 'random' },
            },
            "url": "insertURL"
        }]
        resolve(imageVariable);
    }); 
```
You can also do this in the carousal by [creating your own custom/dynamic object](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/prompt-nodes#dynamic-carousels) (depending on the use case for which you select the node)​

</div>
  <br/>
   </div>
</details>

<details>
 <summary>The options in a dynamic Whatsapp list always leads to the fallback flow. How can we tweak this?
</summary>

 You can use the [Condition](https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/logic-nodes#1-condition) node to redirect each option to the respective flow.
 <div>
  <div>

1. Insert the condition node in your flow.
2. Populate the node with button values.

![](https://i.imgur.com/FYETzej.png)

4. Connect each button to the flow that has to be executed if that button is clicked.

![](https://i.imgur.com/SysoleQ.png)
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Can we increase the pagination size limit in Database Node?
</summary>
 <div>
  <div>
  
  You can increase the size limit upto 25, to increase beyond that, while setting the <b>Pagination</b>, instead of <b>Text</b>, use <b>Variables</b> with a static value. <b>Variables</b> let you increase the size limit upto 200.


![](https://i.imgur.com/Dgla9UJ.png)

​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>I am able to create the same variable in Journey and Global but when I create the first global variable, I am unable to create the journey variable with same name
</summary>
 <div>
  <div>Variables should not have the same name. If they do, it will fetch the value for which it is assigned based on the assigned priorities from global to local.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How to retrieve multiple data from the database node?
</summary>

<div>
 <div>

 Create  <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/code"> function </a> and extract the data from the variable that <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/bot-variables#-4-store-and-access-variables-via-nodes">stored the DB response.</a>

 Write

 ```
 let records = data.variables.db_response.records
 console.log(records, "records")
 ```

 Log the result and check the data. After this you can use the data based on your use case.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why am I getting a fallback message even when WhatsApps list message is configured?
</summary>
 <div>
  <div>To avoid a fallback message, you must store the value of the WhatsApp list option in a variable and use an IF condition to compare the variable value to trigger the respective outcome (flow, text, and so on).
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>What is a transformation function in integration node?
</summary>
 <div>
  <div> The <b>Parse API response</b> field helps you fetch custom functions that will filter out specific data from the API response you recieve. For steps to use it, click <a href="https://docs.yellow.ai/docs/cookbooks/integrations/parseapi">here</a>.​
</div>
  <br/>
   </div>
</details>

<details>
 <summary> What is the difference between Dynamic chat node and Prompt Executor node?
</summary>
 <div>
  <div>The <b>Dynamic chat node</b> drives the conversation around a particular goal whereas the <b>Prompt Executor</b> node just executes the given prompt and exits the flow. You can use Dynamic chat node if you want the AI-agent to have goal based conversations with the user, for example telling the user about different loans and convincing them to buy one. You can go with the Prompt Executor node if you want the AI-agent to just perform a certain action such as generating a recipe, writing a poem or performing a calculation.
</div>
  <br/>
   </div>
</details>

<details>
 <summary> Why does selecting a QR button go to the default fallback instead of the next step?
</summary>
 <div>
  <div>When users click QR (Quick Reply) buttons after 24 hours of conversation with the AI-agent, the context is lost. As a result, the button click triggers the fallback response instead of proceeding to the next step.
</div>
  <br/>
   </div>
</details>

------

### Documents

<details>
 <summary>What does a good document format look like?
</summary>
 <div>
  <div>The following are some of the characteristics of a document that’ll be processed well during document cognition. It's recommended to follow these guidelines while pre-processing your document -
​
  
​
* It does not have scanned pages and images, these will be skipped if present in the doc.
​
* At least 80% of the content is textual and well-formatted (e.g. Wikipedia articles)
​
* Remove content and index pages, appendix pages, etc. (we will add the logic to skip these automatically in coming releases)
​
* No bullet points before headings. Headings should have a larger font size and no spaces so that the parser can detect headings easily.
​
* Simple tabular data works better than complex or merged tabular data in the documents.
​
  
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why am I not getting the right result in the first suggestion?
</summary>
 <div>
  <div>Because document cognition is a probabilistic model that is “predicting” the relevance of a specific paragraph or page by looking at the input string. There is no guarantee that the first result will be the most relevant. The most relevant results are expected to come in the top 3 results.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why am I getting the other documents in suggestions which don't have the answer?
</summary>
 <div>
  <div>Same answer as above. The model assigns individual scores to all the documents’ paragraph and use them to show the results, so if the confidence threshold is low it can still show irrelevant answers. You can fine-tune the confidence threshold using some test cases.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why am I getting multiple occurrences of the same document in the results?
</summary>
 <div>
  <div>Because there might be multiple pages/occurrences of relevant content in the same document. In such cases, we rank them, based on the score and return only two occurrences in each document by default. If you want to see more or fewer occurrences within the same document, you can control it by passing the value of `results per document` in your search query.
​
</div>
  <br/>
   </div>
</details>
 
 <details>
 <summary>Can the model read tabular data or image presents in the documents?
</summary>
 <div>
  <div>Tables can be indexed by enabling the Parse table option while uploading, Simpler table works better than complex/merged tables. Images/diagrams will be skipped.
​
</div>
  <br/>
   </div>
</details>
 
<details>
 <summary>Why am I not able to access a document link, from a conversation I had yesterday? Can I change this dynamic URL to some fixed redirection URL?
</summary>
 <div>
  <div>Currently, we have restricted the life of each SAS link to an hour for security reasons. This can be removed/updated as per the client's request. You can generate a new link by asking the same query again in the AI-agent. You can also change this redirection URL to a fixed URL using the document properties option.
 
​
![](https://camo.githubusercontent.com/f1d4e073603851fadf4777a41e25d88d9412a1856666b67f8f0738b5b5d1daea/68747470733a2f2f63646e2e79656c6c6f776d657373656e6765722e636f6d2f524c333558336d436f7a5038313631333534343436393233362e706e67) 
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How do I ensure that the AI-agent shows only relevant documents?
</summary>
 <div>
  <div>There is no specific logic added to detect irrelevance right now. However, we do provide a relevance score with each search result that the AI-agent developer can use. The model returns all documents which contain even a few keywords in the query in decreasing order of relevance. The AI-agent developer can choose to show only Top N (e.g. Top 5) or Top 25% of the results based on relevance score.
​​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Can the Doc cog work if the documents are stored in a different system?
</summary>
 <div>
  <div>Doc cog has in-build integrations for Sharepoint, S3, URLs, and KBs (Salesforce, Service-now, Confluence). Any other KB can also be integrated which has APIs to access the articles/documents.
​​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Docs QNAs are not being generated, do I need it for working of doc cog? or can I edit the response of doc cog results?
</summary>
 <div>
  <div>Doc cog search will work fine without the QNAs. If the upload docs are showing completed status, you can just enable doc cog fallback or add Action Node and start using it. QNA's are only required for editing the answers and adding them to the FAQs section.
​​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Is permission-based Doc cog results possible so that only certain groups of people can search in a certain list of Docs / External KBs?
</summary>
 <div>
  <div>Yes, It is possible, User can add tags to the documents and pass the tag value as a variable in the doc cog action node while searching.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>If a single document has different answers/responses wrt a user profile like CEO, HR, SDE etc, Can we filter and show just the answers related to the User Profile?
</summary>
 <div>
  <div>If the results are on a different page, page logic can be used to filter the results
​
if answers are in a tabular structure, you can try adding the role of the user in the query itself, like

​
```<query>: SDE”, eg. Annual leave entitlement?, SDE"```
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why my documents are taking so long for indexing, is it stuck?
</summary>
 <div>
  <div>Doc cog uses queue base indexing flow which has a common queue among all the AI-agents. A pending/queued status represents doc is still in the queue and waiting for indexing while the indexing status represents the doc is being indexed.
​
</div>
  <br/>
   </div>
</details>


<details>
 <summary>Is there any limit on documents uploading?
</summary>
 <div>
  <div>Yes, for a Tier 0 (Free Tier) AI-agent there is a limit of a max of 50 total pages or a max of 5 documents and Tier 1 AI-agent has a max 200 documents limit. Tiers other than T0 can have max of 500 pages per document.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Can I index my articles present on ServiceNow / Confluence / Salesforce etc.?
</summary>
 <div>
  <div>Yes, using Doc cog External KB integration it is possible to index the articles using the APIs.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why my AI-agent is showing Journey Suggestions (Did you mean) instead of Doc cog results in fallback?
</summary>
 <div>
  <div>A AI-agent has a specific priority order of actions in the fallback case.
​
Order: Journey -> FAQs -> Journey suggestion -> Doc cog -> Other fallback.
​
So if the Journey suggestions are enabled and with good suggestion confidence, Journey suggestion will be triggered due to the priority order. You can try disabling the suggestion or increasing the confidence threshold of the suggestion.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Can I change the layout of the doc cog results cards?
</summary>
 <div>
  <div>Yes, but the default layout is recommended which helps us in analytics, improves accuracy and provides a better user experience.
​
A layout that can be changed: Change vertical to horizontal cards, change the display name, remove tags, and remove the preview button.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How do I suggest documents from a category?
</summary>

 You cannot. If you have configured the document search node, you will receive answers from it, otherwise, it suggests alternatives. If neither option is available, it resorts to the fallback.

 <div>
  <div>
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How to Change the Default Fallback Response of Document Search?
</summary>
In the Flow editor, add the <b>Knowledge Search</b> node and connect the <b>Fallback</b> output to a Message, Prompt, or Action node. This ensures that when no relevant document is found, the bot provides this custom fallback response instead of the default response.

 <div>
  <div>
​
</div>
  <br/>
   </div>
</details>

---------

### Functions & APIs

<details>
 <summary>How to get the exact status code as our API Event Data explorer while getting API responses in a journey?
</summary>
 <div>




 <div>

 Create a <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/code"> function </a> after the API call and apply the below code snippet.

 ```
 ymLib.args.apiResponse.statusCode
 ```
 
 </div>
 <br/>
 </div>
 </details>


<details>
<summary>Can I fetch data directly from array or object variables within a function?</summary>

Yes, ensure that you declare the array or object variable before attempting to capture or fetch data from it within the function. Here's a sample of valid data fetching:

```js
let req = data.variables.getReq; // Assigning value from array variable
let jobs = data.variables.getJobs; // Assigning value from object variable

let jobsData = jobs.d; // Fetching key from object
let reqData = req.d.results; // Fetching key from array
```
</details>

<details>
 <summary> How do we access values from an object data type in a Function?</summary>

 It's essential to declare the variable according to its datatype before performing calculations. For instance, if it's an object variable, declare the object variable first and then capture the required data. Here's a simple example:

 You can access the values as follows:

```js
return new Promise(resolve => {
    // Your logic goes here
    let userInput = data.variables.dateList;
    console.log(userInput);
    console.log(userInput.value.date);

    let selectedDate = userInput.value.date;
    resolve(selectedDate);
});
```

Note: If you want to capture the date, store the response in a variable of type number. [Click here for more details](https://docs.yellow.ai/docs/platform_concepts/studio/build/code#using-functions-in-flows).

</details>



<details>
 <summary> How can I extract specific date values from a function that returns a date?
 </summary> 

To extract specific date values, you can use the following syntax:

* Day: data.variables.{FunctionName}.value.day
* Month: data.variables.{FunctionName}.value.month
* Year: data.variables.{FunctionName}.value.year
* Date: data.variables.{FunctionName}.value.date

</details>

<details>
<summary>How do I pass user responses collected in a node to a function?</summary>

To pass user input from node to a function, follow these steps:

1. In a flow, use a **Prompt** node (Question, Quick replies) to collect user input and **Store the response in** a variable.

      ![](https://i.imgur.com/8DvMW9r.png)
      
2. Navigate to the **Functions** section and create a new function. In this function, use below syntax to access the user response (Variable).

`let any_variable_name = data.variables.selected_user_variable;`  

Example: 

```javascript
return new Promise(resolve => {
        // Your logic goes here
        let userName=data.variables.user_name;
    console.log("userName :" + userName);
        resolve(userName);
    });  
```

   ![](https://i.imgur.com/PL2AYwi.png)
   
3. Go to your flow and add a **Function** node after the Prompt node. Select the function that you have created to pass the user input.

      ![](https://i.imgur.com/H5QUEQs.png)
      
4. Test your flow using the **Preview** option to view the user's input, which is passed to the function.

5. To verify, go to **Analyze** > **Conversation logs**.

    ![](https://i.imgur.com/yrISEwZ.png)
    
6. Go to **Logs** and click on the below high-lighted icon.

   ![](https://i.imgur.com/Jteo6Sc.png)
   
7. Click on **Logs** icon to view the user input.

    ![](https://i.imgur.com/S2DcP4P.png)

</details>

<details>
 <summary> How to access the data of the database inside a function?</summary>

To access database data within a function, store the database response in a variable of type object and use it within the function. You can retrieve and process the data using the following function:

```js
return new Promise(resolve => {
        // Your logic goes here
        let records = data.variables.db_response.records;
    console.log(records, 'records');
        resolve(records);
    }); 
```

<b>Note</b>: Here, "db_response" is the variable name of object data type in which the database (search) node's response is stored.

</details>


-------



### Journey(flow)

<details>
 <summary>Can I retrieve journey data outside the AI-agent?
</summary>
 <div>
  <div>The accessibility of journey data depends on the type of variable:<br/>
 <br/> <b>Journey Variables:</b> These variables are limited to the flow in which they are created and can only be accessed within that specific flow.<br/>
 <br/> <b>Global Variables:</b> Unlike journey variables, global variables are accessible across all flows within your AI-agent, allowing for broader usage and integration of journey data.<br/>
<br/><b>User Properties:</b> User properties are user variables that can be accessed in Automation, Engage, and User 360.<br/>
<br/>You can use the appropriate variable type based on your specific use case.<br/>
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How to open a website in a AI-agent conversation?
</summary>
 <div>
  <div>Add a <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/message-nodes1/text-node">text node</a> to the flow and paste your website URL in it.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How do I link one flow to another flow for a AI-agent?
</summary>
 <div>
  <div>Use <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/nodes/action-nodes-overview/execute-flow">Execute Flow</a> to link  another flow to a AI-agent.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How to export/clone a journey to another AI-agent?
</summary>

 <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/exportflow#-1-export-bot-template">Export the template of that journey</a> and <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/exportflow#14-view-approved-template-in-marketplace"> import it </a> to the AI-agent of your preference.

 <div>
  <div>
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Will regex entity trigger a flow?
</summary>

 Yes, <a href="https://docs.yellow.ai/docs/platform_concepts/studio/train/entities#add-regex-type-entities">create a regex entity</a> and set it as the <a href="https://docs.yellow.ai/docs/platform_concepts/studio/build/Flows/configureflow#trigger-flow-using-entities">start trigger for a flow</a>.
 <div>
  <div>
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>What does it mean when the AI-agent is in a critical status? Does it affect the AI-agent's operations or performance?
</summary>
 <div>
  <div>When the AI-agent is in a critical status, it means that the health check configured for the AI-agent is failing. However, this does not have any impact on the AI-agent's operations or performance.
You can execute the health check and update the test case to bring the status back to normal.
​
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Can a flow be restored from Staging to Sandbox if it was deleted from Sandbox?
</summary>
 <div>
  <div>No, it is not possible to restore a flow from Staging to Sandbox. You can publish a flow from lower to higher environments, and there is no rollback mechanism to retrieve deleted flows back to Sandbox. If a flow is deleted from Sandbox, it must be recreated manually.
​
</div>
  <br/>
   </div>
</details>

### KB

<details>
 <summary>How can we tailor the responses retrieved from the knowledge base? For instance, by restricting the response size, presenting answers in sequential steps when appropriate, and interpreting tables and flowcharts.
</summary>

You can customize KB responses by following the steps mentioned [here](https://docs.yellow.ai/docs/platform_concepts/studio/kb/advancedsettings#modify-auto-generated-bot-answers). To present the steps in sequential manner, [set the AI-agent's tone to Instruction based](https://docs.yellow.ai/docs/platform_concepts/studio/kb/advancedsettings#set-tone-for-your-bot-responses). KB interprets data only from websites and not from tables and flowcharts directly. However, you can provide the website URL containing the tables, flowcharts, and supporting data.

 <div>
  <div>
​
</div>
  <br/>
   </div>
</details>


<details>
 <summary>How to use knowledge base for pdf?
</summary>
To upload PDFs to your Knowledge Base, follow the steps mentioned <a href= "https://docs.yellow.ai/docs/platform_concepts/studio/kb/ingestion#upload-documents-from-local-system" >here</a>.
 <div>
  <div>​
</div>
  <br/>
   </div>
</details>


<details>
 <summary> While using Doc cog (document search) the AI-agent response generates irrelevent links, how to resolve it? 
</summary>
 <div>
  <div> 
      Increase the Document search threshold value to improve the accuracy of the links generated.
</div>
  <br/>
   </div>
</details>


<details>
 <summary> Why do search results differ between the app platform and the cloud? 
</summary>
 <div>
  <div> 
      If the knowledge base is the same, search results may vary due to differences in the search algorithms or indexing processes between the platforms.
</div>
  <br/>
   </div>
</details>

<details>
 <summary> Does our platform support multilingual websites?
</summary>
 <div>
  <div> 
      No, currently multilingual websites are not supported as a live feature. Only English and Bahasa languages are supported.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why does the AI-agent display incomplete information from the website?
</summary>
 <div>
  <div> 
      This could happen if you edit or rephrase the query to get the context of the conversation, which can sometimes result in incomplete information being displayed by the AI-agent.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why can't I configure SharePoint even though my credentials are correct?
</summary>
 <div>
  <div> 
     When configuring SharePoint folders, ensure that you remove "https:" from the target host.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How do I handle uploaded documents where the company is referred to as a third party (for example, "them" and "they provide")?
</summary>
 <div>
  <div> 
     To avoid confusion, use the model response type set to "formal/short answer" to ensure clarity.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why doesn't the URL "xyz/abc.com" work when the domain is listed as "ABC Network - ABC.com"?
</summary>
 <div>
  <div> 
     The issue is that the domain has been configured to retrieve answers only from the specified website ("ABC.com"). Ensure that the site URL passed under the document cog node matches the configured domain.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How to avoid irrelevant documents being fetched for the entered query?
</summary>
 <div>
  <div> 
     To prevent this issue, adjust the document search threshold confidence level. By setting an appropriate threshold, irrelevant documents can be filtered out more effectively, enhancing the relevance of the search results.<br/> <b>Note:</b> The model has inherent accuracy limitations, so the results may not be 100% accurate all the time.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>How to enable summarized results and summarized answers for the Knowledge Base (KB)?
</summary>
 <div>
  <div> 
     To enable summarized results and summarized answers for the Knowledge Base (KB), follow these steps:<br/> 1.Go to <b>Automation</b> > <b>Build</b> > <b>Conversation settings</b>.<br/> <img src="https://i.imgur.com/GXendkw.png" alt="drawing" width="80%"/><br/>2.Under Document Search, enable <b>Summarized results</b> and <b>Summarized links</b>. <img src="https://i.imgur.com/odRJlGs.png" alt="drawing" width="70%"/>
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Why is document search not working?
</summary>
 <div>
  <div> 
     If the document search is not functioning, follow these troubleshooting steps:<br/>
     * <b>Ensure data is indexed</b>: Verify that the data is properly indexed.<br/>
     * <b>Check search configuration</b>: Confirm that the document search node is correctly configured. If not, the system will suggest alternatives or fallback options.<br/> 
     * <b>Use filters</b>: Narrow down the search by filtering based on file name, source, status, or tags.<br/> 
     * <b>Enable document search node</b>: Ensure that the document search node is enabled in the automation flow.Add a prompt node to capture the user query and use the document search node to fetch the response.<br/> 
     * <b>Check search categories</b>: Confirm that you are searching within the correct categories, such as ticket details or message details.<br/>

</div>
  <br/>
   </div>
</details>

<details>
 <summary>Does the bot understand images as inputs in the Knowledge Base?
</summary>
 <div>
  <div> 
     No, currently the bot does not understand or process images as inputs in the Knowledge Base. It can only understand text-based content.
</div>
  <br/>
   </div>
</details>


--------

## Localization

<details>
  <summary> Why is the text in a Message Carousel not appearing in the correct language when using Localization? </summary>
  <div>
    When using localization (translation) for a Message Carousel, if you upload different images for different languages in the same node, the images will display correctly, but the text will appear in the default language (e.g., English). This happens because images are manually uploaded per language, but the text does not update automatically unless added separately. To ensure both text and images appear correctly in the selected language, follow these steps:
    <ul>
      <li>Switch to the desired language in the flow.</li>
      <li>Manually add the translated text for that language.</li>
    </ul>
    By doing this, the Message Carousel will display both text and images correctly in different languages.
  </div>
</details>


-------

## General FAQs

<details>
 <summary>Is it possible to add pictures to the GenAI prompt?
</summary>
 <div>
  <div> 
     Currently, adding images to the GenAI prompt is not supported. The prompt is designed to process and generate responses based on text inputs, as Large Language Models (LLMs) primarily work with textual data. Supporting images would require advanced multimodal capabilities, which are not yet available in the current implementation.
</div>
  <br/>
   </div>
</details>




<details>
 <summary>What is the difference between <b>Suggestions</b> and <b>Fallback</b> under conversation settings? 
</summary>
 <div>
  <div> 

Suggestions appear when the bot's confidence level falls below the set minimum threshold. A fallback is triggered when no similar intents are available to generate suggestions.  <br/> Maximum number of buttons that are visible suggestions will depend on the number of intents being predicted.

</div>
  <br/>
   </div>
</details>

<details>
 <summary>Is it possible to add pictures to the GenAI prompt?
</summary>
 <div>
  <div> 
     Currently, adding images to the GenAI prompt is not supported. The prompt is designed to process and generate responses based on text inputs, as Large Language Models (LLMs) primarily work with textual data. Supporting images would require advanced multimodal capabilities, which are not yet available in the current implementation.
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Is it possible to concatenate (combine) two variables into one?
</summary>
 <div>
  <div> 
     Yes, if the variables are of the string data type, they can be directly concatenated. However, for other data types such as arrays, objects, or integers, you need to write custom logic to concatenate.

   You can concatenate two string variables using the following syntax:

    `{{{variables.user_name}}_{{{variables.last_name}}}`

   A separator such as `_`, `-`, `.`, space, or comma must be used between the two mustache expressions to ensure proper formatting.
   
Refer to the following gif to see how to consolidate two variables into one:<br/><img src="https://imgur.com/FW1gbVn.gif" alt="drawing" width="70%"/>
</div>
  <br/>
   </div>
</details>

<details>
 <summary>Is it possible to import variables?
</summary>
 <div>
  <div> 
     No, it is not possible to import variables directly. However, you can manually define and assign values to variables within the platform or pass them through API calls based on your use case.
</div>
  <br/>
   </div>
</details>


<details>
<summary> What utterances are included in the Studio > Analysis > Message View report, and why might the number of fetched utterances be lower than expected? </summary>
<div>

 This report includes both identified and unidentified utterances when the confidence level is set between 0 and 1. To fetch only unidentified utterances, set the confidence level below the minimum confidence configured in the bot’s NLU settings. The number of fetched utterances may be lower than expected because the report only lists utterances the bot has not seen before, excluding duplicates.
    
</div>
</details>

<details>
<summary> Can we block a user from sending messages to the bot? </summary>
<div>

No, currently you cannot block a user from sending messages to the bot directly.
    
</div>
</details>

<details>
<summary>What does the Failed to encrypt error mean?</summary>
<div>

This error means that the method or function trying to encrypt some data has failed.
It usually happens due to:<br/>* Incorrect encryption setup (like a missing key or invalid input).<br/>* System-level issues or bugs in the function. To find the exact cause, you’ll need to check the full error message and logs for more details.
    
</div>
</details>





