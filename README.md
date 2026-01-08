💰 Serverless Expense Tracker

A cloud-based serverless web application to track daily expenses using AWS Lambda, API Gateway, DynamoDB, and S3.
This project demonstrates CRUD operations, REST APIs, serverless architecture, and frontend–backend integration.

🚀 Features

➕ Add a new expense

🔍 Fetch expense details by ID

✏️ Update an existing expense

🗑 Delete an expense

🌐 Fully serverless backend

📦 Secure data storage using DynamoDB

⚡ Fast REST APIs with AWS Lambda & API Gateway

🎨 Simple and responsive UI using HTML, CSS, and JavaScript

🏗 Architecture Overview

Frontend:

HTML, CSS, JavaScript

Hosted on Amazon S3 (Static Website Hosting)

Backend:

AWS Lambda (Python) – Business logic

Amazon API Gateway – REST API endpoints

Amazon DynamoDB – Expense data storage

AWS IAM – Role-based access control

Testing:

APIs tested using Postman

🛠 Tech Stack
Layer	Technology
Frontend	HTML, CSS, JavaScript
Backend	AWS Lambda (Python)
Database	Amazon DynamoDB
API	Amazon API Gateway
Hosting	Amazon S3
Security	AWS IAM
Testing	Postman
📁 Project Structure
serverless-expense-tracker/
│
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
├── lambda/
│   └── ExpenseLambda.py
│
└── README.md

🔧 Setup & Deployment Steps
1️⃣ Create DynamoDB Table

Table Name: Expenses

Partition Key:

expense_id (String)

2️⃣ Create AWS Lambda Function

Runtime: Python 3.x

Function Name: ExpenseLambda

Handles:

POST → Create Expense

GET → Read Expense

PUT → Update Expense

DELETE → Delete Expense

3️⃣ Create REST API (API Gateway)

API Type: REST API

Resource: /expense

Methods:

POST, GET, PUT, DELETE, OPTIONS

Enable:

Lambda Proxy Integration

CORS

4️⃣ IAM Role for Lambda

Attach the following policies:

AmazonDynamoDBFullAccess

AWSLambdaBasicExecutionRole

5️⃣ Frontend Setup

Create a simple UI using HTML, CSS, and JavaScript

Configure API endpoint in script.js

const API_URL = "https://<your-api-id>.execute-api.<region>.amazonaws.com/prod/expense";

6️⃣ Deploy Frontend on S3

Create S3 bucket

Upload:

index.html

style.css

script.js

Enable static website hosting

📌 API Endpoints
Method	Endpoint	Description
POST	/expense	Add a new expense
GET	/expense?expense_id=ID	Get expense by ID
PUT	/expense	Update an expense
DELETE	/expense?expense_id=ID	Delete an expense
🧪 API Testing

APIs were tested using Postman

Verified request/response handling for all CRUD operations

🎯 Learning Outcomes

Hands-on experience with AWS Serverless Architecture

Building REST APIs using Lambda & API Gateway

Data modeling with DynamoDB

Hosting static websites on Amazon S3

IAM role and permission management

Frontend–backend integration
