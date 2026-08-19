# practical_3
Student Database Management System — README

Overview

This SQL project creates a simple Student Database Management System. It stores information about departments, students, courses, enrollments, and faculty members.

The database demonstrates important SQL concepts such as:

- Primary Keys
- Foreign Keys
- Unique Constraints
- NOT NULL Constraints
- CHECK Constraints
- Table relationships
- INSERT and SELECT operations

Database Tables

1. "department"

Stores information about different departments.

Column| Description
"dept_id"| Unique department ID
"dept_name"| Department name

"dept_id" is the Primary Key, while "dept_name" must be unique and not null.

2. "student"

Stores student details.

Column| Description
"roll_no"| Unique student roll number
"name"| Student name
"email"| Student email
"aadhar_no"| Student Aadhaar number
"dept_id"| Department associated with the student

"roll_no" is the Primary Key. "email" and "aadhar_no" are unique. "dept_id" is a Foreign Key referencing "department".

3. "course"

Stores information about courses offered by departments.

Column| Description
"course_id"| Unique course ID
"course_name"| Name of the course
"dept_id"| Department offering the course

"course_id" is the Primary Key and "dept_id" references the "department" table.

4. "enrollment"

Stores the courses taken by students.

Column| Description
"roll_no"| Student roll number
"course_id"| Course ID
"semester"| Semester in which the course is taken
"grade"| Grade obtained

The combination of "roll_no", "course_id", and "semester" forms a Composite Primary Key.

The "semester" value is restricted to 1 through 8 using a CHECK constraint.

5. "faculty"

Stores faculty information.

Column| Description
"faculty_id"| Unique faculty ID
"faculty_name"| Faculty member's name
"email"| Faculty email
"phone_no"| Faculty phone number
"dept_id"| Department associated with the faculty

"faculty_id" is the Primary Key. "email" and "phone_no" are unique, and "dept_id" references the "department" table.

Relationships

The database has the following relationships:

- One department can have many students.
- One department can offer many courses.
- One department can have many faculty members.
- A student can enroll in multiple courses.
- A course can have multiple students.
- The "enrollment" table connects students and courses.

Relationship Structure

"Department → Student"

"Department → Course"

"Department → Faculty"

"Student → Enrollment ← Course"

Sample Data

The database contains:

- 3 departments
- 3 students
- 3 courses
- 4 enrollment records
- 3 faculty members

How to Run

1. Open a MySQL-compatible SQL environment.
2. Run the "CREATE TABLE" statements first.
3. Insert the department records.
4. Insert student, course, enrollment, and faculty records.
5. Run the "SELECT * FROM ..." statements to verify the inserted data.

Purpose

This project is useful for understanding relational database design, constraints, primary and foreign keys, and relationships between multiple tables using SQL.
