## Entities (Data Model).
Entity Attributes	Description.
1. **Employee** Employee_ID, Name, Email, Department, Role, Leave_Balance	represents an employee of the company.
2. **Manager**	Manager_ID, Name, Email, Department	Approves or rejects vacation requests.
3. **Vacation_Request**	Request_ID, Employee_ID, Start_Date, End_Date, Hours_Per_Day, Category, Description, Status, Manager_ID, Created_Date	Holds all details of each leave request.
4. **Leave_Category**	Category_ID, Category_Name, Max_Days	represents types of leaves (Vacation, Sick, Personal).
5. **Email_Notification**	Notification_ID, Receiver_ID, Subject, Message, Status, Sent_Date	Tracks emails sent for approvals or updates.
6. **System_Log**	Log_ID, User_ID, Action, Timestamp, Details	Records all user and system activities.
