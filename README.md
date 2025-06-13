# 🧠 Research Projects Database

This project is a relational database schema designed to manage and track research projects, their associated employees, and funding agencies. It includes SQL table definitions and data insertion scripts that model a realistic research management environment.

---

## 📘 Overview

The **Research Projects Database** handles:

- Project details: name, manager, duration, budget, and funding agency
- Employee records: SSN, name, salary, and their participation in projects
- Funding agency information: name and address
- Many-to-many relationships between employees and projects
- Identification of project managers (who are also employees)

---

## 🧱 Database Schema

The database consists of the following tables:

1. **Employee**
   - `SSN` (Primary Key)
   - `Emp_Name`
   - `Salary`

2. **FundingAgency**
   - `Agency_ID` (Primary Key)
   - `Name`
   - `Address`

3. **Project**
   - `Project_ID` (Primary Key)
   - `Name`
   - `Duration` (in months)
   - `Budget`

4. **Employee_Project** (Junction Table)
   - Represents the association between employees and projects
   - Also includes the project manager's SSN
   - Composite Primary Key: (`SSN`, `Project_ID`)

5. **Project_Manager**
   - Assigns one manager per project
   - `Project_ID` (Primary Key)
   - `Manager_SSN`

---

## 🔗 Relationships

- Each **project** is funded by a single **agency**.
- Each **project** has a unique name within its **funding agency**.
- Each **project** has **one manager**, who is also an **employee**.
- An **employee** can work on multiple **projects**.
- A **manager** can also participate in the project as a worker.

![image](https://github.com/user-attachments/assets/6b62acb6-3a16-4b0c-9ffe-a51eec67bb9d)


![P2](https://github.com/user-attachments/assets/9664c2e2-62bc-4e0c-8464-4965785a1fcc)





