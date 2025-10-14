# 💼 Client Query Management System 

## 📖 About the Project

The **Client Query Management System** is a Streamlit web application that enables organizations to collect, track, and resolve client queries efficiently and it is designed to bridge the communication gap between clients and support teams.

### 🔨 Development Process
* Database Setup → Created the Database and tables in MySQL.
* Connection Setup → Configured database connectivity in VS Code using connection mysql.connector.connect with MySQL credentials.
* Prototype Testing → Verified database operations and query handling in a Jupyter Notebook (.ipynb).
* Script Conversion → Migrated the working prototype into a Python script (.py).
* UI Development → Built the Streamlit dashboard 
### ✨ Key Features
* Login and Register interface → new user can register and login 
* 👤 Client Interface → Submit and track queries with details and attachments.
* 🛠️ Support Dashboard → View, filter, and resolve client queries..
### ⚙️ Tech Stack
* Database: MySQL
* Frontend/UI: Streamlit
* Data Handling: Pandas
* Database Connectivity:  mysql-connector-python

## 📋Project Overview
* The Client Query Management (CQMS) provides a seamless way for organizations to handle client issues. Clients can submit their queries with necessary details, and the support team can manage, track, and resolve them in real time.

## 🎯Features:
### 🔐 Login & Register 
#### 📝 User Registration
* Create an account with Username, Email, Password, and Role (Client or Support).
* Prevents duplicate usernames or emails.
* Stores passwords securely using SHA256 hashing.
#### 🔑 User Login
* Login with username and password.
* Verifies password with stored hash for security.
* Maintains session state after successful login.
#### 🎭 Role-Based Access
* Client Role → Can only submit and track their own queries.
* Support Role → Can view, manage, and close all queries.
### 👤 Client Features
* 📝 Submit Queries → Fill details like email, mobile, query heading, description, and can upload screenshots.
* 📂 Track Queries → Search by email and view query history with status (Open/Closed).
* 📸 File Upload Support → Attach screenshots or documents with each query.
* ⏱️ Real-time Status Updates → See when queries are created, updated, or closed
### 👨‍💻 Support Team Features
* 📋 View All Queries → Access every query submitted by clients.
* 🔎 Filter Queries → Filter by status: All, Open, or Closed.
* 🛠️ Manage & Close Queries → Update query status and add closing time.
* 🖼️ Preview Attachments → View uploaded screenshots for better issue understanding.
  
## ⚙️ Setup & Installation
### 1️⃣ Clone the Repository

```
git clone https://github.com/your-username/client-query-management-system.git
cd client-query-management-system
```
### 2️⃣ Create a Virtual Environment & Activate

```
python -m venv venv
# Activate environment
source venv/bin/activate   # (Linux/Mac)
venv\Scripts\activate      # (Windows)

#Install packages
pip install -r requirements.txt
```

#### requirements.txt:
* streamlit
* pandas
* mysql-connector-python

### 3️⃣ Configure MySQL Database 
#### Create Database


```
CREATE DATABASE client_query_db;
USE client_query_db;
```

### 4️⃣ Run the Application
```
streamlit run app.py
```
## 🔑 Sample Users
username	password	Role

support_admin	support123	Support

client_user	client123	Client

## 📊 Dataset
* The project comes with a sample dataset (sample_queries_250.csv) containing 1000 client queries generated for testing purposes.

📂 Dataset Columns:

`email`,`mobile`,`query_heading`,`query_description`

`query_created_time`,`status`,`query_closed_time`

## 🔄 How It Works
1. User Authentication → New user can Register and Login based on role.
2.	Client Side → Client can Submit queries with only Registered Email ID.
3.	Support Side → View & filter queries, update status to Closed with datetime.
4.	MySQL → ensures real-time updates.

## 🎯 Use Case
###### The Client Query Management System helps organizations streamline the process of handling client queries, ensuring faster resolution and better customer experience.
* 🏢 IT Companies → For managing client support tickets and technical issues.
* 🎓 Educational Institutions → To handle student queries, complaints, and feedback.
* 🛠 Service-Based Businesses → For tracking customer complaints, requests, and feedback.
* 🏥 Healthcare Sector → For managing patient inquiries or appointment-related issues.
* 🛒 E-commerce Platforms → To resolve order, delivery, or payment-related queries.

## Future Enhancements
* 📌 Role-Based Dashboards → Separate views for admins, clients, and support staff.
* 📊 Advanced Analytics → Query trends, resolution time tracking, and performance metrics.
* ✉️ Email / SMS Notifications → Notify clients when their queries are updated or resolved.
* 📂 Export Options → Download queries as CSV/Excel for reporting.
