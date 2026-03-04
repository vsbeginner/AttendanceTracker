# Attendance Tracker — Python CLI Application

A **Python-based command-line attendance tracker** that allows users to record student attendance, validate entries, generate formatted summaries, and optionally export attendance reports to a text file.

This project demonstrates the use of **Python fundamentals such as input handling, file operations, loops, and data validation**, making it a practical example of building a simple but useful command-line application.

---

#  Project Overview

The **Attendance Tracker** is a lightweight CLI tool designed to help manage and track student attendance through the terminal.

Users can:

* Enter student names
* Record attendance entries
* Validate input data
* Display formatted attendance summaries
* Export attendance reports to a text file

The project emphasizes **clean program structure, error handling, and file management**, making it useful for learning core Python programming concepts.

---

#  Problem Statement

Manual attendance tracking can often be time-consuming and error-prone, especially when managing multiple entries.

This project provides a simple automated solution that:

* Records attendance entries efficiently
* Prevents invalid input
* Generates clear attendance summaries
* Stores attendance logs for future reference

---

#  Solution Approach

The application is built using **Python and runs in the command-line interface (CLI)**.

The program workflow involves:

1. Accepting student names as input
2. Validating user entries
3. Storing attendance data in memory
4. Displaying formatted attendance summaries
5. Optionally exporting the attendance record to a text file

The project highlights practical usage of **Python data structures and file handling techniques**.

---

#  Key Features

###  Attendance Recording

Allows users to input and record multiple student attendance entries.

###  Input Validation

Ensures that incorrect or empty inputs are handled properly.

###  Formatted Attendance Summary

Displays attendance data in a structured and readable format.

###  File Export Support

Attendance reports can be saved to a **text file for record keeping**.

### Command-Line Interface

Runs entirely in the terminal, making it lightweight and easy to execute.

---

#  Tech Stack

| Technology                       | Purpose                   |
| -------------------------------- | ------------------------- |
| **Python 3**                     | Core programming language |
| **CLI (Command Line Interface)** | User interaction          |
| **File Handling (Python)**       | Saving attendance logs    |

---

#  Program Workflow

```
User Input (Student Name)
        │
        ▼
Input Validation
        │
        ▼
Attendance Recording
        │
        ▼
Display Summary
        │
        ▼
Optional File Export
        │
        ▼
attendance_log.txt Generated
```

---

#  Project Structure

```
attendance-tracker
│
├── tracker.py             # Main program file
├── sample_run_1.txt       # Example program execution
├── sample_run_2.txt       # Example program execution
├── sample_run_3.txt       # Example program execution
├── attendance_log.txt     # Generated attendance report
└── README.md              # Project documentation
```

---

#  Example Usage

Example CLI interaction:

```
Enter student name: Rahul
Enter student name: Priya
Enter student name: Aman

Attendance Summary
------------------
Rahul  : Present
Priya  : Present
Aman   : Present

Attendance saved to attendance_log.txt
```

---

#  Example Output Files

The repository includes sample program executions:

```
sample_run_1.txt
sample_run_2.txt
sample_run_3.txt
```

These files demonstrate how the program behaves during different attendance recording scenarios.

---

#  Challenges & Learnings

### Input Validation

Handling incorrect or empty user input was important to ensure program reliability.

### File Handling

Implementing file writing functionality helped demonstrate practical use of Python's file system operations.

### CLI Interaction Design

Designing a clear and easy-to-use command-line interaction improved usability.

---

#  Future Improvements

Potential enhancements for this project include:

* Add **date-based attendance tracking**
* Implement **CSV or Excel export support**
* Create a **graphical user interface (GUI) version**
* Add **student ID support**
* Integrate **database storage**

---

#  Author

**Vinayak Sharma**

GitHub
https://github.com/vsbeginner

LinkedIn
https://www.linkedin.com/in/vinayak-sharma-24a8aa384/

---

