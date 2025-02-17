# Korporate Kitchen

**Korporate Kitchen** is an online food delivery system developed using Spring Boot, Hibernate (JPA), and JSP. The application simulates the end-to-end process of ordering food online and includes separate modules for users, restaurants, delivery agents, and administrators.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Application Flow & Endpoints](#application-flow--endpoints)
- [Database Schema](#database-schema)
- [Troubleshooting](#troubleshooting)
- [License](#license)

## Features

- **User Module:**
  - User registration and login.
  - Home dashboard showing available restaurants.
  - Restaurant menu browsing and adding items to cart.
  - Cart, payment gateway, and order placement with order confirmation.
  - Order history and repeat order functionality.
  - Remarks feature: view and add user remarks.

- **Restaurant Module:**
  - Restaurant registration and login.
  - Dashboard for managing menu items, viewing orders, and bank details.
  - Full CRUD operations for master menu items.

- **Delivery Module:**
  - Delivery agent registration and login.
  - Dashboard displaying orders awaiting delivery.
  - Delivery profile and order status update (e.g., marking orders as delivered).

- **Admin Module:**
  - Admin portal and dashboard for managing users, restaurants, and delivery agents.

## Technologies Used

- **Backend:** Spring Boot, Spring Data JPA, Hibernate, Maven
- **Frontend:** JSP, JSTL, Bootstrap, Font Awesome
- **Database:** MySQL

## Project Structure
KorporateKitchen
├── src
│   ├── main
│   │   ├── java
│   │   │   └── com.example.demo
│   │   │       ├── controller
│   │   │       │   ├── UserController.java
│   │   │       │   ├── RestaurantController.java
│   │   │       │   ├── DeliveryController.java
│   │   │       │   └── AdminController.java
│   │   │       ├── model
│   │   │       │   ├── User.java
│   │   │       │   ├── Restaurant.java
│   │   │       │   ├── Order.java
│   │   │       │   ├── Cart.java
│   │   │       │   ├── MasterMenuItem.java
│   │   │       │   ├── Payment.java
│   │   │       │   ├── Bank.java
│   │   │       │   ├── Delivery.java
│   │   │       │   └── Remark.java
│   │   │       ├── repository
│   │   │       │   ├── UserRepository.java
│   │   │       │   ├── RestaurantRepository.java
│   │   │       │   ├── OrderRepository.java
│   │   │       │   ├── CartRepository.java
│   │   │       │   ├── MasterMenuItemRepository.java
│   │   │       │   ├── PaymentRepository.java
│   │   │       │   ├── BankRepository.java
│   │   │       │   ├── DeliveryRepository.java
│   │   │       │   └── RemarkRepository.java
│   │   │       ├── service
│   │   │       │   ├── UserService.java
│   │   │       │   ├── RestaurantService.java
│   │   │       │   ├── OrderService.java
│   │   │       │   ├── CartService.java
│   │   │       │   ├── MasterMenuItemService.java
│   │   │       │   ├── PaymentService.java
│   │   │       │   ├── BankService.java
│   │   │       │   ├── DeliveryService.java
│   │   │       │   └── RemarkService.java
│   │   │       └── service/impl
│   │   │           ├── UserServiceImpl.java
│   │   │           ├── RestaurantServiceImpl.java
│   │   │           ├── OrderServiceImpl.java
│   │   │           ├── CartServiceImpl.java
│   │   │           ├── MasterMenuItemServiceImpl.java
│   │   │           ├── PaymentServiceImpl.java
│   │   │           ├── BankServiceImpl.java
│   │   │           ├── DeliveryServiceImpl.java
│   │   │           └── RemarkServiceImpl.java
│   │   ├── resources
│   │   │   └── application.properties
│   │   └── webapp
│   │       └── WEB-INF
│   │           └── jsp
│   │               ├── index.jsp
│   │               ├── login.jsp
│   │               ├── register.jsp
│   │               ├── homeDashboard.jsp
│   │               ├── userOrders.jsp
│   │               ├── restaurantMenu.jsp
│   │               ├── cartDashboard.jsp
│   │               ├── paymentGateway.jsp
│   │               ├── confirmPayment.jsp
│   │               ├── deliveryPortal.jsp
│   │               ├── deliveryLogin.jsp
│   │               ├── deliveryRegister.jsp
│   │               ├── deliveryRegisterSuccess.jsp
│   │               ├── deliveryDashboard.jsp
│   │               ├── deliveryProfile.jsp
│   │               ├── adminDashboard.jsp
│   │               ├── remarks.jsp
│   │               └── addRemark.jsp
└── pom.xml


## Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone <repository-url>
   cd KorporateKitchen

2 .Database Setup:

Ensure MySQL is installed and running.
Use the provided SQL schema (available in the repository) to create the database (e.g., korporatekitchen10 or korporatekitchen11).
Update database credentials in src/main/resources/application.properties if needed

Application Flow & Endpoints
User Module
Home Page: http://localhost:8036/
User Login: http://localhost:8036/login
User Registration: http://localhost:8036/register
Home Dashboard: http://localhost:8036/user/home
User Profile: http://localhost:8036/user/profile
View Restaurant Menu: http://localhost:8036/user/restaurantMenu?restaurantId=<id>
View Cart: http://localhost:8036/user/cart
Payment Gateway: http://localhost:8036/user/payment
Order Confirmation: http://localhost:8036/user/confirmPayment
User Orders: http://localhost:8036/user/orders
Remarks: http://localhost:8036/user/remarks
Add Remark: http://localhost:8036/user/addRemark
Logout: http://localhost:8036/user/logout
-------------------------------------------------
Restaurant Module
Restaurant Portal (Login/Register): http://localhost:8036/restaurant/portal
Restaurant Login: http://localhost:8036/restaurant/login
Restaurant Registration: http://localhost:8036/restaurant/register
Restaurant Dashboard: http://localhost:8036/restaurant/dashboard
Manage Menu: http://localhost:8036/restaurant/manageMenu
View Restaurant Menu: http://localhost:8036/restaurant/restaurantMenu?restaurantId=<id>
View Orders: http://localhost:8036/restaurant/orders
Bank Details: http://localhost:8036/restaurant/bank
Logout: http://localhost:8036/restaurant/logout
-----------------------------------------
Delivery Module
Delivery Portal (Login/Register): http://localhost:8036/delivery/portal
Delivery Login: http://localhost:8036/delivery/login
Delivery Registration: http://localhost:8036/delivery/register
Delivery Dashboard: http://localhost:8056/delivery/dashboard
Delivery Profile: http://localhost:8036/delivery/profile
Logout: http://localhost:8036/delivery/logout
--------------------------------------------
Admin Module
Admin Portal (Login/Register): http://localhost:8036/admin/portal
Admin Dashboard: http://localhost:8036/admin/dashboard
(Additional admin endpoints as configured)
-----------------------------------------------
Database Schema
The database schema is provided as an SQL file in the repository. It includes tables for:

Users, Admins, Delivery Agents, Restaurants
Master Menu Items
Orders, Payment, Bank, Delivery, Remarks, User Favorites, Cart, Order History, and Notifications

