Demo - Expense Sharing Application
This is a Spring Boot-based Expense Sharing Application that allows users to manage shared expenses, split costs among multiple people, and track pending payments.
Table of Contents
•	Prerequisites
•	Setup Instructions
•	Running the Application
•	API Endpoints
•	Technologies Used
•	License
Prerequisites
Before you begin, ensure you have the following installed:
•	Java 8 or higher
•	Maven 3.6.3 or higher
•	MySQL (any recent version)
Setup Instructions
Follow these steps to set up the project locally:
1. Clone the Repository
First, clone the repository to your local machine:
git clone https://github.com/HimaVachhani /demo.git
cd demo
2. Set Up MySQL Database
1.	Open your MySQL client or MySQL Workbench and create a new database:

CREATE DATABASE demo_expenses;


2.	(Optional) Create a new MySQL user and grant them privileges:
CREATE USER 'demo_user'@'localhost' IDENTIFIED BY 'password123';
GRANT ALL PRIVILEGES ON demo_expenses.* TO 'demo_user'@'localhost';
FLUSH PRIVILEGES;
3. Configure the Application
In the project, update the src/main/resources/application.properties file with your MySQL credentials:
spring.datasource.url=jdbc:mysql://localhost:3306/demo_expenses
spring.datasource.username=root
spring.datasource.password=Hima123
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
4. Install Project Dependencies
Navigate to the root directory of your project and run the following Maven command to install the necessary dependencies:
mvn clean install
Running the Application
Once the dependencies are installed, you can run the application using the following command:
mvn spring-boot:run
The application will start on http://localhost:8080.
You can also run it via IntelliJ IDEA by right-clicking DemoApplication.java and selecting Run 'DemoApplication'.
Testing API Endpoints
Use Postman or any other API client to test the API endpoints. A few key endpoints are described below.
API Endpoints
1.	User Management
o	POST /api/users: Register a new user
o	GET /api/users/{id}: Get user details by ID
2.	Expense Management
o	POST /api/expenses: Create a new expense
o	GET /api/expenses/{id}: Get details of an expense by ID
o	POST /api/expenses/{id}/settle: Settle the specified expense
Technologies Used
•	Spring Boot: Backend framework
•	MySQL: Relational database for storing users and expenses
•	Hibernate: ORM tool for database interaction
•	Maven: Dependency management
•	JUnit: For testing

