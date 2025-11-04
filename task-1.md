## Requirements from Ch12 (Vacation Tracking System)
 Vision
The goal of the Vacation Tracking System (VTS) is to provide employees with a convenient way to manage their own vacation whatever it is annual leave, sick leave, or personal time off without needing to be experts in company or facility leave policies.
 ## Main Purpose:
•	Empower employees to manage their time-off requests.
•	Reduce the workload on the HR department.
•	Minimize managers’ administrative tasks.
•	Make the process faster, simpler, and more accurate.
________________________________________
## Functional Requirements (The features that the system must do)
1.	Implements a flexible rules-based system to validate leave requests.
2.	Allows manager approval (optional).
3.	Enables access to previous year’s requests and allows new requests up to 1.5 years in advance.
4.	Sends email notifications to managers and employees for approvals and status updates.
5.	Records activity logs for all transactions.
6.	Allows HR staff to override rules, with proper logging.
7.	Allows managers to directly grant personal leave (within system limits).
8.	Provides a Web Service interface for other internal systems to access leave summaries.
9.	Integrates with existing HR legacy systems to retrieve employee data.
10.	Provides an easy and intuitive user interface.
________________________________________
## Non-Functional Requirements
(System qualities and technical expectations)
1.	Ease of Use – The system must be simple and intuitive for all users.
2.	Integration – Must integrate with the existing intranet portal.
3.	Security – Must use the company’s Single Sign-On (SSO) mechanism.
4.	Performance – Should respond quickly and handle multiple users efficiently.
5.	Reliability – Should be stable and available with minimal downtime.
6.	Maintainability – Easy to update, configure, and extend in the future.
7.	Compatibility – Should run on the company’s existing hardware and middleware.
________________________________________
## Constraints
(Limitations that restrict how the system is designed or built)
1.	Must use existing hardware and middleware.
2.	Must be implemented as part of the existing intranet portal.
3.	Must use the existing Single Sign-On system for authentication.
4.	Must interface with legacy HR systems for data retrieval.
5.	Must be a Web-based application accessible via browsers.
________________________________________
 2. ## Domain (Define the Problem)
Currently, the company’s vacation request process is manual and slow.
Employees must submit requests that go through managers and HR clerks, often taking several days.
 Problem to Solve:- 
Create an automated system that:
•	Simplifies and speeds up leave requests.
•	Reduces HR involvement in each request.
•	Gives employees and managers direct control.
•	Improves efficiency and reduces processing time and cost.
________________________________________
 3. ## Actors of the System
Employee:	Submits leave requests, checks request status.
Manager:	Approves or rejects employee requests.
HR Staff:	Updates employee data and can override rules when needed.
System Administrator:	Manages system settings, logs, and permissions.
Email System:	Sends notifications to employees and managers.
HR Legacy System:	Provides existing employee data to the VTS.
Other Internal Systems:	Access vacation data through the Web Service interface
