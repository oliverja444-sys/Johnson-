# Johnson Ayomipo Tephilla-
Matric number-24/13909
Computer science 
200level

# Hello World Program

## Description
This is a simple Python program that prints **"Hello World!"** to the console.  
It is commonly used as a beginner’s introduction to programming.

## Code
```python
print("Hello World!")
Requirements
Python 3.x installed on your system
How to Run
Save the code in a file named hello.py
Open a terminal or command prompt
Run the command:

python hello.py
Output

Hello World!
Author
Tephilla Johnson

SEN ASSIGNMENT 2
Project Title: Student Attendance Management System (SAMS)
 PROJECT OVERVIEW
The Student Attendance Management System (SAMS) is a simple software system that allows lecturers to record, view, and manage student attendance digitally instead of using paper registers.
 FULL SOFTWARE DEVELOPMENT LIFE CYCLE (SDLC)
🔹 1. REQUIREMENT ANALYSIS
Functional Requirements
Add a student
Mark student attendance (Present/Absent)
View attendance records
Save attendance data
Non-Functional Requirements
Easy to use
Fast response time
Runs on any computer with Python installed
Tools Used
Programming Language: Python
IDE: VS Code
Version Control: Git & GitHub
🔹 2. SYSTEM DESIGN
System Components
Student: Has student_id and student_name
Attendance: Stores attendance status
AttendanceManager: Controls all operations
Flow of the System
Lecturer runs the program
Chooses an option from the menu
System performs the selected operation
Data is displayed or saved
🔹 3. IMPLEMENTATION (CODING)
📁 Project Folder Structure
Copy code

Student-Attendance-Management-System/
│
├── main.py
├── attendance_manager.py
├── student.py
└── README.md
🧾 student.py
Copy code
Python
class Student:
    def __init__(self, student_id, student_name):
        self.student_id = student_id
        self.student_name = student_name
🧾 attendance_manager.py
Copy code
Python
from student import Student

class AttendanceManager:
    def __init__(self):
        self.students = {}
        self.attendance = {}

    def add_student(self, student_id, student_name):
        student = Student(student_id, student_name)
        self.students[student_id] = student
        print("Student added successfully.")

    def mark_attendance(self, student_id, status):
        if student_id in self.students:
            self.attendance[student_id] = status
            print("Attendance marked.")
        else:
            print("Student not found.")

    def view_attendance(self):
        for student_id, status in self.attendance.items():
            student = self.students[student_id]
            print(f"{student.student_name} ({student.student_id}): {status}")
🧾 main.py
Copy code
Python
from attendance_manager import AttendanceManager

manager = AttendanceManager()

while True:
    print("\nStudent Attendance Management System")
    print("1. Add Student")
    print("2. Mark Attendance")
    print("3. View Attendance")
    print("4. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        student_id = input("Enter Student ID: ")
        student_name = input("Enter Student Name: ")
        manager.add_student(student_id, student_name)

    elif choice == "2":
        student_id = input("Enter Student ID: ")
        status = input("Enter Attendance (Present/Absent): ")
        manager.mark_attendance(student_id, status)

    elif choice == "3":
        manager.view_attendance()

    elif choice == "4":
        print("Exiting system...")
        break

    else:
        print("Invalid choice. Try again.")
🔹 4. TESTING
Test Cases
Add student → ✅ Successful
Mark attendance → ✅ Successful
View attendance → ✅ Correct output
Invalid student ID → ✅ Error message shown
🔹 5. DEPLOYMENT
The system runs locally using Python.
Can be shared via GitHub for easy access and collaboration.
🔹 6. MAINTENANCE
New features like login system or database storage can be added later.
Bugs can be fixed through updates on GitHub.
3️⃣ PUSHING THE PROJECT TO GITHUB
Step 1: Create a GitHub Repository
Repository name: Student-Attendance-Management-System
Step 2: Open Terminal in Project Folder
Copy code
Bash
git init
git add .
git commit -m "Initial commit - Student Attendance Management System"
git branch -M main
git remote add origin https://github.com/your-username/Student-Attendance-Management-System.git
git push -u origin main
4️⃣ README.md CONTENT (IMPORTANT)
Copy code
Markdown
# Student Attendance Management System (SAMS)

This project is a simple Python-based system for managing student attendance.

## Features
- Add students
- Mark attendance
- View attendance records

## How to Run
1. Install Python
2. Run `python main.py`
