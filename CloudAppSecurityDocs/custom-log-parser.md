---
# required metadata

title: Use the custom log parser for logs that are not supported | Microsoft Docs
description: This article provides information about how to use the custom log parser to upload logs for devices that aren't supported to Cloud App Security.
keywords:
author: rkarlin
ms.author: rkarlin
manager: mbaldwin
ms.date: 5/4/2017
ms.topic: article
ms.prod:
ms.service: cloud-app-security
ms.technology:
ms.assetid: a612d87e-5471-4add-b4b1-dbbb530f2b61

# optional metadata

#ROBOTS:
#audience:
#ms.devlang:
ms.reviewer: reutam
ms.suite: ems
#ms.tgt_pltfrm:
#ms.custom:

---

# Use a custom log parser
Cloud App Security enables you to configure a custom parser to match and process the format of your logs so that they can be used for Cloud Discovery, even if they are from a firewall or device that is not explicitly supported by Cloud App Security. 

The custom parser enables you to use logs from unsupported firewalls by following this process. 


 
To configure a custom CSV parser:
1.	Collect logs from your firewall and proxy, through which users in your organization access the Internet. Make sure to gather logs during times of peak traffic that are representative of all user activity in your organization.  Open the logs you want to process in a text editor and review their format.

2. Copy the contents of the log into a CSV reader, such as Excel, and set the data to be delimited according to the delimiter in your data.
  
2.  In the Cloud App Security portal, click on **Discover** and then **Create new snapshot report**.  
  
    ![Create new snapshot report](./media/create-new-snapshot-report.png)
     
3.  Enter a **Report name** and a **Description**
  
4.  Under **Data source**, select **Custom log format...**.  

     ![New snapshot report](./media/custom-log-upload.png)   

5. In the **Custom log format** screen, fill in the fields based on your data to define the correlation between the fields and columns in the file and the data needed by Cloud App Security.

In order to accurately configure the parser, you need to define the column name for each of the required data attributes. 

Click **Save**. The custom log format your configured will be saved as the default custom parser. You can edit it at any time by clicking on Edit.

    ![custom log parser](./media/custom-log-parser.png) 

5.  **Choose the traffic logs** that you want to upload. You can upload up to 20 files at once. Compressed and zipped files are also supported.  
  

6.  Click **Create**.  

7.  After upload completes, the status message will appear at the top right corner of your screen letting you know that your log was successfully uploaded.  
  
8.  After you upload your log files, it will take some time for them to be parsed and analyzed.  
After processing of your log files completes, you will receive an email to notify you that it is done. 
  
9. A notification banner will appear in the status bar at the top of the portal to update you with the processing status of your log files.  
![processing log file menu bar](./media/processing-log-file-menu-bar.png) 
   
10. After the logs are uploaded successfully, you should see a notification letting you know that the log file processing completed successfully. At this point, a you can view the report either by clicking the link in the status bar, or by going to the Settings cog, and selecting **Cloud Discovery settings**.   
  
     ![Discovery settings tab](./media/discovery-settings-tab.png)
11. Then selecting **Manage snapshot reports** and select your snapshot report.
 
    ![snapshot report management](./media/snapshot-report-managment.png)

  
      




## See also
 
[Create snapshot Cloud Discovery reports](create-snapshot-cloud-discovery-reports.md)

[Configure automatic log upload for continuous reports](configure-automatic-log-upload-for-continuous-reports.md)

[Working with Cloud Discovery data](working-with-cloud-discovery-data.md)
