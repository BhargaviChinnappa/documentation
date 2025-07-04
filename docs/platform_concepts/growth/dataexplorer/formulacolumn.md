---
title: Add a new formula column to the table 
sidebar_label: Add formula column  
---

You can create new columns in tables (custom/default), by specifying formulas to derive their values.


:::note
You can only apply Custom formulas after applying **Summarization** > **Group-by** operation. 
:::

## Add a formula column  

To add a formula to a column, follow these simple steps:

1. Click on the **Actions** dropdown menu and select **Add formula column**.
    ![image](https://imgur.com/Q0xgBbH.png)
2. Enter a **Name** for the formula in the tab that appears.
    ![](https://imgur.com/qnFMs0t.png)
3. Add the required formula using entities like calculating values in a column, calculating values in a specific cell, adding integers or arithmetic operators.
    - To add a column, select **Select column** under **table operations**. The available columns in your summarized table will be listed on the right side. Click **Add** next to the column name.
    ![](https://imgur.com/1le4ZIe.png)
    - To add a cell, select **Select cell** after choosing a column. All the available rows for the selected column will be displayed in the dropdown list. Select a value.
    ![](https://imgur.com/734TXBW.png)
    - Complete the formula with numbers and operators **+, -, *, /, ()**.
    - Click **Next**.
    ![image](https://imgur.com/dMQyhnh.png)

4. You can add multiple formula columns following the same steps measured above. 

### Edit/Delete formula column

The summarized table will now have a new column with the calculated formula values. You can edit or delete this data as needed by clicking on the new column name.

![image](https://imgur.com/hsS3KsT.png)

### Save the report 

Click **Save query** to save this as a new report or add it to the existing one. 

![image](https://imgur.com/b9IVjeS.png)


## Common formulas that can be applied on summarized tables

1. **Ticket status percentage split** (used to Summarize Chat tickets table by their ticket status count)      
**New column**: `Status %`     
**Formula**: `Count / (Count, RTotal) * 100`     
![](https://i.imgur.com/fQmaZzl.png)

2. **Journey retention rate** (Used to summarize flows started count and group by flows - to see funnel of users from one flow to another)     
**New column**: `Retention rate`     
**Formula**: `Count / (Count, R1) * 100`     
![](https://i.imgur.com/fKPKvKh.png)

3. **Average session duration every month** (Used to get count of unique Session IDs and sum of user response time for each message - grouped by month)     
**New column**: `Average session duration`     
**Formula**: `SUM_SESSION_SUM / DISTINCT_SESSIONID`     
![](https://i.imgur.com/FGREMwr.png)



