# 🚆 Railway Reservation System

A simple yet functional web application built using the **.NET Framework (MVC architecture)** that allows users to search trains, book seats, cancel bookings, and for admins to manage the system.

This project follows a **Database-First approach**, where the database is created first using **SQL Server Management Studio (SSMS)**, and the application code is scaffolded in **Visual Studio** using an `.edmx` file.

---

## 📌 Features

This project contains 5 core modules:

### 🔐 Login & Registration
User authentication and registration.

### 🔍 Search Trains
Users can search for trains between stations.

### 🪑 Book Seat
Book a seat for a selected train.

### ❌ Cancel Booking
Cancel previously booked tickets.

### 🛠️ Admin Panel
For managing train data, users, and bookings.

---

## 🛠️ Technologies Used

- **Frontend:** ASP.NET MVC (Razor Views)  
- **Backend:** C#, Entity Framework (Database-First)  
- **Database:** SQL Server (SSMS)

---

## 🧰 Tools

- Visual Studio  
- SQL Server Management Studio (SSMS)

---

## 📂 Folder Structure

```
RailwayReservation/
├── Controllers/         # All controller logic
├── Models/              # Entity Framework models
├── Views/               # Razor views (UI)
├── App_Data/            # Local database (if any)
├── RailwayReservation.sln  # Visual Studio solution file
├── Web.config           # Connection strings and config
```

---

# 🚀 How to Run the Project

## ✅ Prerequisites

- Visual Studio 2019 or newer  
- SQL Server & SSMS installed

---

## 🔄 Step-by-Step Execution

### 1. Clone or Download the Repository

Open the solution by double-clicking `RailwayReservation.sln`.

### 2. Create the Database in SSMS

- Open **SQL Server Management Studio (SSMS)**  
- Create a new database (e.g., `RailwayDB`)  
- Create all required tables manually or using a script (script not included)

### 3. Configure the Connection String

- Open `Web.config`
- Update the connection string with your server name and DB name:
  
```xml
<connectionStrings>
  <add name="RailwayDBEntities" 
       connectionString="metadata=res://*/Models.YourModel.csdl|res://*/Models.YourModel.ssdl|res://*/Models.YourModel.msl;
       provider=System.Data.SqlClient;
       provider connection string=&quot;data source=YOUR_SERVER_NAME;initial catalog=RailwayDB;integrated security=True;
       MultipleActiveResultSets=True;App=EntityFramework&quot;" 
       providerName="System.Data.EntityClient" />
</connectionStrings>
```

### 4. Build the Project

- In Visual Studio:  
  `Build > Build Solution`  
- Make sure no errors are shown.

### 5. Run the App

- Press `F5` or click the **Start** button to launch in your browser.

---

## 🏗️ Building From Scratch (Database-First Setup)

If you want to build the project from scratch using Database-First:

### Step 1: Create Database & Tables

- Use **SSMS** to create your database and tables.

### Step 2: Create New MVC Project

- In Visual Studio:  
  File → New → Project → ASP.NET Web Application (.NET Framework)

### Step 3: Add ADO.NET Entity Data Model

- Right-click `Models` folder → Add → New Item  
- Choose **ADO.NET Entity Data Model**, name it `RailwayModel.edmx`  
- Select **EF Designer from database**  
- Connect to your database and select tables → Finish

### Step 4: Scaffold Controllers and Views

- Right-click `Controllers` folder → Add → Controller  
- Choose **MVC 5 Controller with views, using Entity Framework**  
- Choose your **Model** and **DbContext**  
- Repeat for all entities (e.g., Trains, Bookings, Users)

---

## 🧪 Testing the Features

- ✅ Login/Register as a user  
- 🔍 Search for trains using source and destination  
- 🪑 Book a seat and check if it's saved in the DB  
- ❌ Cancel a booking and confirm deletion  
- 🛠️ Admin: verify all management functionality

---

Feel free to contribute or raise issues if you'd like to improve this project!
