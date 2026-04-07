# 📘 SAP ABAP Interview Q&A – Topic-wise Classification

## 🔹 1. SAP Introduction & Data Dictionary (DDIC)

### Core Concepts

**Q10. What is a Structure?**

Answer:  
A Structure is a collection of different data fields grouped together but it does not store data in the database. It is mainly used for data processing in programs.

---

**Q11. What is a Check Table?**

Answer:  
A Check Table is used to validate data using a foreign key relationship. It ensures that only valid values from the referenced table are entered into the field.

---

**Q36. What are Views and their types?**

Answer:  
A View is a virtual table created from one or more database tables.  

Types of Views:  
• Database View  
• Projection View  
• Maintenance View  
• Help View  

---

**Q37. What is the first field you create when creating a table?**

Answer:  
The first field usually created is MANDT (Client Field).

---

**Q38. What is MANDT field and why do we use it?**

Answer:  
MANDT represents the client field in SAP. It is used to separate data between different clients in the same SAP system.

---

**Q43. What objects are available in ABAP Dictionary?**

Answer:  
Common ABAP Dictionary objects include:  

• Tables  
• Views  
• Data Elements  
• Domains  
• Structures  
• Table Types  
• Lock Objects  
• Search Helps  

---

**Q44. What is Technical Settings while creating a table?**

Answer:  
Technical settings define how the table is stored in the database.  

It includes:  
• Data class  
• Size category  
• Buffering settings  
• Logging options  

---

**Q49. What is Primary Key in SAP Table?**

Answer:  
A Primary Key is a field or combination of fields that uniquely identifies each record in a table. Primary keys cannot contain duplicate or null values.

---

**Q65. Difference between Value Table and Check Table**

Value Table                            |        Check Table  
Provides possible values for a field   |     Ensures referential integrity  
Used in domain level                   |     Used in foreign key relationship  

---

**Q86. What is Cardinality?**

Answer:  
Cardinality defines the relationship between two entities or tables, indicating how many records of one entity are related to another.  

Examples: 1:1, 1:N, N:1, N:N.  
In CDS views, cardinality helps define relationships between entities.

---

**Q94. What is a Table? Types of Tables**

Answer:  
A Table in SAP stores structured data in rows and columns.  

Types:  
1. Transparent Table – Data stored directly in database  
2. Cluster Table – Multiple tables stored in one database table  
3. Pooled Table – Many logical tables stored in a single physical table  

---

**Q112. What is DATA CLASS in Transparent Table Settings?**

Answer:  
Data Class defines the physical storage area of the table in the database.  

Examples:  
• APPL0 – Master data  
• APPL1 – Transaction data  
• APPL2 – Organizational data  

It helps the database manage storage and performance efficiently.

---

**Q140. What is Foreign Key?**

Answer:  
A Foreign Key is a field in one table that references the primary key of another table, ensuring data integrity and relationship between tables.

---

### Table & Object Creation

**TMG**

**Q32. How do you create a TMG?**

Answer:  
TMG stands for Table Maintenance Generator.  

Steps:  
1. Go to SE11  
2. Open the table  
3. Click Utilities → Table Maintenance Generator  
4. Maintain Authorization Group and Function Group  
5. Generate  

---

**Q57. Why is TMG used in SAP and how is it performed?**

Answer:  
TMG (Table Maintenance Generator) is used to create maintenance screens for tables so users can insert, update, and delete records easily.  

Steps:  
1. Go to SE11  
2. Open the table  
3. Click Utilities → Table Maintenance Generator  
4. Maintain function group and authorization group  
5. Generate  

---

**Q105. What is TMG? Explain its purpose.**

Answer:  
TMG (Table Maintenance Generator) is used to generate maintenance screens for database tables so that users can insert, update, and delete table data easily without writing a program.

---

**Q90. How to create a table in ABAP (step-by-step)?**

Answer:  
Go to Transaction SE11  
Select Database Table  
Enter Table Name  
Define Fields and Data Elements  
Set Primary Key  
Maintain Technical Settings  
Activate the table  

---

## 🔹 2. Report Techniques (Core ABAP)

### Basic Reporting

**Q29. What is the default event in a report?**

Answer:  
The default event in an ABAP report program is START-OF-SELECTION. It is automatically triggered when the user executes the report.

---

**Q30. How do you provide a default value to a selection screen?**

Answer:  
We can provide default values using the DEFAULT keyword in the parameter.  

Example:  
PARAMETERS p_name TYPE string DEFAULT 'SAP'.

---

**Q33. Classical Views vs ALV Views**

Classical Report               |        ALV Report  
Uses WRITE statements          |       Uses ALV classes/function modules  
Less interactive               |       Highly interactive  
No sorting/filtering           |       Sorting, filtering, export available  
Simple output                  |       Structured grid output  

---

**Q85. What is the basic syntax of a report?**

Example:  
```abap
REPORT zsample_report.  
DATA: lv_text TYPE string VALUE 'Hello SAP'.  

START-OF-SELECTION.  
WRITE: lv_text.  

```
Explanation:  
• REPORT → Program name  
• DATA → Variable declaration  
• START-OF-SELECTION → Main execution block  
• WRITE → Display output  

---

**Q93. How did you create a report to display data?**

Answer:  
The process to create a report:  

1. Create a program in SE38  
2. Define selection screen parameters  
3. Fetch data from database using SELECT statement  
4. Store data in internal table  
5. Display output using WRITE statement or ALV report  

---

**Q149. How to extract a particular row or all rows from a table in SE38?**

Answer:  

To extract all rows:  
```abap
SELECT * FROM table_name INTO TABLE it_tab.  
```
To extract a particular row:  
```abap
SELECT * FROM table_name  
WHERE field = value  
INTO TABLE it_tab.  
```
This code is written in SE38 (ABAP report program).

---

### Selection Screen

**Q28. How to create a Dynamic Selection Screen?**

Answer:  
Dynamic selection screens are created using MODIF ID and AT SELECTION-SCREEN OUTPUT event.  
We control field visibility or activation dynamically based on user input.  

Example concept:  
```abap
AT SELECTION-SCREEN OUTPUT.  
LOOP AT SCREEN.  
IF screen-group1 = 'A'.  
screen-active = 0.  
MODIFY SCREEN.  
ENDIF.  
ENDLOOP.  
```
---

**Q62. Which event is used to validate the input for Select-Options field?**

Answer:  
The event used is AT SELECTION-SCREEN.  
It is used to validate user input before the report execution.  

Example:  
```abap
AT SELECTION-SCREEN.  
IF s_date IS INITIAL.  
  MESSAGE 'Please enter date' TYPE 'E'.  
ENDIF.  
```
---

**Q63. Difference between AT SELECTION-SCREEN and AT SELECTION-SCREEN OUTPUT**

AT SELECTION-SCREEN                    |   AT SELECTION-SCREEN OUTPUT  
Used for validation                    |   Used to modify selection screen dynamically  
Triggered when user presses execute    |   Triggered before the screen is displayed  
Used for error messages                |   Used for enabling/disabling fields  

---

**Q102. How does RADIOBUTTON GROUP control logic flow?**

Answer:  
Radio buttons grouped together allow the user to select only one option at a time.  
Based on the selected radio button, we can control the program logic using IF conditions.  

Example:  
```abap
IF r1 = 'X'.  
  WRITE 'Option 1 Selected'.  
ENDIF.  
```
---

**Q104. Why did you use LOOP AT SCREEN?**

Answer:  
LOOP AT SCREEN is used to dynamically modify screen fields such as enabling, disabling, hiding, or making fields mandatory based on conditions.

---

**Q126. How do you design a selection screen using PARAMETERS and SELECT-OPTIONS?**

Answer:  
A selection screen allows the user to enter input before running a report.  

Example:  
```abap
PARAMETERS: p_name TYPE string.  

SELECT-OPTIONS: s_date FOR sy-datum.  
```
• PARAMETERS → Single value input  
• SELECT-OPTIONS → Range input (multiple values)  

---

### Events

**Q61. Explain all the Classical Report Events**

Answer:  

• INITIALIZATION – Triggered when the program loads  
• AT SELECTION-SCREEN – Triggered when the user interacts with the selection screen  
• START-OF-SELECTION – Main processing event  
• END-OF-SELECTION – Executed after data processing  
• TOP-OF-PAGE – Prints header in list output  
• END-OF-PAGE – Prints footer in list output  

---

## 🔹 3. Debugging Techniques

**Q14. What is SY-SUBRC?**

Answer:  
SY-SUBRC is a system field that stores the return code of the last executed statement.  
If the value is 0, the operation was successful; otherwise, it indicates an error or different condition.

---

**Q23. User says report is giving wrong total amount. How will you debug?**

Answer:  
First, I will reproduce the issue and debug the program using breakpoints.  

Then I will check:  
• Data fetched from the database  
• Calculation logic  
• Internal table values  
• ALV field catalog configuration  

---

**Q124. What is Debugging?**

Answer:  
Debugging is the process of identifying and fixing errors (bugs) in a program.  
In SAP ABAP, debugging is done using the ABAP Debugger by placing breakpoints or watchpoints to analyze program execution step by step.

---

## 🔹 4. Modularization Techniques

**Q88. What do you mean by Modularization?**

Answer:  
Modularization means dividing a large program into smaller reusable modules to improve readability, maintenance and reusability.  

Examples in ABAP:  

• FORM routines  
• Function Modules  
• Methods  
• Subroutines  

---

**Q98. What are Function Modules?**

Answer:  
A Function Module is a reusable procedure stored in a Function Group.  
It can be called from different programs and is used for modular programming and code reuse.  

Example:
```abap
CALL FUNCTION 'FUNCTION_NAME'.  
```
---

**Q99. What are different types of ABAP programs?**

Answer:  

Main types:  

1. Executable Programs (Reports)  
2. Module Pool Programs (Dialog programs)  
3. Function Group Programs  
4. Class Pools (OO ABAP)  
5. Interface Pools  

---

## 🔹 5. Miscellaneous Concepts

**Q12. What is a TR Number?**

Answer:  
A TR (Transport Request) Number is used to transport development objects from one SAP system to another system, such as Development → Quality → Production.

---

**Q31. What is Buffering?**

Answer:  
Buffering is a technique used to store frequently accessed table data in the application server memory to improve performance and reduce database access.

---

**Q135. How do you optimize ABAP code?**

Answer:  

Some optimization techniques:  

• Use JOIN instead of nested SELECT  
• Avoid SELECT inside loops  
• Use FOR ALL ENTRIES  
• Use proper indexes  
• Use hashed or sorted tables  

---

**Q130. What is Work Process Allocation?**

Answer:  
In SAP architecture, Work Processes execute user requests.  

Types include:  
• Dialog Work Process  
• Update Work Process  
• Background Work Process  
• Spool Work Process  
• Enqueue Work Process  

---

## 🔹 6. Dialog Programming (Module Pool)

**Q100. What is a Module Pool Program?**

Answer:  
A Module Pool Program is used to create dialog-based applications with screens in SAP.  
It uses screen flow logic, PBO (Process Before Output), and PAI (Process After Input) to handle user interaction.

---

**Q102. How does RADIOBUTTON GROUP control logic flow?**

Answer:  
Radio buttons grouped together allow the user to select only one option at a time.  
Based on the selected radio button, we can control the program logic using IF conditions.  

Example:  

```abap
IF r1 = 'X'.  
  WRITE 'Option 1 Selected'.  
ENDIF.
```
