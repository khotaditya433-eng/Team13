Feature Set III
The system includes the following five features:
Employee Details
Leave Balance
Leave Request
Leave Type
Approval Status
Algorithm
Start
Enter Employee Details such as Employee ID, Employee Name, and Department.
Verify the Employee Details.
Check and display the Employee's available Leave Balance.
Enter Leave Request details such as Leave Start Date, End Date, and Reason.
Select the Leave Type such as Casual Leave, Sick Leave, or Earned Leave.
Calculate the total number of Leave Days requested.
Compare the requested Leave Days with the available Leave Balance.
If the Leave Balance is insufficient, display "Insufficient Leave Balance" and stop the process.
If the Leave Balance is sufficient, submit the Leave Request.
Set Approval Status = Pending.
Send the Leave Request to the Manager/Approver for review.
Check the Approval Status.
If the request is rejected, set Approval Status = Rejected, notify the employee, and stop.
If the request is approved, set Approval Status = Approved.
Deduct the approved Leave Days from the Employee's Leave Balance.
Update the Leave Request and Leave Balance.
Notify the Employee about the final Approval Status.
Stop
Flowchart
The flowchart follows standard flowchart notation:
Oval → Start / End
Parallelogram → Input / Output
Rectangle → Process
Diamond → Decision
Arrow → Flow direction
Flow Logic
START
   ↓
Enter Employee Details
(Employee ID, Employee Name, Department)
   ↓
Verify Employee Details
   ↓
Check Available Leave Balance
   ↓
Enter Leave Request
(Start Date, End Date, Reason)
   ↓
Select Leave Type
(Casual / Sick / Earned)
   ↓
Calculate Required Leave Days
   ↓
◇ Is Leave Balance Sufficient?
   ├── NO → Display "Insufficient Leave Balance" → END
   │
   └── YES
         ↓
Submit Leave Request
         ↓
Set Approval Status = Pending
         ↓
Send Request to Manager/Approver
         ↓
Manager Reviews Leave Request
         ↓
◇ Is Leave Request Approved?
   ├── NO → Set Status = Rejected
   │          ↓
   │       Notify Employee
   │          ↓
   │         END
   │
   └── YES
         ↓
Set Approval Status = Approved
         ↓
Deduct Approved Leave Days
         ↓
Update Leave Request and Leave Balance
         ↓
Notify Employee
         ↓
END
Entity Relationship Diagram (ERD)
Entities
1. EMPLOYEE
Attribute
Key
Employee_ID
PK
Employee_Name
—
Department
—
Email
—
Phone
—
2. LEAVE_BALANCE
Attribute
Key
Balance_ID
PK
Employee_ID
FK
Leave_Type_ID
FK
Available_Days
—
3. LEAVE_REQUEST
Attribute
Key
Request_ID
PK
Employee_ID
FK
Leave_Type_ID
FK
Start_Date
—
End_Date
—
Total_Days
—
Reason
—
Approval_Status
—
4. LEAVE_TYPE
Attribute
Key
Leave_Type_ID
PK
Leave_Type_Name
—
Description
—
5. APPROVAL_STATUS
Attribute
Key
Status_ID
PK
Status_Name
—
Approved_Date
—
Remarks
—
Relationships
Relationship
Cardinality
EMPLOYEE → LEAVE_BALANCE
1 : M
EMPLOYEE → LEAVE_REQUEST
1 : M
LEAVE_TYPE → LEAVE_BALANCE
1 : M
LEAVE_TYPE → LEAVE_REQUEST
1 : M
APPROVAL_STATUS → LEAVE_REQUEST
1 : M
Project Structure
Employee-Leave-Leave-Request/
│
├── README.md
│
├── Algorithm/
│   └── Employee_Leave_Algorithm.txt
│
├── Flowchart/
│   └── Employee_Leave_Flowchart.png
│
└── ERD/
    └── Employee_Leave_ERD.png
Purpose
The purpose of this project is to demonstrate how an Employee Leave – Leave Request system can be designed using:
Step-by-step algorithm
Standard flowchart
Database-standard ERD
Primary Keys (PK)
Foreign Keys (FK)
Entity relationships
1:M cardinality
Technologies / Concepts
Database Management System (DBMS)
Entity Relationship Diagram (ERD)
Algorithm Design
Flowchart
Primary Key and Foreign Key
Relational Database Concepts
BCA / Computer Science Project
Conclusion
The Employee Leave – Leave Request project provides a structured design for handling employee leave requests. It verifies employee details, checks leave balance, records leave requests, manages leave types, processes approval status, updates leave balance, and notifies the employee about the final status
