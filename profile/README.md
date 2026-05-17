<div align="center">

<img src="peerToPeer.ico" alt="StudyLink Logo" width="80"/>

# 🎓 StudyLink — Peer Tutoring Ecosystem

> *Bridging the academic gap through a secure, peer-to-peer knowledge exchange platform.*

![Status](https://img.shields.io/badge/Status-Academic%20Project-blue?style=flat-square)
![Language](https://img.shields.io/badge/Language-C%23-purple?style=flat-square&logo=csharp)
![Framework](https://img.shields.io/badge/Framework-WPF%20.NET%2010-blueviolet?style=flat-square)
![Database](https://img.shields.io/badge/Database-MySQL%208.0-orange?style=flat-square&logo=mysql)
![Platform](https://img.shields.io/badge/Platform-Windows-0078D6?style=flat-square&logo=windows)

</div>

## 📖 Table of Contents

- [About the Project](#-about-the-project)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Diagrams](#-diagrams)
- [Project Structure](#-project-structure)
- [How to Run](#-how-to-run)
- [Database Setup](#-database-setup)
- [User Roles](#-user-roles)
- [Team](#-team)

## 🧠 About the Project

**StudyLink** is a desktop peer tutoring marketplace built for 1st and 2nd-year university students facing academic or financial challenges.

Professional tutoring is prohibitively expensive, leading to increased stress and higher dropout rates. At the same time, high-achieving upper-year students lack structured ways to monetize their academic expertise.

StudyLink bridges this gap by connecting students with peer tutors in a secure, accountable ecosystem — featuring booking management, payment simulation, a review & rating system, and an admin panel with jury-based dispute resolution.

### 🌍 Societal Impact
- Promotes **educational equity** by making tutoring accessible to mid-to-low income students
- Empowers **upper-year students** to earn income using their academic skills
- Ensures **quality control** through transparent reviews and administrator oversight

## 🛡️ Features

### 👨‍🎓 For Students
- **Smart Search** — Find tutors instantly by course code or subject
- **Verified Profiles** — View tutor expertise, ratings, and hourly rates
- **Booking System** — Schedule sessions and track your history

### 👩‍🏫 For Tutors
- **Profile Management** — Customize your bio, set your rates, and showcase expertise
- **Availability Calendar** — Manage your available time slots dynamically
- **Reputation System** — Build trust through verified peer reviews and ratings

### 🛡️ For Administrators
- **User Oversight** — Full management of accounts and tutor approval workflows
- **Jury Dispute Resolution** — Handle "Jury Cases" to maintain tutoring standards
- **System Analytics** — Access platform statistics and security logs

## 🏗️ Tech Stack

| Layer | Technology |
|---|---|
| Language | C# |
| UI Framework | WPF (.NET 10.0+) |
| Database | MySQL 8.0 |
| Data Access | Raw SQL with MySqlConnector |
| Security | SHA256 Password Hashing |
| IDE | Visual Studio |

## 📊 Diagrams

### Entity Relationship Diagram (ERD)

![ERD](Diagrams/ERD.jpeg)

### UML Class Diagram

![UML](Diagrams/UML.jpeg)

## 📁 Project Structure

```
StudyLink/
├── Data/
│   └── DatabaseHelper.cs         # MySQL connection & query execution
├── Helpers/
│   ├── PasswordHelper.cs         # SHA256 hashing logic
│   └── ValidationHelper.cs       # Input validation utilities
├── Models/
│   ├── User.cs
│   ├── TutorProfile.cs
│   ├── Booking.cs
│   ├── BookingDisplay.cs
│   ├── Review.cs
│   ├── AvailabilitySlot.cs
│   └── JuryCase.cs
├── Services/
│   └── UserService.cs            # Business logic layer
├── Views/
│   ├── AdminDashboardWindow.xaml
│   ├── BookingWindow.xaml
│   ├── PaymentWindow.xaml
│   ├── RegisterWindow.xaml
│   ├── ReviewWindow.xaml
│   ├── TutorDashboardWindow.xaml
│   ├── TutorProfileWindow.xaml
│   ├── ForgotPasswordWindow.xaml
│   └── Panels/
│       ├── StudentPanel.xaml
│       └── TutorPanel.xaml
├── Diagrams/
│   ├── ERD.jpeg
│   └── UML.jpeg
├── Wireframes/
├── App.xaml
├── MainWindow.xaml
└── StudyLink.csproj
```

## 🚀 How to Run

### Prerequisites

Before running StudyLink, make sure you have the following installed:

- [Visual Studio 2022+](https://visualstudio.microsoft.com/) with **.NET Desktop Development** workload
- [.NET 10.0 SDK](https://dotnet.microsoft.com/en-us/download)
- [MySQL Server 8.0](https://dev.mysql.com/downloads/mysql/)
- [MySqlConnector NuGet package](https://www.nuget.org/packages/MySqlConnector)

### Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/ThomasMore-StudyLink/StudyLink-Desktop.git
   cd StudyLink-Desktop
   ```

2. **Set up the database** — see [Database Setup](#-database-setup) below

3. **Configure your connection string**

   Open `Data/DatabaseHelper.cs` and update the connection string with your MySQL credentials:
   ```csharp
   private static string connectionString =
       "Server=localhost;Database=studylink;User ID=root;Password=YOUR_PASSWORD;";
   ```

4. **Open the solution in Visual Studio**
   ```
   Open StudyLink.csproj
   ```

5. **Restore NuGet packages**

   Visual Studio will do this automatically, or run:
   ```bash
   dotnet restore
   ```

6. **Run the project**

   Press `F5` or click the **▶ Run** button in Visual Studio.

## 🗄️ Database Setup

1. Open your MySQL client via CMD:
   ```bash
   mysql -u root -p
   ```
2. Create and select the database:
   ```sql
   CREATE DATABASE studylink;
   USE studylink;
   ```
3. Run the full SQL schema from the `HOW-TO-RUN.md` file included in this repo.

## 👥 User Roles

| Role | Description |
|---|---|
| **Student** | Searches for tutors, books sessions, makes payments, leaves reviews |
| **Tutor** | Manages profile & availability, receives bookings, builds reputation |
| **Administrator** | Manages all users, approves tutors, resolves jury disputes |

## 👨‍💻 Team

Built with ❤️ by the **ThomasMore-StudyLink** team.

| Contributor | Role |
|---|---|
| mehmetmetinerdemli | Developer |
| IsenGrd (Ihsan Mercan) | Developer |

<div align="center">

*Made as part of an academic project — Thomas More University*

</div>
