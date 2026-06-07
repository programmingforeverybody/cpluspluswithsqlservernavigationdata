# Data Navigation Like .NET in C++ with SQL Server

This project demonstrates how to implement .NET-style data navigation in C++ using SQL Server.

The application allows users to navigate through records using:

* First Record
* Previous Record
* Next Record
* Last Record

The project is designed to help developers understand how data navigation works behind the scenes in desktop applications.

## Technologies Used

* C++
* SQL Server
* ODBC
* Visual Studio
* Windows Desktop Development

## Database Setup

Create the database and table using the following SQL Server script:

```sql
USE [db103]
GO

CREATE TABLE [dbo].[Table1]
(
    [id_student] INT IDENTITY(1,1) NOT NULL,
    [name_student] VARCHAR(50) NULL,
    [English] FLOAT NULL,
    [French] FLOAT NULL,
    [Spanish] FLOAT NULL,

    CONSTRAINT [PK_Table1]
    PRIMARY KEY CLUSTERED
    (
        [id_student] ASC
    )
)
GO

SET IDENTITY_INSERT [dbo].[Table1] ON

INSERT INTO [dbo].[Table1]
([id_student], [name_student], [English], [French], [Spanish])
VALUES
(1,'John',10,9,8),
(3,'Martin',10,10,10),
(5,'Salah',10,10,10),
(6,'Vladimir',10,10,10),
(7,'Randy',10,9,9.5),
(8,'Kane',10,10,10),
(9,'Kamal',9,9.5,NULL)

SET IDENTITY_INSERT [dbo].[Table1] OFF
GO
```

## Query Used

```sql
SELECT
    id_student,
    name_student,
    English,
    French,
    Spanish
FROM dbo.Table1;
```

## Application Features

* Connect to SQL Server
* Load student records
* Display record information
* Navigate through records
* First / Previous / Next / Last functionality
* Record position tracking
* Simple and reusable navigation logic

## User Interface Fields

* Student ID
* Student Name
* English Grade
* French Grade
* Spanish Grade

## How to Run

1. Create the database using the script above.
2. Open the project in Visual Studio.
3. Configure the SQL Server connection string.
4. Build and run the application.
5. Use the navigation buttons to browse records.

## Video Tutorial

Watch the complete tutorial on YouTube:

https://youtu.be/QXkuH7q5RXc
## Source Code

This repository contains the complete source code used in the tutorial.

## Author

Programming For Every Body

⭐ If this project helps you, please star the repository and subscribe to the YouTube channel for more C++, SQL Server, and database programming tutorials.
