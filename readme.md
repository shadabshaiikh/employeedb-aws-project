### 1. Update System 

```bash
sudo apt-get update
```
### 2.install Sql-client
```bash
sudo apt-get install mysql-client 
```
```bash
mysql -h <rds endpoint> -u <username> -p <password>
```

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

### 3.Installed python and related frameworks
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

### 4.for running application
```bash
sudo python3 EmpApp.py
```
