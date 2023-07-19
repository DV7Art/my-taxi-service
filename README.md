# 🚖Taxi Service🚕
Web-application that supports authentication, registration and other CRUD operations.

# 🚀 Features
- register as a driver;
- authentication as a driver
- create/update/remove a driver
- create/update/remove a country
- create/update/remove a manufacturer
- adding a driver to a car
- display a list of cars by a specific driver
- display a list of all drivers/countries/manufacturers
# Link to the AWS
You can test and see how the program works by following this link: [Link](http://taxi-env.eba-ppngpufp.eu-west-2.elasticbeanstalk.com/)

# Used technologies
- Java 11
- JDBC
- Servlet API 4.0.1
- JSP and HTML
- JSTL 1.2
- Maven 3.1.1
- MySQL 8.0
- Tomcat 9.0.50

# Project structure
This project is designed to meet the standards of multi-level architecture. Therefore, the project is divided into the following levels:
- "controller" is a package of controllers for each model separately (car, country, driver) and, accordingly, for each entity there are several controllers, each of which is responsible for one function;
- "dao" is a package  with a set of interfaces and their implementations for each individual entity for  work with the database (DAO layer);
- service is a package that describes the web application's business logic. It consists of a set of interfaces and their implementations for each individual entity (car, country, driver), as well as the logic for authenticating a new user (driver);
- "lib" is a package contains the implementation of the necessary annotations (@Inject, @Service, @Dao) and the implementation of the injector;
- "util" is a package contains a class that is responsible for providing a connection to the MySQL database in the project. It uses JDBC (Java Database Connectivity) to create a connection to the database;
- "web.filer" is a package contains a class that is an authentication filter for the taxi service web application. It is used to control access to different URLs and to check user authentication;
- "resources" is a directory contains a file with the necessary script to initialize the database with the necessary tables and their relationships;
- "webapp" is a directory contains a hierarchy of packages for each model separately, where JSP pages are located for each request. This directory also contains web.xml - this file is responsible for the configuration of the web application. It defines the settings of servlets, filters, and URL mappings used in the taxi service web application;
- checkstyle.xml - is a configuration file for the checkstyle tool, which is used to check the code style. It contains settings for various checkstyle modules that perform various code checks for compliance with style standards;
- pom.xml - used to configure and create a Maven project, add the necessary dependencies.
# Instructions for launching the project
In order to launch this project, you need to take the following steps:
1. Clone the project to your local machine.
2. Install the following software:
- Tomcat servlet container version 9.0.50;
- MySQL version 8.0 (DBMS);
- IntelliJ IDEA (IDE) to run the application.
3. Open the project in IntelliJ IDEA.
4. Locate the "init_db.sql" file in the resources directory of the project. This file contains the necessary script to initialize the database tables. Copy the content of this file.
5. Create a database and assign a username and password.
6. Paste the copied script from the "init_db.sql" file into the database to create the necessary tables.
7. In the project's "util" package, you will find a "ConnectionUtil" class. Update the configuration data for the database (URL, username, and password) in this class.
8. Connect Tomcat to the project by following these steps:
- go to "Edit Configuration" in IntelliJ IDEA;
- select the installed and unzipped Tomcat version as the "Application Server";
- in the Tomcat server configuration, specify the start page that will be displayed when the application starts. Select "war exploded" and remove any unnecessary characters before the "/" sign.
9. Once the configuration is complete, click the "Run" button in IntelliJ IDEA to start the application. You can choose either normal mode or debug mode.
10. If all the steps have been followed correctly, the server will start successfully.
  Please follow these instructions carefully to launch the project.
