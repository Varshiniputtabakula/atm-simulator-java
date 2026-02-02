# 🏧 ATM-SIMULATOR

ATM-SIMULATOR is a **JavaFX-based desktop application** that simulates real-world ATM banking operations such as secure login, account management, balance inquiry, deposits, withdrawals, and transaction history tracking.

The system is backed by a **MySQL database** and follows a **controller-driven architecture**, ensuring data consistency, session control, and reliable transaction processing.

This project is intended for **academic evaluation, viva demonstrations, and portfolio presentation**.

---

## 🚀 Features

- Card Number & PIN–based authentication  
- Create new bank accounts  
- Balance inquiry  
- Cash deposit and withdrawal with validation  
- Transaction history logging  
- Profile management (PIN reset)  
- Session-based access control  
- Persistent storage using MySQL  

---

## 🏗️ Project Structure

```text
ATM_FINAL/
│
├── src/
│   └── application/
│       ├── Main.java
│       ├── ATMController.java
│       ├── CreateAccountController.java
│       ├── DashboardController.java
│       ├── LoginController.java
│       ├── ProfileController.java
│       ├── SetPasswordController.java
│       ├── TransactionController.java
│       ├── DBConnection.java
│       ├── DBTransaction.java
│       ├── SessionManager.java
│       ├── atm.fxml
│       ├── create_account.fxml
│       ├── dashboard.fxml
│       ├── login.fxml
│       ├── profile.fxml
│       ├── set_password.fxml
│       └── transaction.fxml
│
├── bin/
│   └── application/
│       ├── Main.class
│       ├── ATMController.class
│       ├── CreateAccountController.class
│       ├── DashboardController.class
│       ├── LoginController.class
│       ├── ProfileController.class
│       ├── SetPasswordController.class
│       ├── TransactionController.class
│       ├── DBConnection.class
│       ├── DBTransaction.class
│       └── SessionManager.class
│
├── lib/
│   ├── javafx.base.jar
│   ├── javafx.controls.jar
│   ├── javafx.fxml.jar
│   ├── javafx.graphics.jar
│   ├── javafx.media.jar
│   ├── javafx.swing.jar
│   ├── javafx.web.jar
│   └── mysql-connector-j-9.2.0.jar
│
├── database/
│   ├── atm_db_setup.sql
│   └── update_schema.sql
│
├── .gitignore
└── README.md
🔐 Authentication & Session Handling
Users authenticate using Card Number + PIN

Credentials are verified against the database

Active sessions are managed using a SessionManager

Unauthorized access is blocked at the controller level

🔁 Transaction Flow
User Authentication

Session Initialization

Operation Selection (Deposit / Withdraw / Balance / Profile)

Business Rule Validation

Database Update via JDBC

Transaction Logging

UI Feedback to User

🗄️ Database Design
accounts Table
Column Name	Description
id	Primary key
card_number	Unique card identifier
pin	User PIN
balance	Account balance

transactions Table
Column Name	Description
id	Primary key
card_number	Account reference
transaction_type	Deposit / Withdrawal
amount	Transaction amount
timestamp	Date & time

🛠️ Tech Stack
Language: Java

UI: JavaFX, FXML

Backend Logic: Java Controllers

Database: MySQL

Connectivity: JDBC

IDE: VS Code / IntelliJ IDEA

⚙️ Local Installation
bash
Copy code
git clone <repository-url>
cd ATM_FINAL
Import the project into your IDE

Configure JavaFX libraries

Set up MySQL using database/atm_db_setup.sql

Update database credentials in DBConnection.java

Run Main.java

🧪 Testing
Login validation testing

Insufficient balance handling

Transaction history verification

Session expiry and logout handling

📌 Use Case & Learning Outcomes
Real-world ATM transaction simulation

Secure authentication workflows

Database-backed JavaFX applications

MVC-style controller separation

Practical JDBC & MySQL integration

⚠️ Disclaimer
This project is intended for educational and demonstration purposes only.
It is not designed for production banking environments.

👩‍💻 Author
Varshini Puttabakula
Data Science & Machine Learning | Java | Software Engineering
