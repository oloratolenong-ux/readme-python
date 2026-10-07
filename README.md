# Student Grade Management System

## Description

The Student Grade Management System is a Python program that allows users to be able to manage student data and grades.

The program uses dictionaries to store student names, subjects, and grades. It allows the user to add, update student data, remove student data, search for students, and view grades for a specific subject.

# Features

The program provides the following features:

1. Add a New Student
   - Allows the user to enter a student name.
   - Allows grades to be entered for Math, English, and Science.
   - Stores the student's information in the dictionary.

2. Update Student Grades
   - Adds a new grade to the student's existing grades.
   - User can select student and student grades.

3. Remove a Student
   - Allows the user to remove a student from the system.

4. Search for a Student
   - Allows the user to search for a student by their name.
   - Displays the student's grades for each subject.
   - Calculates and displays the student's average grade.

5. View Subject Grades
   - Allows the user to select a subject.
   - Displays the grades for that subject for all students.

6. Exit
   - Allows the user to close the program.

## Data Structure

The program uses a nested dictionary to store the student information.

The structure is:


students = {
    "Peo Molatlhi": {
        "Math": [80],
        "English": [75],
        "Science": [90]
    }
}
