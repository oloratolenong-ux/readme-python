# Student Grade Management System

## Description

The Student Grade Management System is a Python program that allows users to be able to manage student data and grades.The program uses dictionaries to store student names, subjects, and grades. It allows the user to add, update student data, remove student data, search for students, and view grades for a specific subject.

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

# Gradebook Management System

A command-line Python program for recording and managing student grades across several subjects. The code is organised into small, reusable functions with built-in validation and error handling.



## Features

- Add students with a grade for each subject (Math, English, Science)
- Search for a student by name and update their grades
- Remove a student
- View one student's grades and overall average
- View all grades for a single subject
- View a summary of every student's average, plus the class average, highest and lowest
- Input validation and clear error messages (no crashes on bad input)


## How to Run

1. Save the program as `gradebook_menu_modular.py`.
2. Open a terminal in the folder containing the file.
3. Run:

   ```
   python gradebook_menu_modular.py
    ```
## How to Use

When the program starts, it asks how many students to add. For each student, enter a name and a grade (0-100) for every subject. Then the main menu appears:


1. Add Student
2. Update Grades
3. Remove Student
4. Search Student
5. View Subject Grades
6. Students Summary
7. Exit
 Option | What it does |
|--------|--------------|
| 1. Add Student | Adds a new student and prompts for a grade in each subject. |
| 2. Update Grades | Searches for a student by name, shows their grades, then adds a new grade to the subject you choose. |
| 3. Remove Student | Deletes a student by name. |
| 4. Search Student | Shows a student's grades per subject and their overall average. |
| 5. View Subject Grades | Lists every student's grades for one subject. |
| 6. Students Summary | Shows each student's average, the class average, and the highest and lowest student averages. |
| 7. Exit | Closes the program. |

Name and subject searches are not case-sensitive, so `amy` finds `Amy` and `math` finds `Math`.

## Data Structure

Students are stored in a dictionary. Each student maps to their subjects, and each subject holds a list of grades:

students = {
    "Amy": {"Math": [85.0, 90.0], "English": [78.0], "Science": [92.0]},
    "Ben": {"Math": [70.0], "English": [88.0], "Science": [65.0]},
}


Updating a grade appends the new grade to the subject's list rather than replacing the old one. The average is calculated across all stored grades.

## Functions

| Function | Purpose |
|----------|---------|
| `get_valid_grade(prompt)` | Keeps asking until the user enters a number from 0 to 100. |
| `get_number_of_students()` | Asks for the number of students and returns a non-negative whole number. |
| `find_student(name)` | Finds a student by name (case-insensitive); returns the stored name or `None`. |
| `find_subject(subject)` | Finds a subject by name (case-insensitive); returns the subject or `None`. |
| `add_student()` | Adds a student with one validated grade per subject. Rejects empty or duplicate names. |
| `calculate_average(student_grades)` | Returns the average of all of a student's grades, or `None` if there is no data. |
| `display_student(name)` | Shows a student's grades per subject and their average. |
| `display_students_summary()` | Shows every student's average and the class statistics. |
| `search_and_update()` | Finds a student by name and adds a new grade to a chosen subject. |
| `remove_student()` | Removes a student by name. |
| `view_subject_grades()` | Shows all students' grades for one subject. |
| `show_menu()` | Prints the main menu. |
| `main()` | Runs the program loop. |

## Validation and Error Handling

| Situation | How it is handled |
|-----------|-------------------|
| Non-numeric grade or student count | `try/except ValueError` shows a message and asks again. |
| Grade below 0 or above 100 | Rejected with an explanation, then asks again. |
| Empty or duplicate student name | Rejected with a message. |
| Student or subject does not exist | A "not found" message is shown and no changes are made. |
| No grades available for an average | `ZeroDivisionError` is caught and a message is shown. |
| Missing or invalid grade data | `TypeError`, `AttributeError` and `KeyError` are caught inside the functions. |
| Invalid menu choice | An "Invalid choice" message is shown and the menu appears again. |

## Example Session


Enter number of students: 1

Student 1
Enter student name: Amy
Enter Math grade: 85
Enter English grade: abc
Please enter a valid number.
Enter English grade: 78
Enter Science grade: 92
Student added.

1. Add Student
2. Update Grades
...
Enter choice: 4
Enter student name: amy

Grades for Amy
Math : [85.0]
English : [78.0]
Science : [92.0]
Average: 85.00

 Option | What it does |
|--------|--------------|
| 1. Add Student | Adds a new student and prompts for a grade in each subject. |
| 2. Update Grades | Searches for a student by name, shows their grades, then adds a new grade to the subject you choose. |
| 3. Remove Student | Deletes a student by name. |
| 4. Search Student | Shows a student's grades per subject and their overall average. |
| 5. View Subject Grades | Lists every student's grades for one subject. |
| 6. Students Summary | Shows each student's average, the class average, and the highest and lowest student averages. |
| 7. Exit | Closes the program. |

Name and subject searches are not case-sensitive, so `amy` finds `Amy` and `math` finds `Math`.

## Data Structure

Students are stored in a dictionary. Each student maps to their subjects, and each subject holds a list of grades:


students = {
    "Amy": {"Math": [85.0, 90.0], "English": [78.0], "Science": [92.0]},
    "Ben": {"Math": [70.0], "English": [88.0], "Science": [65.0]},
}


Updating a grade appends the new grade to the subject's list rather than replacing the old one. The average is calculated across all stored grades.

## Functions

| Function | Purpose |
|----------|---------|
| `get_valid_grade(prompt)` | Keeps asking until the user enters a number from 0 to 100. |
| `get_number_of_students()` | Asks for the number of students and returns a non-negative whole number. |
| `find_student(name)` | Finds a student by name (case-insensitive); returns the stored name or `None`. |
| `find_subject(subject)` | Finds a subject by name (case-insensitive); returns the subject or `None`. |
| `add_student()` | Adds a student with one validated grade per subject. Rejects empty or duplicate names. |
| `calculate_average(student_grades)` | Returns the average of all of a student's grades, or `None` if there is no data. |
| `display_student(name)` | Shows a student's grades per subject and their average. |
| `display_students_summary()` | Shows every student's average and the class statistics. |
| `search_and_update()` | Finds a student by name and adds a new grade to a chosen subject. |
| `remove_student()` | Removes a student by name. |
| `view_subject_grades()` | Shows all students' grades for one subject. |
| `show_menu()` | Prints the main menu. |
| `main()` | Runs the program loop. |

## Validation and Error Handling

| Situation | How it is handled |
|-----------|-------------------|
| Non-numeric grade or student count | `try/except ValueError` shows a message and asks again. |
| Grade below 0 or above 100 | Rejected with an explanation, then asks again. |
| Empty or duplicate student name | Rejected with a message. |
| Student or subject does not exist | A "not found" message is shown and no changes are made. |
| No grades available for an average | `ZeroDivisionError` is caught and a message is shown. |
| Missing or invalid grade data | `TypeError`, `AttributeError` and `KeyError` are caught inside the functions. |
| Invalid menu choice | An "Invalid choice" message is shown and the menu appears again. |

## Example Session


Enter number of students: 1

Student 1
Enter student name: Amy
Enter Math grade: 85
Enter English grade: abc
Please enter a valid number.
Enter English grade: 78
Enter Science grade: 92
Student added.

1. Add Student
2. Update Grades
...
Enter choice: 4
Enter student name: amy

Grades for Amy
Math : [85.0]
English : [78.0]
Science : [92.0]
Average: 85.00

## Possible Improvements

- Save and load students from a file so data persists between runs
- Add letter grades or pass/fail thresholds
- Allow replacing a grade instead of only appending
