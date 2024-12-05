
![image](https://github.com/user-attachments/assets/b43d2ed3-fafa-4452-9970-6c6c3cecb317)


# SYSADM1 – Managing Services in Windows
# Requirement: 
- A virtual machine running Linux and Windows OS

**Services** are background processes that run independently of user interactions in Windows. They provide essential system functions, such as network connectivity, printing, and time synchronization. This lab will guide you through the process of managing services using the Services app.
# Instructions: 
1. Open the Start menu and search for "Services"
1. Familiarize yourself with the columns, including Service Name, Display Name, Status, and Startup type.
1. Right-click on a service and select "Start", "Stop", or "Restart". Fill out the table below

   ![image](https://github.com/user-attachments/assets/f4e70df0-20f8-4930-bfff-3cc00594adfb)


1. Select five network services, right-click to view its properties. Modify the startup setting to Manual.

   **SS**:

   ![image](https://github.com/user-attachments/assets/43da4089-9e5f-4abb-a6a4-23314bc1a4b4)
   ![image](https://github.com/user-attachments/assets/62571af3-ff09-44cf-ba72-01aa9e84c184)
   ![image](https://github.com/user-attachments/assets/e3057a12-1b85-4c51-b30d-c2f5be23bb54)
   ![image](https://github.com/user-attachments/assets/4516f35d-5088-4d9c-89c2-843425053e7c)






1. Explore the "General", "Recovery", and "Log On" tabs to understand additional service settings.
1. Create a batch file that will be added as a new service later on. Refer to the batch file code below.

   ![image](https://github.com/user-attachments/assets/21a37221-f623-46f9-9f2f-916b02afb0e4)


1. Save the batch file in Z:\lastname\_timer.bat

   ![image](https://github.com/user-attachments/assets/cf667b0f-3b8b-4707-9649-cb4182d4491e)


1. Use the sc command to add timer.bat service in the command line interface.

   *sc create BatchTimerService binPath= "path\_to\_your\_batch\_file.bat" start= auto*

   *net start BatchTimerService*

   **Replace path\_to\_your\_batch\_file.bat with the actual path to your batch file.**

1. Verify that BatchTimerService has been added to the services.

   ![image](https://github.com/user-attachments/assets/a5f98d4b-052b-4ebc-ad50-11194320822f)


1. **Testing the Service:** Now, if you open a new command prompt, you should see the timer countdown without requiring your interaction. Once the timer finishes, you'll see the "Timer finished!" message.





   **SS:**

   ![image](https://github.com/user-attachments/assets/cadf3b3e-1ab9-4f84-b0ce-00e8ad57d9ec)


**Rubric**

![image](https://github.com/user-attachments/assets/5be5c57d-5cb9-452b-99af-e5e5513ede74)



`	`Page 8** of 8**	
