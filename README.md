# ATBU-PastQuestion Documentation

### Registration and AUthentication API Documentation

### Registration API
## To register new user
POST http://localhost:8080/api/v1/auth/register

{
  "id": 0,
  "first_name": "",
  "last_name": "",
  "email": "",
  "phone_number": "",
  "faculty": "",
  "password": ""
}

## To Authenticate USer
### Authentication API

POST http://localhost:8080/api/v1/auth/authenticate
{
  "email": "",
  "password": ""
}

## To test the authorized  users on apllication with demo to return status 201:ok

GET http://localhost:8080/api/v1/demo-controller

### Course API Documentation
#### Get all Courses
GET http://localhost:8080/api/courses

#### Get Course by ID
GET http://localhost:8080/api/course/{{courseId}}

Example: Get the course by ID number 5
GET http://localhost:8080/api/course/5

#### Add a New Course
POST http://localhost:8080/api/course

Request Body:
{
  "id": 20,
  "code": "CSE419",
  "department": {
    "id": 32,
    "departmentName": "Department of Computer & Communication"
  },
  "questions": []
}

#### Update Course Code by ID
PUT http://localhost:8080/api/course/{{courseId}}

Example: Update course code for ID number 2
PUT http://localhost:8080/api/course/2

Request Body:
{
  "id": 2,
  "code": "(AEE101)",
  "department": {
    "id": 2,
    "departmentName": "Department of Agricultural Extension and Rural Development",
    "courses": []
  },
  "questions": []
}
#### Delete Course by ID
DELETE http://localhost:8080/api/course/{{courseId}}

Example: Delete a course by ID number 6
DELETE http://localhost:8080/api/course/6

This documentation provides a clear understanding of the Course API endpoints and how to interact with them, including examples for each operation.


### Department API Documentation

###### Get all Departments
GET http://localhost:8080/api/department/departments

###### Get Department by ID
GET http://localhost:8080/api/department/{{departmentId}}

Example: Get the department by ID number 3
GET http://localhost:8080/api/department/3

###### Create a New Department
POST http://localhost:8080/api/department
Request Body:
{
  "id": 39,
  "departmentName": "Department of Sociology",
  "courses": []
}

###### Delete Department by ID
DELETE http://localhost:8080/api/department/{{departmentId}}

Example: Delete a department by ID number 39
DELETE http://localhost:8080/api/department/39

###### Update Department by ID
PUT http://localhost:8080/api/department/{{departmentId}}

Example: Update department ID number 32
PUT http://localhost:8080/api/department/32
Content-Type: application/json

Request Body:
{
  "id": 32,
  "departmentName": "Department of Agricultural Extension and Rural Developmentss"
}
This documentation provides clear instructions on how to interact with the Department API endpoints, including examples for each operation.

### Question API Documentation

###### Get all Questions
GET http://localhost:8080/api/question/questions

###### Get Question by ID
GET http://localhost:8080/api/question/{{questionId}}

Example: Get the question by ID number 14
GET http://localhost:8080/api/question/14

###### Delete Question by ID
DELETE http://localhost:8080/api/question/{{questionId}}
DELETE http://localhost:8080/api/question/18

###### Retrieve Questions by Course ID
GET http://localhost:8080/api/question/course/{{courseId}}

Example: Retrieve all questions that belong to course ID number 22
GET http://localhost:8080/api/question/course/22

###### Update Question by ID
PUT http://localhost:8080/api/question/{{questionId}}

Example: Update any question by ID number 21
PUT http://localhost:8080/api/question/21

Request Body:
{
  "text": "Your question text here"
}
###### Delete Question by ID
DELETE http://localhost:8080/api/question/{{questionId}}

Example: Delete a question by ID number 23
DELETE http://localhost:8080/api/question/23

###### Create a New Question
POST http://localhost:8080/api/question

Request Body:
text=Your%20question%20text%20here&courseId=22


This documentation provides a clear overview of the available endpoints, their functionalities, and examples of how to use them.

