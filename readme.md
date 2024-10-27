# Project Overview
This project demonstrates how to set up an AWS environment to host and run applications with data storage and retrieval capabilities. The focus is on building a backend application with MySQL, using EC2 for compute, RDS for database storage, S3 for object storage, and IAM for managing permissions.

### Project Components
EC2 Instance Setup for Hosting:
Launch an EC2 instance to serve as the application server. Connect via SSH to configure the server.

### 1. Update System 

```bash
sudo apt-get update
```
### 2. Install MySQL Client on the EC2 instance
```bash
sudo apt-get install mysql-client 
```
### 3. Connect to RDS and create a database schema for the application
```bash
mysql -h <rds endpoint> -u <username> -p <password>
```
### 4. Create Database and Table
```bash
show databases;
```
```bash
create database employee;
```
```bash
use employee
```
```bash
create table employee(
empid varchar(20),
fname varchar(20),
lname varchar(20),
pri_skill varchar(20),
location varchar(20));
```

### 5.Installed Python environments and related frameworks
```bash
sudo apt-get install python3
```
```bash
sudo apt-get install python3-flask
```
```bash
sudo apt-get install python3-pymysql
```
```bash
sudo apt-get install python3-boto3
```

### 6. For running application
```bash
sudo python3 EmpApp.py
```
### 7. Use S3 for Storage:

Create an S3 bucket to store application data, backups, or other resources.
Configure S3 access in the application code using the boto3 library, allowing the EC2 instance to upload and retrieve data from the bucket.

### 8. IAM Role and Security Setup:
Create an IAM Role for EC2, providing permissions for access to RDS and S3.
Attach Policies that allow access only to the required resources, adhering to the principle of least privilege.

### 9. Testing and Verification:
Verify Database Connection:
Go to your database and check if the data has come in or not.
Access Applications: Test the web applications hosted on the EC2 instance by navigating to the public IP.

# Benefits and Learning Outcomes
This setup introduces learners to a comprehensive AWS deployment pipeline, combining EC2 for hosting, RDS for managed database services, S3 for storage, and IAM for secure access. It also provides experience with both Node.js and Python applications, working with databases, and leveraging AWS tools for real-world scenarios.
