# Complete-Meditation

# CERN Experiment Database

## Description
To create an API for a CERN experiment database – designed to allow users connected with CERN to login into a system with upload and download experiment data functionality with constrictions on access based on user privilege; the learning outcome from the project was to demonstrate Secure Software Development (SSD) based on the OWASP top ten security vulnerabilities. 
## 1. Implementation
The CERN experiment database API was programmed in Python3, utilizing Python SQLite3 module to interact with SQLite databases and with Flask providing the framework to connected each module. Code written in IDE's Visual code studio and PyCharm.
## 2. Architecture 
We have used Flask to build a web application microservice. 
## 3. Features
### User funtionality
* User menu (command line input)
* Sign up/login
  
Sign up and login steps take apropriate inpurs to create a user account 
or to allow for access to the database respectively. These functionalities
are implemented by `log_in()` and `sing_up` functions in `Input_checker.py` file.
* Upload/download (experiment data)
### Security Features
Selected to demostrate SSD and based on the OWASP top ten security vulnerabilities this project incoporates the following security features.
* Authentication
  
Authentication part of the software ensures that only authorized individuals 
have access to the system. In our implementation, during the login step 
(`log_in()` in `Inpur_chekre.py`), a user provides their username and password. 
These data are also stored in the database. The application uses a hashing 
algorithm (`hashing()` in `Authentication_checker.py`) on the input-password and
compares it with a hashed password stored in the database (search takes place 
based on username as a primary key). If these two passwords are the same, then 
logging-in is successful and `log_in()` returns a user object.

* Hashing  
  
For authentication, we used built-in hashlib library to protect the password by 
SHA-2 cryptographic hash function that transforms each password with a random 
length into a sequence 256 bits and all secured hashed passwords will be stored
in the database.

* Data encryption
* Parametrised Queries

Parametrised queries seperate the data from the SQL statement to be compliled. As the query is translated placeholders `("?")`  will be used instead of parameters (column value) and the parameter value would be supplied at the time of execution. For example ; `(name, format, subject) VALUES(?, ?, ?)`. This helps prevent SQL injection attacks where actors inject malicious code to try change the intention of the query.

* Authorisation
## 4. Installation
### Dependencies 
The programme requirements :
* Python 3.10
* Flask 2.2.2 
### How to run
Description of how to run the file
## 5. Structure
Display a directory diagram
## 6. Project files
list of file and brief Description of functionality
* `Encryptor.py`
* `client.py`
* `database_cern.py`
* `flask_cert.pem`
* `flask_private-key.pem`
* `plaeholder.txt`
* `requirements.txt`
* `server.py`
* `session.py`
* `Authentication.py`
* `Authentication_checker.py`
* `Classes.py`
* `Input_checker.py`
* `database.py`
* `database_file.db`
* `database_managment.py`
* `main.py`
* `AuthorisationDataBase.py`
* `authorisation.py`
* `crud.py`
* `crud_server.py`
* `db_and_table.py`

## 7. Tests
Mention all the different tests performed with code examples
## 8. How to Use
Simple step by step guide to how to use the app. How to sign up , login in , upload a file encryption
## 9. References
Great Learning Team (2021). README File – Everything you Need to Know [online] Available from:
https://www.mygreatlearning.com/blog/readme-file/ [accessed 28th August 2022]

Pynative.com (2021). Python MySQL Execute Parameterized Query using Prepared Statement. [online] Available from:
https://pynative.com/python-mysql-execute-parameterized-query-using-prepared-statement/
