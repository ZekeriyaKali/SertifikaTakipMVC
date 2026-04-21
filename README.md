# CertificateTrackingMVC

CertificateTrackingMVC is a web-based application developed with ASP.NET Core MVC to manage employee certificates, track expiration dates, and automate notification processes.

The system allows employees to apply for certificate renewals and receive alerts via email and SMS before their certificates expire.

---

## Project Overview

This application is designed to solve certificate expiration tracking problems in organizations.

Users can:

- Register and log in to the system
- View their certificates
- Apply for certificate renewal
- Receive notifications before expiration
- Get alerts via email and SMS

The project follows a layered architecture using Repository and Service patterns.

---

## Technologies Used

- ASP.NET Core MVC
- Entity Framework Core
- MSSQL Server
- Session-based Authentication
- MailKit (Email sending)
- Twilio API (SMS sending)

---

## Architecture

The project is built using a multi-layered architecture:

- Presentation Layer (MVC Controllers & Views)
- Service Layer (Business logic)
- Repository Layer (Data access)
- Entity Layer (Database models)

This structure improves maintainability and separation of concerns.

---

## Key Features

- Employee registration and login system (Session-based)
- Certificate management (create, update, view)
- Certificate expiration tracking
- Application (renewal request) system
- Email notification system (MailKit)
- SMS notification system (Twilio)
- User-specific data filtering (based on session)
- Error handling and validation

---

## How It Works

1. Employee registers and logs into the system
2. Employee views their certificates
3. System checks certificate expiration date
4. If expiration is over (e.g. 30 days), notifications are triggered
5. Employee can submit a renewal application
6. System stores and tracks applications

---

## Notification Logic

- System calculates expiration date
- If remaining time is less than 30 days:
  - Email notification is sent
  - SMS notification is sent
- Otherwise, user is informed that the date is not نزدیک

---

## Security

- Session-based authentication
- User-specific data access
- Basic validation and error handling

---

## Project Structure
Controllers/
ApplicationController.cs
CertificateController.cs
LoginController.cs
NotificationController.cs
HomeController.cs
AdminLoginController.cs
HomeScreenController

Services/
ApplicationManager.cs
CertificateManager.cs
EmployeeManager.cs

Repositories/
IRepositoryManager.cs
RepositoryContext.cs

Entities/
Employee.cs
Certificate.cs
Application.cs
Notification.cs
Apply.cs
ESignatureCertificate.cs
NotificationType.cs
NotificationRecord.cs
## Setup

1. Clone the repository

git clone https://github.com/yourusername/CertificateTrackingMVC.git

2. Configure database

Update connection string in appsettings.json

3. Run the project

dotnet run

---

## Notes

- Twilio credentials must be configured for SMS functionality
- Email sending requires valid SMTP credentials
- Session must be enabled in Startup/Program.cs

---

## Project Status

This project is partially completed and still under development.

Planned improvements:

- Role-based authentication (Admin/User)
- UI/UX improvements
- Notification scheduling (background jobs)
- API integration
- Deployment to cloud

---

## Purpose

This project is developed to demonstrate backend development skills, layered architecture, and real-world business logic implementation.

---

