
# Cafe Management System

The **Cafe Management System** is a Spring Boot application designed to manage cafe operations such as product management, order processing, and user management. It provides a user-friendly interface for managing cafe items and customer orders while maintaining a robust backend with MySQL for persistent data storage.

## Project Description

The **Cafe Management System** is a full-fledged backend system that allows cafe administrators to:
- Manage menu items such as coffee, snacks, and beverages.
- Process customer orders.
- Track order statuses.

This system is designed to help cafes handle their daily operations more effectively and efficiently.

## Features

- **Product Management:**
  - Add, update, and delete items from the menu.
  - Retrieve all available items or search for a specific item by its ID.
  
- **Order Management:**
  - Place customer orders.
  - View all orders or retrieve details of a specific order.
  - Update the status of an order (e.g., processing, completed).
  - Delete an order if necessary.
  
- **User Interface:**
  - Simple and user-friendly front-end built with HTML for order placement and menu display.

## Technologies Used

- **Backend:**
  - Java
  - Spring Boot (for REST APIs)
  - JPA & Hibernate 
  
- **Frontend:**
  - HTML, CSS
  
- **Database:**
  - MySQL
  
- **Other Tools:**
  - Lombok (to simplify the creation of data objects)
  - Spring Data JPA (to handle database operations)

 **MySQL Setup**:
   - Ensure you have MySQL installed.
   - Create a database named `cafedata`:
     \`\`\`sql
     CREATE DATABASE cafedata;
     \`\`\`

**Run the application**:
   You can run the application using Maven or from your IDE:
   \`\`\`bash
   mvn spring-boot:run
   \`\`\`
 **Access the application**:
   - The application will run at `http://localhost:8000`.
   - You can test the API endpoints using tools like Postman or your browser.

## API Endpoints

The API endpoints enable interaction with cafe items and orders. Below are the available endpoints:

### **Cafe Item Endpoints:**
- **GET /api/items** – Get a list of all cafe items.
- **GET /api/items/{id}** – Get a specific cafe item by its ID.
- **POST /api/items** – Add a new cafe item.
- **DELETE /api/items/{id}** – Delete a cafe item by its ID.

### **Order Endpoints:**
- **GET /api/orders** – Get a list of all orders.
- **GET /api/orders/{id}** – Get a specific order by its ID.
- **POST /api/orders/o** – Create a new order.
- **PUT /api/orders/{id}/status** – Update the status of an existing order (e.g., processing, completed).
- **DELETE /api/orders/{id}** – Delete an order by its ID.

JPA is configured to automatically update the database schema. If you need to modify it manually, adjust the `spring.jpa.hibernate.ddl-auto` property in `application.properties` accordingly.

