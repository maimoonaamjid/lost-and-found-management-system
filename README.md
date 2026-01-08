# Lost & Found Item Management System (Java + MySQL)

A database-driven Lost & Found Management System developed using Java Swing and MySQL. The system allows administrators to register found items, manage claims, search items, update status, and maintain logs. It aims to digitize lost & found processes for institutions such as schools, colleges, and offices.

---

## 🚀 Key Features

✔ Add Found / Lost Items  
✔ Search Items by Name or Category  
✔ Manage Item Claims  
✔ Approve or Reject Claims  
✔ Track Item Status (Found → Pending → Returned)  
✔ Secure Database Storage (MySQL)  
✔ Logs for Status Updates & Claims  
✔ Java Swing Desktop UI  
✔ JDBC-based Backend Connectivity  

---

## 🧱 Tech Stack

**Frontend**
- Java Swing
- Java AWT
- JPanel, JTable, JTextField, JComboBox, Dialogs

**Backend Logic**
- Java OOP + Event-Driven Programming
- JDBC (Java Database Connectivity)

**Database**
- MySQL
- Stored Procedures
- Triggers
- Foreign Keys
- CRUD Operations

**Tools Used**
- NetBeans / IntelliJ
- MySQL Workbench / XAMPP
- MySQL Connector/J
- Draw.io (Diagrams)
- VS Code / Word / PPT (Docs)

---

## 📦 System Modules

| Module | Purpose |
|---|---|
| Found Item Module | Register lost/found items |
| Claim Module | Submit & verify claims |
| Status Module | Track returned or pending items |
| Search Module | Query by keyword/category |
| Database Module | Handle CRUD, triggers & logs |
| UI Module | Java Swing interface |

---

## 🛢 Database Schema

### **Tables**

#### `users`
| Field | Type | Key |
|---|---|---|
| user_id | INT | PK |
| name | VARCHAR(100) | |
| username | VARCHAR(50) | |
| password | VARCHAR(100) | |

#### `items`
| Field | Type | Key |
|---|---|---|
| item_id | INT | PK |
| item_name | VARCHAR(100) | |
| category | VARCHAR(50) | |
| description | TEXT | |
| found_date | DATE | |
| found_location | VARCHAR(100) | |
| status | VARCHAR(20) | |

#### `claims`
| Field | Type | Key |
|---|---|---|
| claim_id | INT | PK |
| item_id | INT | FK |
| claimer_name | VARCHAR(100) | |
| claimer_contact | VARCHAR(50) | |
| claim_date | DATE | |
| status | VARCHAR(20) | |

---

## ⚙ Database Logic

**Stored Procedures**
- `add_item` → Insert new item
- `approve_claim` → Handle approval + status update

**Triggers**
- `claim_submit_trigger` → Auto status: Pending
- `status_update_trigger` → Log status changes

---

## 🖥 Screens & Interface (Java)

✔ Dashboard  
✔ Add Item Screen  
✔ View Items Table  
✔ Claim Item Form  
✔ Status Update Dialog  
✔ Logs & Approval Screen  

---

## 🔧 How to Run

### **Requirements**
- JDK 8+
- MySQL Server
- MySQL Connector/J (JDBC)
- IDE (NetBeans/IntelliJ/Eclipse)

### **Steps**
1. Clone or Download Repo
2. Import SQL script into MySQL
3. Update DB credentials in Java code:
```java
Connection con = DriverManager.getConnection(
 "jdbc:mysql://localhost:3306/lost_found", "root", ""
);
