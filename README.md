# Bank-Management-System.
# 🏦 Bank Management System | C++ OOP

A menu-driven Bank Management System built using C++ and Object-Oriented Programming (OOP) concepts, featuring customer management, savings and current accounts, financial transactions, transaction statements, and persistent file storage.

The project also includes a browser-based banking dashboard built with HTML, CSS, and JavaScript, providing an interactive interface for managing banking operations.

## 📌 Project Overview

The Bank Management System simulates basic banking operations while demonstrating the practical application of object-oriented programming concepts.

It allows users to create customers, open bank accounts, deposit and withdraw money, transfer funds, view account statements, apply monthly account updates, and manage stored records.

The project is designed as an academic mini-project to demonstrate C++ classes, inheritance, polymorphism, encapsulation, abstraction, exception handling, and file handling.

## ✨ Features

- **Customer Management:** Create customers and assign unique customer IDs.
- **Account Management:** Open savings and current accounts with automatically generated account numbers.
- **Deposit:** Add money to an account with transaction recording.
- **Withdrawal:** Withdraw money while enforcing account-specific balance limits.
- **Fund Transfer:** Transfer funds between accounts within the bank.
- **Inter-Bank Transfer:** Transfer funds between supported bank profiles through the web interface.
- **Transaction History:** Record transaction type, amount, timestamp, and resulting balance.
- **Account Statements:** View and print account transaction statements.
- **Savings Account:** Apply monthly interest based on the configured annual interest rate.
- **Current Account:** Support an overdraft limit and monthly maintenance fee.
- **Monthly Account Update:** Apply interest or maintenance fees according to account type.
- **Delete Operations:** Remove accounts, account types, or customers.
- **Dashboard Statistics:** Display customer counts, account counts, and total deposits.
- **Multiple Bank Profiles:** Switch between predefined bank profiles in the web interface.
- **Data Persistence:** Save and reload banking records using text files.
- **Input Validation:** Handle invalid amounts, missing records, and insufficient funds.
- **Interactive UI:** Use a styled web dashboard with light/dark mode support.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| C++ | Core banking logic |
| HTML5 | Web interface structure |
| CSS3 | Dashboard styling and themes |
| JavaScript | Interactive banking interface |
| File Handling | Saving and loading banking records |
| C++ STL | Vectors, strings, and smart pointers |
| Exception Handling | Handling invalid operations and errors |

## 🧠 Object-Oriented Programming Concepts

This project demonstrates the following OOP concepts:

### 1. Classes and Objects
Classes such as `Bank`, `Customer`, `Account`, and `Transaction` represent the main entities of the banking system.

### 2. Encapsulation
Account balances, transaction history, and customer details are managed through class members and public methods.

### 3. Inheritance
`SavingsAccount` and `CurrentAccount` inherit from the base `Account` class. Custom exception classes also inherit from a common banking exception class.

### 4. Runtime Polymorphism
Virtual functions such as `withdraw()`, `monthlyUpdate()`, `type()`, and `display()` allow account-specific behavior to be selected at runtime.

### 5. Abstraction
The `Account` base class defines a common interface for different account types while leaving account-specific behavior to derived classes.

### 6. Function Overriding
Derived account classes override virtual functions to implement their own withdrawal rules and monthly updates.

### 7. Operator Overloading
The `+=` operator is overloaded to support deposit operations in a natural syntax.

### 8. Friend Function and Stream Operator
The `Transaction` class uses an overloaded stream insertion operator to format transaction details.

### 9. Static Members
Static counters generate unique customer and account IDs and track the number of account objects.

### 10. Exception Handling
Custom exceptions handle invalid amounts, insufficient funds, and missing customers or accounts.

## 🏦 Account Types

### Savings Account
- Maintains a configured minimum balance of ₹500.
- Applies a configured annual interest rate of 4%, calculated monthly.
- Records deposits, withdrawals, and interest transactions.

### Current Account
- Supports an overdraft limit of ₹5,000.
- Deducts a configured monthly maintenance fee of ₹100.
- Records account transactions and applies account-specific withdrawal rules.

*These rates and limits are demonstration values defined in the source code, not recommendations for real banking products.*

## 📂 Project Structure

```text
BankSystem/
├── Account.cpp
├── Bank.cpp
├── Customer.cpp
├── CurrentAccount.cpp
├── SavingsAccount.cpp
├── Transaction.cpp
├── Exceptions.cpp
├── FileManager.cpp
├── main.cpp
├── index.html
├── style.css
├── script.js
├── bank_data.txt
├── indian_bank_data.txt
├── national_bank_data.txt
├── titan_bank_data.txt
├── royal_bank_data.txt
├── golden_trust_bank_data.txt
└── vit_bank_data.txt
```

## ⚙️ How to Run the C++ Application

### Prerequisites
- A C++ compiler supporting C++17, such as GCC.
- Visual Studio Code or another C++ development environment.

### Steps

1. Download or clone this repository.
2. Open the `BankSystem` folder in your code editor.
3. Open a terminal in that folder.
4. Compile the program:

   ```bash
   g++ -std=c++17 main.cpp -o bank
   ```

5. Run the executable.

   **Windows:**
   ```bash
   .\bank.exe
   ```

   **Linux/macOS:**
   ```bash
   ./bank
   ```

6. Follow the menu to create customers, open accounts, perform transactions, and view account statements.

The console application loads existing records from `bank_data.txt` and automatically saves data after supported operations.

## 🌐 How to Run the Web Interface

1. Open the `BankSystem` folder.
2. Open `index.html` in a web browser.
3. Explore the dashboard and available banking operations.

The browser interface uses HTML, CSS, JavaScript, and browser storage. Its data workflow is separate from the C++ application's text-file storage unless an explicit integration is implemented.

## 🔮 Future Enhancements

- Integrate the web interface with a C++ backend or REST API.
- Add MySQL database integration.
- Implement authentication and role-based access control.
- Add stronger validation and transaction rollback mechanisms.
- Improve transaction reporting and account search.
- Add automated unit tests.
- Introduce secure password handling and audit logging.

## 👨‍💻 Project Information

**Project Title:** Bank Management System

**Project Type:** C++ OOP Mini-Project

**Author:** Atharv Pawar

**Purpose:** Academic project demonstrating object-oriented programming and basic banking operations.

## 📜 Disclaimer

This is an educational simulation and is not intended for real financial transactions. It does not implement production-grade banking security, authentication, or regulatory compliance.
