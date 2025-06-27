# Bookstore-Management-System---Spring-Boot-Application
Overview
This is a Spring Boot web application for managing a bookstore inventory. It allows users to:

View available books

Add new books to the inventory

Maintain a personal book list

Edit and delete book records

Features
Book Management: Full CRUD operations for books

Personal Book List: Users can save books to their personal list

Database Integration: Uses MySQL for persistent storage

Thymeleaf Templates: Server-side rendered HTML views

MVC Architecture: Clear separation of concerns with controllers, services, and repositories

Technologies Used
Backend: Spring Boot 3.5.0

Database: MySQL

ORM: Spring Data JPA (Hibernate)

Templating: Thymeleaf

Build Tool: Maven

Java Version: 17

Application Structure
text
com.bookstore1
├── Bookstore1Application.java       # Main application class
├── controller
│   ├── BookController.java          # Main controller for book operations
│   └── MyBookListController.java    # Controller for personal book list
├── entity
│   ├── Book.java                    # JPA Entity for books
│   └── MyBookList.java              # JPA Entity for personal book list
├── repository
│   ├── BookRepository.java          # Repository for Book entity
│   └── MyBookRepository.java        # Repository for MyBookList entity
└── service
    ├── BookService.java             # Service implementation for books
    └── MyBookListService.java       # Service implementation for personal book list
Database Configuration
The application uses MySQL with these settings (configured in application.properties):

Database name: booksystem

Username: root

Password: root

Tables: Automatically created by Hibernate (Book and MyBooks)

Setup Instructions
Prerequisites
Java 17 JDK

MySQL Server

Maven 3.6+

Installation Steps
Clone the repository:

bash
git clone https://github.com/yourusername/bookstore-management.git
cd bookstore-management
Create a MySQL database:

sql
CREATE DATABASE booksystem;
Update database credentials in src/main/resources/application.properties if needed.

Build and run the application:

bash
mvn spring-boot:run
Access the application at: http://localhost:8083/

Application Endpoints
HTTP Method	Path	Description
GET	/	Home page
GET	/book_register	Book registration form
POST	/save	Save a new book
GET	/available_books	View all available books
GET	/my_books	View personal book list
GET	/mylist/{id}	Add book to personal list
GET	/editBook/{id}	Edit book form
GET	/deleteBook/{id}	Delete a book
GET	/deleteMyList/{id}	Remove from personal list
Screenshots
(Add screenshots of your application's UI here if available)

License
This project is open-source and available under the MIT License.

Contribution Guidelines
Contributions are welcome! Please follow these steps:

Fork the repository

Create a new branch for your feature

Commit your changes

Push to the branch

Create a Pull Request

Known Issues
None currently reported

Future Enhancements
User authentication system

Book search functionality

Book categories and filtering

Shopping cart feature
