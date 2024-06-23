# Student Database Management System

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [How to Use](#how-to-use)
- [Usage](#usage)
- [Implementation Details](#implementation-details)
- [Contributing](#contributing)
- [Authors](#authors)
- [Acknowledgements](#acknowledgements)

## Introduction
The **Student Database Management System** (SDMS) is a robust C++ application designed to manage student records efficiently. It allows for the storage, retrieval, and manipulation of student data, including grades, courses, and personal information. This system was developed collaboratively by Akshara Rathore and Vaibhav Sharma to streamline educational data management for institutions.

## Features
- **Student Management**: Add, remove, and list students.
- **Course Management**: Add and manage courses.
- **Grade Management**: Enter and update marks for various assessments.
- **Reporting**: Generate detailed reports for student performance and course statistics.
- **Data Import**: Import student data from CSV files.
- **Data Export**: Export student data to CSV and TXT files.

## How to use
### Table of Contents
- [Running the Application](#running-the-application)
- [Main Menu Options](#main-menu-options)
- [Adding a New Student](#adding-a-new-student)
- [Adding a New Course](#adding-a-new-course)
- [Entering Marks](#entering-marks)
- [Generating Reports](#generating-reports)

### Running the Application
To get started with the Student Database Management System, follow these steps:

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/itsVaibhavSharma/Student-Database-Management-System.git
    cd Student-Database-Management-System
    ```

2. **Compile the Code**:
    Make sure you have a C++ compiler installed. You can use `g++` to compile the code:
    ```sh
    g++ -o sdms main.cpp
    ```

3. **Run the Application**:
    ```sh
    ./sdms
    ```
After running the application, you will be greeted with a main menu that provides various options to manage student records, courses, and grades.

### Main Menu Options
- **1. Add Student**: Add a new student to the database.
- **2. Remove Student**: Remove an existing student from the database.
- **3. Add Course**: Add a new course to the database.
- **4. Enter Marks**: Enter or update marks for students.
- **5. Generate Reports**: Generate performance reports for students and courses.
- **6. Import Data**: Import student data from a CSV file.
- **7. Exit**: Exit the application.

### Adding a New Student
1. Select **"Add Student"** from the main menu.
2. Enter the student's name.
3. Enter the student's enrollment number.

### Adding a New Course
1. Select **"Add Course"** from the main menu.
2. Enter the course name.
3. Enter the course code.

### Entering Marks
1. Select **"Enter Marks"** from the main menu.
2. Choose the student by entering their enrollment number.
3. Select the course by entering the course code.
4. Enter the marks for each assessment (MidSem1, MidSem2, Proficiency, Quiz/Assignment, EndSem).

### Generating Reports
1. Select **"Generate Reports"** from the main menu.
2. Choose the type of report you want to generate:
    - **Course Average**: Get the average marks for a specific course.
    - **Student Performance**: Get a detailed report of a student's performance across all courses.
3. Follow the prompts to view or save the report.


## Usage
The Student Database Management System (SDMS) is a versatile tool designed to cater to various needs within educational institutions. Below are the key uses of this system:

### Student Management
- **Add New Students**: Easily add new student records to the database, including personal details and enrollment information.
- **Remove Students**: Remove students from the database when they graduate or leave the institution.
- **Update Student Information**: Modify existing student details as needed.

### Course Management
- **Add New Courses**: Introduce new courses into the system with all relevant details such as course name and code.
- **Remove Courses**: Remove outdated or obsolete courses from the database.
- **Update Course Information**: Make changes to course details as required.

### Grade Management
- **Enter Assessment Marks**: Record marks for various assessments including MidSem1, MidSem2, Proficiency, Quiz/Assignment, and EndSem exams.
- **Update Marks**: Update or correct marks for any assessment.
- **Automated Grade Calculation**: Automatically calculate total marks and grades based on the entered assessment marks.

### Performance Reporting
- **Generate Student Performance Reports**: Create detailed reports on individual student performance across all enrolled courses.
- **Course Statistics Reports**: Generate statistical reports on course performance, including average marks and grade distributions.
- **Customizable Reports**: Customize the reports based on specific criteria to meet various administrative needs.

### Data Import and Export
- **Import Student Data**: Import student records from CSV files to quickly populate the database.
- **Export Data**: Export student data, course information, and performance reports for use in other applications or for archival purposes.

### Administrative Efficiency
- **Centralized Database**: Maintain a centralized database of all student records and course information, facilitating easy access and management.
- **Error Handling**: Robust error handling ensures smooth operation and user-friendly interaction.
- **User-Friendly Interface**: Intuitive menu-driven interface simplifies navigation and reduces the learning curve for new users.

### Academic Analysis
- **Track Academic Progress**: Monitor and track the academic progress of students throughout their course of study.
- **Identify Trends**: Analyze performance trends over time to identify areas needing improvement.
- **Support Academic Decisions**: Use data-driven insights to support academic decisions and policy-making.

### Scalability
- **Support for Multiple Semesters**: Manage records for multiple semesters, allowing for continuous tracking of student performance over their academic career.
- **Extendable Architecture**: The system’s architecture allows for future enhancements and scalability to meet growing needs.

### Security and Integrity
- **Data Integrity**: Ensure the integrity and accuracy of student records through consistent validation checks.
- **Confidentiality**: Maintain the confidentiality of student data with secure handling and storage practices.


## Implementation Details

### Table of Contents
- [Project Structure](#project-structure)
- [Class Descriptions](#class-descriptions)
- [Data Storage](#data-storage)
- [Mark Calculation](#mark-calculation)
- [Error Handling](#error-handling)
- [Future Enhancements](#future-enhancements)

### Project Structure
The Student Database Management System is organized into several key files and directories:

- **main.cpp**: The entry point of the application.
- **student.h / student.cpp**: Contains the `Student` class definition and implementation.
- **course.h / course.cpp**: Contains the `Course` class definition and implementation.
- **semester.h / semester.cpp**: Contains the `Semester` class definition and implementation.
- **utils.h / utils.cpp**: Utility functions and helpers.

### Class Descriptions
#### Class: `Course`
- **Attributes**:
    - `string Cname`: The name of the course.
    - `string Ccode`: The course code.
    - `int midsem1`: Marks for MidSem1.
    - `int midsem2`: Marks for MidSem2.
    - `int proficiency`: Marks for proficiency tests.
    - `int endsem`: Marks for the EndSem exam.
    - `int quizAssignment`: Marks for quizzes and assignments.
- **Methods**:
    - `void updateMid1(int m)`: Update MidSem1 marks.
    - `void updateMid2(int m)`: Update MidSem2 marks.
    - `void updateproficiency(int m)`: Update proficiency marks.
    - `void updateEndSem(int m)`: Update EndSem marks.
    - `void updateQA(int m)`: Update quiz/assignment marks.
    - `int getMid1()`: Get MidSem1 marks.
    - `int getMid2()`: Get MidSem2 marks.
    - `int getProf()`: Get proficiency marks.
    - `int getEndsem()`: Get EndSem marks.
    - `int getQA()`: Get quiz/assignment marks.
    - `double getCourseMarks()`: Calculate total course marks.
    - `string getCourseGrade()`: Calculate the course grade.

#### Class: `Student`
- **Attributes**:
    - `string name`: The name of the student.
    - `string enrol`: The enrollment number.
    - `vector<Course> course`: List of courses the student is enrolled in.
    - `double CGPA`: The calculated CGPA of the student.
- **Methods**:
    - `Student(string n, string e)`: Constructor to initialize student details.
    - `void calCGPA()`: Calculate and update the CGPA of the student.

#### Class: `Semester`
- **Attributes**:
    - `vector<Student> student`: List of students in the semester.
    - `vector<Course> course`: List of courses offered in the semester.
- **Methods**:
    - `void addStudent(string name, string enrol)`: Add a new student.
    - `void importStudent(string fname)`: Import students from a CSV file.
    - `void MidSem1(string Ccode)`: Enter MidSem1 marks for a course.
    - `void MidSem2(string Ccode)`: Enter MidSem2 marks for a course.
    - `void Proficiency(string Ccode)`: Enter proficiency marks for a course.
    - `void EndSem(string Ccode)`: Enter EndSem marks for a course.
    - `void QuizAssignment(string Ccode)`: Enter quiz/assignment marks for a course.
    - `void addCourse()`: Add a new course.
    - `void removeStudent(string enrol)`: Remove a student.
    - `void printStList()`: Print the list of students.
    - `void printMarks(string Ccode)`: Print marks for a course.

### Data Storage
Data is stored in memory using standard C++ containers such as `vector`. Each student and course is represented as an object, and their details are stored as attributes within these objects.

### Mark Calculation
Marks for each course are entered and updated using dedicated methods in the `Course` class. The total marks for a course are calculated by summing the marks for all assessments. The `getCourseGrade` method computes the grade based on the total marks.

The `Student` class calculates the CGPA by averaging the grades of all courses a student is enrolled in.

### Error Handling
The application includes robust error handling to manage invalid inputs and operations. This ensures the system remains stable and provides meaningful feedback to users.

### Future Enhancements
- **Database Integration**: Integrate with a database to store and retrieve data persistently.
- **Web Interface**: Develop a web-based interface for remote access and management.
- **Enhanced Reporting**: Add more customizable reporting features.
- **User Authentication**: Implement user authentication and authorization.

## Special Features

### Table of Contents
- [Introduction](#introduction)
- [Student Management](#student-management)
- [Course Management](#course-management)
- [Grade Management](#grade-management)
- [Reporting System](#reporting-system)
- [Data Import](#data-import)
- [User-Friendly Interface](#user-friendly-interface)

### Introduction
The Student Database Management System (SDMS) is packed with several special features that make it a powerful tool for educational institutions. These features ensure efficient data management, easy accessibility, and comprehensive reporting.

### Student Management
- **Add/Remove Students**: Easily add new students or remove existing ones from the database.
- **Detailed Student Records**: Maintain detailed records of students, including their personal information and academic performance.

### Course Management
- **Add/Remove Courses**: Add new courses or remove outdated ones.
- **Course Details**: Store comprehensive details about each course, including course code and name.

### Grade Management
- **Enter/Update Marks**: Enter and update marks for various assessments such as MidSem1, MidSem2, Proficiency, Quiz/Assignment, and EndSem.
- **Automated Grade Calculation**: Automatically calculate grades based on entered marks.

### Reporting System
- **Performance Reports**: Generate detailed performance reports for individual students.
- **Course Statistics**: Obtain statistical data for courses, including average marks and grade distributions.
- **Customizable Reports**: Customize the reports based on specific criteria and requirements.

### Data Import
- **CSV Import**: Import student data from CSV files, making it easy to populate the database with existing records.
- **Bulk Import**: Import data for multiple students and courses at once, saving time and effort.

### User-Friendly Interface
- **Intuitive Menu System**: Navigate through the application with ease using the intuitive menu system.
- **Clear Prompts**: Clear and concise prompts guide users through each operation, reducing the learning curve.
- **Error Handling**: Robust error handling ensures the application runs smoothly and handles invalid inputs gracefully.

## Contributing
We welcome contributions to enhance the Student Database Management System. To contribute, follow these steps:

1. **Fork the Repository**: Click the "Fork" button on the top right of this page.
2. **Clone Your Fork**:
    ```sh
    git clone https://github.com/itsVaibhavSharma/Student-Database-Management-System.git
    ```
3. **Create a Branch**:
    ```sh
    git checkout -b feature-branch
    ```
4. **Make Your Changes**: Implement your changes and commit them with descriptive messages.
5. **Push to Your Fork**:
    ```sh
    git push origin feature-branch
    ```
6. **Create a Pull Request**: Open a pull request on the original repository to merge your changes.

## Authors
- **Akshara Rathore** - [@itsAksharaRathore](https://github.com/itsAksharaRathore)
- **Vaibhav Sharma** - [@itsVaibhavSharma](https://github.com/itsVaibhavSharma)

## Acknowledgements
- We would like to thank our instructors and peers for their support and guidance throughout the development of this project.

