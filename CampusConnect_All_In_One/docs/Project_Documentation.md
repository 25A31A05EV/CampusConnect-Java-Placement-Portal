# CampusConnect – Smart Placement Management System

## Abstract
CampusConnect is a web-based placement management concept designed to organize student profiles, placement opportunities, eligibility checks and application progress in one place.

## Problem statement
Placement information is often distributed across notices, spreadsheets and messages. Students may find it difficult to track opportunities and eligibility, while placement coordinators need a structured way to manage student and drive information.

## Objectives
1. Maintain student academic profiles.
2. Publish placement drives and eligibility criteria.
3. Check student eligibility against minimum CGPA.
4. Track application status.
5. Present placement activity through a dashboard.

## Modules
- Dashboard: summary counts and recent activity.
- Student Management: add and view student profiles.
- Placement Drives: list company opportunities and criteria.
- Eligibility: compare student CGPA with drive requirement.
- Applications: record and track application status.

## Main workflow
Start → Open dashboard → Select module → Enter/view data → Validate input → Save/update record → Display confirmation → End.

## Algorithms
### Student registration
1. Read student name, email, department and CGPA.
2. Validate required fields.
3. Validate CGPA is between 0 and 10.
4. Check whether email already exists.
5. If invalid or duplicate, show an error.
6. Otherwise save student and show success.

### Eligibility checking
1. Select a student and placement drive.
2. Read student CGPA and drive minimum CGPA.
3. If student CGPA >= minimum CGPA, mark academically eligible.
4. Otherwise mark not eligible.
5. Display the result.
6. Note: actual recruitment eligibility may include backlogs, branch, graduation year and other criteria.

### Application tracking
1. Select student and drive.
2. Check whether an application already exists.
3. If duplicate, show a warning.
4. Otherwise create application with status `Applied`.
5. Display the updated application list.

## Suggested data entities
Student(studentId, name, email, department, cgpa)
Drive(driveId, company, role, minCgpa, eligibleBranch)
Application(applicationId, studentId, driveId, status, appliedDate)

## Testing checklist
- Reject blank student name/email.
- Reject CGPA outside 0–10.
- Reject duplicate email.
- Verify eligible and ineligible CGPA cases.
- Prevent duplicate applications.
- Verify status display after an application is added.

## Limitations and future enhancements
Current browser demo stores data in localStorage on one browser. Future work can add a shared database, authentication, role-based access for students/coordinators, email notifications, resume upload, analytics and deployment.
