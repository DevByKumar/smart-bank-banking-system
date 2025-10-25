# smart-bank-banking-system

## ✨ Core Features

* **User Onboarding & KYC Verification:** A multi-step registration process where users submit details and KYC documents, which require admin approval before activation.
* **Authentication & Role Management:** It ensures secure login and provides different access permissions for Customers and Admins based on their roles.
* **Customer Dashboard Portal** A central view for customers to see their account details, transaction history, and loan statuses.
* **Admin Control Panel:** A dashboard for admins to approve/reject KYC applications, manage loan requests, and view all user accounts.
* **Loan Management System** A full-cycle loan application process with EMI calculation, form submission, and admin review.

---

## 🔄 Application & User Flows

This project is built on two primary user flows:

### 1. New User Registration & KYC Approval

This flow ensures no user can access the system until they are verified by an admin.

1.  **Customer (Sign Up):** A new user registers by submitting their personal details (name, email, password) and uploading (simulated) KYC documents.
2.  **System:** Creates a new user in the database with a `status: "pending_approval"`.
3.  **Admin (Review):** The admin logs in and sees a list of all "pending" users in their dashboard. They can review the submitted details.
4.  **Admin (Action):** The admin chooses to **Approve (✅)** or **Reject (❌)** the user's application.
5.  **System:** The user's status is updated to `"approved"` or `"rejected"`.
6.  **Customer (Log In):** The user can now log in *only if* their status is `"approved"`.

### 2. Loan Application Flow

This flow allows approved customers to apply for loans, which are then reviewed by an admin.

1.  **Customer (Dashboard):** The customer logs into their dashboard and clicks "Apply for Loan".
2.  **Customer (Form):** They fill out a form with:
    * Loan Type (e.g., Personal, Home)
    * Loan Amount
    * Loan Tenure (in months)
3.  **System:**
    * Validates the form data.
    * Calculates the estimated **EMI** using the formula: `EMI = (P * r * (1 + r)^n) / ((1 + r)^n - 1)`.
    * Saves the application to the database with a `status: "pending"`.
4.  **Admin (Review):** The admin sees a new "pending" loan application in their dashboard.
5.  **Admin (Action):** The admin reviews the application and the customer's profile, then chooses to **Approve (✅)** or **Reject (❌)** the loan.
6.  **Customer (Status):** The customer sees their loan status (e.g., "Approved", "Rejected") updated in their dashboard.

---

## 💻 Tech Stack

* **Backend:** Python (Django)
* **Database:** MYSQL
* **Frontend:** React, JavaScript

-------------------
**commands to run project**

1)Navigate to Project Directory:
```
cd Hackathon\banking
```

2)Install Requirements (
pip install Django Pillow mysqlclient

3)Apply Migrations:
python manage.py makemigrations
python manage.py migrate

4)Create Admin User
python manage.py createsuperuser

5)Run Server:
python manage.py runserver


**Result**
<img width="1884" height="862" alt="image" src="https://github.com/user-attachments/assets/2d356e58-d946-483a-8e6b-f19649df581e" />
<img width="1865" height="606" alt="image" src="https://github.com/user-attachments/assets/54d9e815-6ae4-4a3f-876a-005377a09707" />
<img width="1914" height="781" alt="image" src="https://github.com/user-attachments/assets/67028a30-96f2-406f-b5a3-c9ff31e961f3" />
<img width="1910" height="679" alt="image" src="https://github.com/user-attachments/assets/9c899c52-7927-4bd0-8f67-db21e6e29361" />
<img width="1914" height="759" alt="image" src="https://github.com/user-attachments/assets/d72f4fb3-92b1-4009-bfcc-25275ea30b9a" />
<img width="1915" height="743" alt="image" src="https://github.com/user-attachments/assets/c3f2cecd-8097-44bb-8c9f-1f9f269171b1" />
<img width="1918" height="657" alt="image" src="https://github.com/user-attachments/assets/121f6efb-edd4-4dbb-8291-35e30639ca48" />






