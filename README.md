# Student Academic Records Management System

A responsive web-based application for managing student academic records, calculating GPA and CGPA, generating transcripts, analysing academic performance, and importing or exporting student data.

## Live Demo

[Open the Student Academic Records Management System](YOUR-GITHUB-PAGES-LINK)

## Project Overview

The Student Academic Records Management System was developed as an academic assignment for the **Programming for Mechanical Engineers** course unit.

The project demonstrates how programming concepts can be applied to develop a practical system for managing student information and academic results. It provides a clean and responsive interface for registering students, recording semester results, calculating academic performance, generating transcripts, and producing summary reports.

## Academic Context

**Institution:** Kyambogo University

**Department:** Mechanical and Production Engineering

**Programme:** Bachelor of Engineering in Automotive and Power Engineering

**Course Unit:** Programming for Mechanical Engineers

**Academic Year:** 2025/2026

**Student:** Ronald Owomugisha

**Registration Number:** 24/U/APD/11369/PD

## Main Features

* Student registration and record management
* Student searching, filtering, and sorting
* Semester and course unit management
* Automatic grade and grade-point calculation
* Semester GPA calculation
* Cumulative GPA calculation
* Academic classification
* Student transcript generation
* Academic performance dashboard
* Programme and year-level reports
* CSV data import and export
* Printing of dashboards, reports, registers, and transcripts
* Browser-based data persistence
* Responsive layout for computers, tablets, and mobile phones

## Academic Grading System

| Mark Range | Grade | Grade Point |
| ---------- | ----: | ----------: |
| 80–100     |     A |         5.0 |
| 75–79      |    B+ |         4.5 |
| 70–74      |     B |         4.0 |
| 65–69      |    C+ |         3.5 |
| 60–64      |     C |         3.0 |
| 55–59      |    D+ |         2.5 |
| 50–54      |     D |         2.0 |
| Below 50   |     F |         0.0 |

The system calculates GPA and CGPA using the credit-weighted grade points of the recorded course units.

## Technologies Used

* HTML5
* CSS3
* JavaScript
* Browser Local Storage
* CSV file handling
* GitHub Pages

The application is implemented as a self-contained frontend project and does not require external frameworks or a build process.

## Running the Project Locally

1. Download or clone this repository.
2. Open the project folder.
3. Open `index.html` in a modern web browser.

No software installation, server, or database configuration is required.

## CSV Import Format

Student information can be imported using a CSV file with the following column structure:

```csv
Name,Reg Number,Programme,Year,Email,CGPA,Classification,Semesters
```

A sample CSV file is included in the repository.

## Data Storage

Student records and changes are stored locally in the browser using Local Storage.

This means:

* Records remain available after refreshing the page.
* Information is stored only in the browser and device being used.
* Records are not automatically shared between users or devices.
* Clearing browser data may remove saved records.

## Printing

The system supports printing of the active dashboard, student register, reports, and academic transcripts using a simplified print layout.

## Project Structure

```text
student-records-system/
├── index.html
├── README.md
├── CODE_REVIEW.md
├── sample_students.csv
└── .nojekyll
```

## Project Scope

This application was developed as an academic frontend project and demonstration system.

It should not be used for official or confidential university records without a secure backend, authentication system, central database, user permissions, backups, and institutional data-protection controls.

## Author

**Ronald Owomugisha**
Bachelor of Engineering in Automotive and Power Engineering
Department of Mechanical and Production Engineering
Kyambogo University
