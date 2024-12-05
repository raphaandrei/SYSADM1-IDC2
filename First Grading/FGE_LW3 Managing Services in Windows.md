
![image](https://github.com/user-attachments/assets/b43d2ed3-fafa-4452-9970-6c6c3cecb317)


# SYSADM1 – Managing Services in Windows
# Requirement: 
- A virtual machine running Linux and Windows OS

**Services** are background processes that run independently of user interactions in Windows. They provide essential system functions, such as network connectivity, printing, and time synchronization. This lab will guide you through the process of managing services using the Services app.
# Instructions: 
1. Open the Start menu and search for "Services"
1. Familiarize yourself with the columns, including Service Name, Display Name, Status, and Startup type.
1. Right-click on a service and select "Start", "Stop", or "Restart". Fill out the table below

   |**Status**|**Name of Service** |**Screenshot**|
   | :-: | :-: | :-: |
   |Start|Credential Manager|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.002.png)|
   ||||
   |Stop|Diagnostic System Host|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.003.png)|
   |Restart|Base Filtering Engine|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.004.png)|
   |Pause|Diagnostic Policy Service|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.005.png)|

1. Select five network services, right-click to view its properties. Modify the startup setting to Manual.

   **SS**:

   |Network Location Awareness|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.006.png)|
   | :- | :- |
   |Network Store Interface Service|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.007.png)|
   |IP Helper|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.008.png)|
   |TCP?IP NetBIOS Helper |![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.009.png)|
   |Windows Firewall|![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.010.png)|


1. Explore the "General", "Recovery", and "Log On" tabs to understand additional service settings.
1. Create a batch file that will be added as a new service later on. Refer to the batch file code below.

   ![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.011.png)

1. Save the batch file in Z:\lastname\_timer.bat

   ![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.012.png)

1. Use the sc command to add timer.bat service in the command line interface.

   *sc create BatchTimerService binPath= "path\_to\_your\_batch\_file.bat" start= auto*

   *net start BatchTimerService*

   **Replace path\_to\_your\_batch\_file.bat with the actual path to your batch file.**

1. Verify that BatchTimerService has been added to the services.

   **SS: ![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.013.png)**

1. **Testing the Service:** Now, if you open a new command prompt, you should see the timer countdown without requiring your interaction. Once the timer finishes, you'll see the "Timer finished!" message.





   **SS:**

   ` `![](Aspose.Words.dbfa4ed8-25e5-4f88-9449-c0ade22055e3.014.png)

**Rubric**

|**Criteria**|**Excellent (10)**|**Good (7)**|**Needs Improvement (3)**|**Unsatisfactory (1)**|
| :-: | :-: | :-: | :-: | :-: |
|Understanding of Services|Demonstrates a deep understanding of the concept of services, their roles, and their importance in Windows.|Shows a solid understanding of services, but may lack some depth in specific areas.|Has a basic understanding of services, but may struggle with specific concepts.|Shows little or no understanding of services.|
|Service Management Skills|Successfully starts, stops, restarts, and configures services using the Services app.|Demonstrates proficiency in managing services, but may encounter minor difficulties.|Can perform basic service management tasks, but may need assistance or guidance.|Struggles to perform even basic service management tasks.|
|Custom Service Creation|Successfully creates and manages a custom service using the appropriate tools and techniques.|Can create a custom service, but may encounter minor difficulties or require assistance.|Has limited experience with creating custom services.|Cannot create a custom service.|
|Problem-Solving|Demonstrates strong problem-solving skills when encountering challenges or errors.|Can effectively troubleshoot and resolve most issues related to service management.|May require assistance to troubleshoot some issues.|Struggles to troubleshoot and resolve issues.|
|Documentation and Reporting|Provides clear and concise documentation of the lab activities, including relevant screenshots and observations.|Documents the lab activities adequately, but may lack some detail or clarity.|Provides basic documentation, but may be disorganized or incomplete.|Does not provide any documentation or reporting.|
|**Score:**|`     `**/50**||||


`	`Page 8** of 8**	
