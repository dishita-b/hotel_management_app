# 🏨 Hotel Management System

A full stack desktop application built in Java for managing core hotel operations including room bookings guest records and billing all backed by a MySQL database

Note: This is a Java Swing desktop application and cannot be deployed as a live web preview. It requires a local Java runtime and MySQL instance to run.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | Java (JDK 8+) |
| UI Framework | Java Swing |
| Database | MySQL |
| DB Connector | mysql-connector-java 8.0.28 / mysql-connector-j 8.3.0 |
| Table Rendering | rs2xml |
| Build Tool | Apache Ant (build.xml) |
| IDE | NetBeans / IntelliJ IDEA |

---

## Project Structure

```
hotel_management_app/
├── src/                              # Java source files
├── nbproject/                        # NetBeans project config
├── build.xml                         # Ant build script
├── Hotel Management System.iml       # IntelliJ module file
├── mysql-connector-j-8.3.0.jar       # MySQL JDBC driver (latest)
├── mysql-connector-java-8.0.28.jar   # MySQL JDBC driver (legacy)
└── .gitignore
```

---

## Why No Live Demo

Unlike web-based projects this application is built on Java Swing which renders native OS-level GUI windows and requires direct access to a display environment. This architecture cannot be containerized into a browser-accessible deployment the way Python or Node.js web apps can. Running it requires a local JDK and a configured MySQL server which is standard for enterprise-grade desktop software of this kind.

---

## Database Connectivity

The app connects to MySQL using JDBC. rs2xml is used to populate Swing JTable components directly from ResultSet objects making database-to-UI rendering seamless

```xml
<orderEntry type="library" name="mysql-connector-java-8.0.28" level="project" />
<orderEntry type="library" name="rs2xml" level="project" />
```

---

## Core Modules

- Room Management — add view and update room availability and types
- Guest Management — register and manage guest check-in and check-out records
- Booking System — handle reservations linked to guest and room data
- Billing — generate bills based on stay duration and room pricing
- Admin Panel — manage hotel staff and operational data

---

## How to Run

Prerequisites: JDK 8 or above and MySQL server installed

```bash
# 1. Clone the repository
git clone https://github.com/dishita-b/hotel_management_app.git

# 2. Import into NetBeans or IntelliJ as a Java project

# 3. Set up your MySQL database and update the DB credentials in the source

# 4. Add both JAR files to the project classpath
#    mysql-connector-j-8.3.0.jar
#    rs2xml.jar

# 5. Build and run via Ant
ant run
```
---

## Build System

The project uses Apache Ant with a standard NetBeans-generated build.xml

Key Ant targets available:

- clean — removes compiled build artifacts
- build — compiles all Java source files
- run — executes the main application class
- jar — packages the project into a distributable JAR

## Author

Dishita Barman
LinkedIn: https://www.linkedin.com/in/dishita-barman5/
GitHub: https://github.com/dishita-b
