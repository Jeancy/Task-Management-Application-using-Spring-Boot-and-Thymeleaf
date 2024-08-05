# Task-Management-Application-using-Spring-Boot-and-Thymeleaf

## Overview
This is a full-featured web application for managing tasks, built using Spring Boot and Thymeleaf. The application includes user authentication, task CRUD operations, dynamic content generation, and database integration.

## Features
- User Registration and Login
- Role-based Access Control (Admin, User)
- Create, Read, Update, and Delete (CRUD) operations for tasks
- Task assignment to users
- Task status updates (Pending, In Progress, Completed)
- Dashboard with an overview of tasks
- Filter and search tasks by status, assignee, or due date

## Technologies Used
- **Backend:** Spring Boot, Spring Security, Spring Data JPA
- **Frontend:** Thymeleaf, Bootstrap
- **Database:** MySQL (or PostgreSQL)
- **Build Tool:** Maven

## Getting Started

### Prerequisites
- Java 11 or higher
- Maven
- MySQL (or PostgreSQL) database

### Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/yourusername/task-management-application.git
    cd task-management-application
    ```

2. **Set up the database:**
    - Create a database named `taskdb` in MySQL (or PostgreSQL).
    - Update the `src/main/resources/application.properties` file with your database credentials.

    ```properties
    spring.datasource.url=jdbc:mysql://localhost:3306/taskdb
    spring.datasource.username=yourusername
    spring.datasource.password=yourpassword
    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.thymeleaf.cache=false
    spring.security.user.name=user
    spring.security.user.password=password
    ```

3. **Build and run the application:**
    ```bash
    mvn clean install
    mvn spring-boot:run
    ```

4. **Access the application:**
    Open your browser and navigate to `http://localhost:8080`.

## Usage

### Register
1. Navigate to `http://localhost:8080/register`.
2. Fill in the registration form and submit.

### Login
1. Navigate to `http://localhost:8080/login`.
2. Enter your credentials and login.

### Task Management
- **View Tasks:** Navigate to `http://localhost:8080/tasks` to view all tasks.
- **Create Task:** Click on "Create Task" and fill in the details.
- **Edit Task:** Click on "Edit" next to a task and update the details.
- **Delete Task:** Click on "Delete" next to a task to remove it.

## Project Structure
src
├── main
│ ├── java
│ │ └── com
│ │ └── jeancy
│ │ └── taskmanagement
│ │ ├── TaskManagementApplication.java
│ │ ├── config
│ │ │ ├── SecurityConfig.java
│ │ ├── controller
│ │ │ ├── TaskController.java
│ │ │ ├── UserController.java
│ │ ├── entity
│ │ │ ├── Role.java
│ │ │ ├── Task.java
│ │ │ ├── User.java
│ │ ├── repository
│ │ │ ├── RoleRepository.java
│ │ │ ├── TaskRepository.java
│ │ │ ├── UserRepository.java
│ │ ├── service
│ │ │ ├── TaskService.java
│ │ │ ├── UserService.java
│ ├── resources
│ │ ├── static
│ │ │ ├── css
│ │ │ │ └── styles.css
│ │ ├── templates
│ │ │ ├── dashboard.html
│ │ │ ├── login.html
│ │ │ ├── register.html
│ │ │ ├── tasks
│ │ │ │ ├── create.html
│ │ │ │ ├── edit.html
│ │ │ │ ├── list.html
│ │ ├── application.properties
├── test
└── java
└── com
└── jeancy
└── taskmanagement
├── TaskManagementApplicationTests.java


## Contributing
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a Pull Request.



## Contact
For any questions or feedback, please contact jeancyts@gmail.com.
