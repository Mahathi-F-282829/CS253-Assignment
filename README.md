# Car Rental Management System

## Overview
This Car Rental Management System is a comprehensive solution designed to facilitate the management of car rentals. Built using C++ and integrating MongoDB for data persistence, the system offers functionalities for customers, employees, and managers to rent cars, return cars, and manage user and car records effectively.

## Features
- **Customer Management:** Customers can rent cars, return them, and view their rental records.
- **Employee Management:** Employees have the capability to rent cars with special discounts, return cars, and access their rental records.
- **Car Management:** Add, update, and delete car records. Cars can be rented and returned, with their availability status being tracked.
- **Database Integration:** Utilizes MongoDB to store and manage user (customer and employee) and car data securely.
- **Authentication:** Verifies customer, employee, and manager credentials to ensure secure access to the system.

## Prerequisites
- MongoDB server (local or cloud)
- MongoDB C++ Driver installed and configured with your C++ development environment
- C++17 compiler

## Setup and Installation
1. **MongoDB Setup:**
   - Ensure that MongoDB is installed and running on your system. You can use MongoDB Atlas for a cloud-based setup.
   - Create a database named `carRentalDB` and collections `customers`, `employees`, and `cars`.

2. **Environment Setup:**
   - Make sure you have a C++17 compatible compiler.
   - Install the MongoDB C++ Driver. Follow the official MongoDB C++ Driver [installation guide](https://mongodb.github.io/mongo-cxx-driver/mongocxx-v3/installation/).

3. **Configuration:**
   - Update the MongoDB connection string in the `main` function to point to your MongoDB instance.

## Usage
Compile the project using your C++ compiler. For example, if you are using `g++`, you can compile the project as follows:
```bash
g++ -o carRentalSystem main.cpp -std=c++17 -lmongocxx -lbsoncxx
## Key Features

- **User Authentication**: The system includes a verification mechanism for customers, employees, and managers to log in using their IDs and passwords.
- **Car Management**: Administrators can add, update, delete, and view all cars in the system. Cars have attributes like model, condition, and rental status.
- **Customer and Employee Profiles**: Customers and employees can view their profiles, rent cars, return cars, and view their rental records. Customers have a limit on how many cars they can rent based on their customer record, and employees have a similar mechanism with an employee record.
- **Managerial Functions**: Managers have the authority to perform database operations for cars, customers, and employees, such as adding, updating, and deleting records in the database.
- **Database Integration**: The system is integrated with MongoDB, a NoSQL database, to store and retrieve data about users, cars, and transactions. It demonstrates how to connect to a MongoDB database, perform CRUD operations, and manage data efficiently.

## Classes and Their Functions

- **User**: An abstract class representing a generic user of the system with attributes like name, ID, and password. It declares virtual functions for renting and returning cars, and showing user information.
- **Customer and Employee**: Derived classes from User, implementing the virtual functions and adding specific attributes like rentedCars, fineDue, and record (customerRecord for customers and employeeRecord for employees).
- **Car**: Represents a car in the system, with attributes including model, condition, other details, rental status, and due date for return.
- **Manager**: A class derived from User representing a manager with managerial functions.
- **Database**: Handles database operations, connecting to MongoDB, and performing CRUD operations for cars, customers, and employees. It includes functions for verifying user credentials and displaying all records.

## Main Function

The main function serves as the entry point for the application. It initializes the database connection, creates objects for cars, customers, employees, and provides a menu-driven interface for users to interact with the system based on their roles. Users can log in as customers, employees, or managers and perform actions according to their permissions.

## MongoDB Integration

The project uses MongoDB C++ Driver for database interactions. It demonstrates establishing a connection to a MongoDB database, creating BSON documents for data storage, and executing queries to add, update, delete, and retrieve data from the database.

## Conclusion

This Car Rental System project is an example of an object-oriented application in C++ that integrates with a NoSQL database. It showcases the principles of inheritance, polymorphism, database management, and system design.
