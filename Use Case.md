## Entities (Data Model).
Entity Attributes	Description.
1. **Employee** Employee_ID, Name, Email, Department, Role, Leave_Balance	represents an employee of the company.
2. **Manager**	Manager_ID, Name, Email, Department	Approves or rejects vacation requests.
3. **Vacation_Request**	Request_ID, Employee_ID, Start_Date, End_Date, Hours_Per_Day, Category, Description, Status, Manager_ID, Created_Date	Holds all details of each leave request.
4. **Leave_Category**	Category_ID, Category_Name, Max_Days	represents types of leaves (Vacation, Sick, Personal).
5. **Email_Notification**	Notification_ID, Receiver_ID, Subject, Message, Status, Sent_Date	Tracks emails sent for approvals or updates.
6. **System_Log**	Log_ID, User_ID, Action, Timestamp, Details	Records all user and system activities.

## Flow Chart
<img width="924" height="750" alt="VTS Flow Chart" src="https://github.com/user-attachments/assets/11efae05-426a-45ce-9f4a-e889d123a1fb" />

## Sequence Diagram 


## Pseudocode
BEGIN ManageVacationRequest
    IF Employee is not authenticated THEN
        DISPLAY "Access Denied"
        EXIT
    END IF

    DISPLAY Employee Leave Balance

    INPUT VacationType, StartDate, EndDate, Hours, Description

    IF any field is missing OR invalid THEN
        DISPLAY ErrorMessage
        RETURN to Form
    END IF

    CREATE new VacationRequest
    SAVE VacationRequest to Database

    IF ManagerApprovalRequired THEN
        SEND Email to Manager
        SET Request.Status = "Pending Approval"
    ELSE
        SET Request.Status = "Approved"
        SEND Confirmation Email to Employee
    END IF

    WAIT for Manager Action

    IF Manager.Approve THEN
        UPDATE Request.Status = "Approved"
    ELSE IF Manager.Reject THEN
        UPDATE Request.Status = "Rejected"
        RECORD Reason
    END IF

    SEND Notification Email to Employee
END
