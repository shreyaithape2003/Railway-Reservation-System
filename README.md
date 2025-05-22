#🚆 Railway Reservation System 
A simple yet functional web application built using the .NET Framework (MVC architecture) that allows users to search trains, book seats, cancel bookings, and for admins to manage the system.

This project follows a Database-First approach, where the database is created first using SQL Server Management Studio (SSMS), and the application code is scaffolded in Visual Studio using an .edmx file.

##📌 Features
This project contains 5 core modules:

###🔐 Login & Registration: User authentication and registration.

###🔍 Search Trains: Users can search for trains between stations.

###🪑 Book Seat: Book a seat for a selected train.

###❌ Cancel Booking: Cancel previously booked tickets.

###🛠️ Admin Panel: For managing train data, users, and bookings.

##🛠️ Technologies Used
Frontend: ASP.NET MVC (Razor Views)

Backend: C#, Entity Framework (Database-First)

Database: SQL Server (SSMS)

##Tools:

Visual Studio

SQL Server Management Studio (SSMS)

##📂 Folder Structure

RailwayReservation/
├── Controllers/       # All controller logic
├── Models/            # Entity Framework models
├── Views/             # Razor views (UI)
├── App_Data/          # Local database (if any)
├── RailwayReservation.sln  # Visual Studio solution file
├── Web.config         # Connection strings and config

#🚀 How to Run the Project
##✅ Prerequisites
Visual Studio 2019 or newer

SQL Server & SSMS installed

##🔄 Step-by-Step Execution
###Clone or Download the Repository
Open the solution by double-clicking RailwayReservation.sln.

###Create the Database in SSMS

Open SSMS.

Create a new database (e.g., RailwayDB).

Create all required tables manually or via a provided SQL script (not included here, you must define schema).

###Configure the Connection String

Open Web.config.

Update the connection string with your SSMS server name and DB name:

<connectionStrings>
  <add name="RailwayDBEntities" 
       connectionString="metadata=res://*/Models.YourModel.csdl|res://*/Models.YourModel.ssdl|res://*/Models.YourModel.msl;provider=System.Data.SqlClient;provider connection string=&quot;data source=YOUR_SERVER_NAME;initial catalog=RailwayDB;integrated security=True;MultipleActiveResultSets=True;App=EntityFramework&quot;" 
       providerName="System.Data.EntityClient" />
</connectionStrings>
    
###Build the Project

Click Build > Build Solution in Visual Studio.

Ensure no errors appear in the Output panel.

###Run the App

Press F5 or click the "Start" button to launch the app in your browser.

##🏗️ Building From Scratch (Database-First Setup)
If you want to create the project from scratch using Database-First approach:

Create Database & Tables in SSMS.

Open Visual Studio and create a new ASP.NET MVC Web Application (.NET Framework).

Add ADO.NET Entity Data Model:

Right-click the Models folder → Add → New Item.

Select ADO.NET Entity Data Model → Name it RailwayModel.edmx.

Choose EF Designer from database.

Connect to your database and select tables → Finish.

Scaffold Controllers & Views:

Right-click the Controllers folder → Add → Controller.

Select MVC 5 Controller with views, using Entity Framework.

Choose your model class and DbContext.

Repeat for all required entities (e.g., Trains, Bookings, Users).

##🧪 Testing the Features
Login/Register as a user and explore features.

Search for trains using source and destination.

Book a Seat: test if records appear in DB.

Cancel a Booking: check DB to ensure deletion.

Admin Panel: validate administrative operations.
