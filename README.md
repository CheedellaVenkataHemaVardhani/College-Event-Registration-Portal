College Event Registration Portal

📌 Project Overview

The College Event Registration Portal is a ServiceNow-based web application that helps students view college events, register for events, and track their registration status.

The application also provides an admin approval process and a dashboard to monitor event registrations.

🎯 Objectives

Allow students to view upcoming college events.

Allow students to register for an event.

Automatically fill the logged-in student's details.

Prevent duplicate registrations for the same event.

Send registrations for admin approval.

Update registration status as Pending, Confirmed, or Rejected.

Allow students to view their own registrations.

Provide a dashboard with useful registration statistics.

✨ Main Features

1. View Events

Students can view available college events with information such as:

Event Name

Event Type

Event Date

Event Time

Venue

Available Seats

Event Status

2. Event Registration

Students can register for an event through the registration form.

The form contains:

Event – selected event

Student – automatically filled with the logged-in user

Registration Date – automatically filled

Registration Reason / Notes – entered by the student

Status – automatically set to Pending

Student, Registration Date, and Status are read-only.

3. Duplicate Registration Prevention

A Business Rule checks whether the student has already registered for the selected event.

If a duplicate registration is detected, the system prevents the registration and displays an appropriate message.

4. Admin Approval

New registrations are initially set to Pending.

The existing ServiceNow Flow handles the approval process:

Student Registration
        ↓
     Pending
        ↓
   Admin Approval
      ↙     ↘
Confirmed   Rejected

5. My Registrations

Students can view the events they have registered for and check their current status.

Example:

Event

Registration Date

Status

College Tech Fest

15-Aug-2026

Pending

Python Workshop

15-Aug-2026

Confirmed

6. Student Dashboard

The dashboard provides a quick overview of registration activity.

Current dashboard components include:

Registrations By Event – bar chart

Registration Status – pie chart

Total Registrations – number indicator

Registration Trend – line chart

Daily Registrations – chart

🔄 Project Workflow

Student opens Portal
        ↓
View Events
        ↓
Select an Event
        ↓
Open Registration Form
        ↓
Event is selected
        ↓
Student details are auto-filled
        ↓
Student enters Notes
        ↓
Submit Registration
        ↓
Duplicate Registration Check
        ↓
Status = Pending
        ↓
Admin/Event Organizer Approval
        ↓
   ┌───────────────┐
   ↓               ↓
Confirmed       Rejected
   ↓               ↓
Student can view the updated status

🛠️ Technologies Used

ServiceNow

App Engine Studio

UI Builder

Flow Designer

Client Scripts

Business Rules

ServiceNow Tables

ServiceNow Reports / Dashboards

JavaScript

🗃️ Main Tables

Event Table

Stores college event information.

Important fields:

Event Name

Event Type

Event Date

Event Time

Venue

Capacity

Available Seats

Event Status

Event Registration Table

Stores student registration information.

Important fields:

Event

Student

Registration Date

Registration Reason / Notes

Status

Approval information

⚙️ Automation

Client Script

The Client Script automatically:

Sets the Student field to the current logged-in user.

Sets the Registration Date.

Sets the Status to Pending.

Makes Student, Registration Date, and Status read-only.

Business Rule

The Business Rule prevents the same student from registering for the same event more than once.

Flow Designer

The approval flow processes new registrations and updates the registration status based on the admin's decision.

📊 Dashboard

The dashboard helps administrators/students understand registration activity through visual reports.

Example dashboard:

College Event Registration Dashboard

┌──────────────────────┬──────────────────────┬──────────────────┐
│ Registrations        │ Registration Status  │ Total            │
│ By Event             │                      │ Registrations    │
│ Bar Chart             │ Pie Chart            │ Number           │
└──────────────────────┴──────────────────────┴──────────────────┘

┌──────────────────────┬──────────────────────┐
│ Registration Trend   │ Daily Registrations  │
│ Line Chart           │ Column Chart         │
└──────────────────────┴──────────────────────┘

👥 User Roles

Student

View events

Register for events

Enter registration notes

View personal registrations

Check approval status

View dashboard information

Admin / Event Organizer

Manage events

Review registrations

Approve or reject registrations

Monitor registration activity

✅ Benefits

Simplifies college event registration.

Reduces manual registration work.

Prevents duplicate registrations.

Provides a clear approval workflow.

Gives students real-time registration status.

Provides useful dashboard reports.

Demonstrates ServiceNow application development and automation.

🚀 Future Enhancements

Email notifications for registration confirmation and rejection.

Automatic available-seat updates after confirmation.

Event search and filtering.

QR-code-based event check-in.

Mobile-friendly portal design.

Admin analytics for event popularity.

Automatic cancellation when an event reaches capacity.

👩‍💻 Project Type

ServiceNow Application Development Project

Project Name: College Event Registration Portal

Platform: ServiceNow App Engine Studio
