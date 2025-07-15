# Transaction Viewer Application

## Overview
This is a Spring Boot web application that allows users to view and explore financial transaction data. The application provides a simple interface to browse through transactions, view transaction details, and distinguish between credit and debit transactions.

## Features
- View a list of all transactions sorted by date
- See transaction details including ID, date, retailer, and amount
- Distinguish between credit (funds in) and debit (funds out) transactions
- Responsive web interface with clean, easy-to-read tables

## Technology Stack
- Java
- Spring Boot
- Thymeleaf templates
- HTML/CSS

## Getting Started

### Prerequisites
- Java 8 or higher
- Maven

### Setup
1. Clone this repository
2. Navigate to the project directory
3. Run the application using Maven:
   ```
   mvn spring-boot:run
   ```
4. Open your browser and navigate to `http://localhost:8080/transactions`

## Application Structure
- **Domain**: Contains the Transaction model class
- **Repository**: Handles data access and loading transactions from the serialized file
- **Service**: Provides business logic and connects controllers with repositories
- **Controller**: Handles HTTP requests and returns appropriate views
- **Templates**: Thymeleaf HTML templates for rendering the UI

## API Endpoints
- `GET /transactions` - Returns a page displaying all transactions
- `GET /transactions/{id}` - Returns a page displaying details for a specific transaction

## Important Notes

### Package Name
All of the Java packages are `com.codercampus...` instead of `com.coderscampus...`. This is technically a valid package name, but it differs from the standard naming convention used in other related projects. When working with this application, please use `com.codercampus...` for your package names.

### Dependency on Binary File
This project is entirely dependent upon a binary file named `doNotTouch` located in `src/main/resources/doNotTouch/`. If this file is moved, renamed, or changed, the Transaction.java class will not work and the project will fail to run as intended.

You can test this by running the unit tests provided. If they fail, the file may have been moved or renamed. Note that the tests will not fail if you change the internals of this binary file.

The rest of this project follows standard conventions for a Spring Boot web application.
