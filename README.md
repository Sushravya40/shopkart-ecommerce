# ShopKart

A comprehensive, full-stack e-commerce web application with a modern user interface and a secure, robust backend API.

## 📦 Project Architecture

This is a monorepo containing both the frontend and backend of the ShopKart application.

* **`/backend`** - Java Spring Boot REST API
* **`/frontend`** - React (Vite) User Interface

---

## 🛠️ Tech Stack

**Frontend:**
* React 18
* Vite
* CSS (Custom modern styling)

**Backend:**
* Java 17+
* Spring Boot 3
* Spring Security & JWT (JSON Web Tokens)
* Spring Data JPA (Hibernate)
* MySQL Database
* Razorpay Integration (for Payments)

---

## 🚀 Getting Started

Follow these instructions to set up the project locally on your machine.

### 1. Database Setup
This project uses **Hibernate (spring.jpa.hibernate.ddl-auto=update)**. This means **you do not need a `.sql` schema file**! The application will automatically create all the necessary database tables (Users, Products, Orders, etc.) as soon as you run it.

1. Install [MySQL](https://dev.mysql.com/downloads/).
2. Create a brand new, empty database named `Project`:
   ```sql
   CREATE DATABASE Project;
   ```
3. Open `backend/src/main/resources/application.properties` and update your MySQL username and password if they are different from the defaults:
   ```properties
   spring.datasource.username=your_mysql_username
   spring.datasource.password=your_mysql_password
   ```

### 2. Backend Setup
1. Open a terminal and navigate to the `backend` folder:
   ```bash
   cd backend
   ```
2. Build and run the Spring Boot application using the Maven wrapper:
   ```bash
   # On Windows
   mvnw.cmd spring-boot:run
   
   # On Mac/Linux
   ./mvnw spring-boot:run
   ```
3. The backend API will start securely on `http://localhost:8080`.

### 3. Frontend Setup
1. Open a new terminal and navigate to the `frontend` folder:
   ```bash
   cd frontend
   ```
2. Install the necessary Node.js dependencies:
   ```bash
   npm install
   ```
3. Start the Vite development server:
   ```bash
   npm run dev
   ```
4. The frontend will be up and running at `http://localhost:5173`. Open this URL in your web browser.

---

## ✨ Features

* **User Authentication:** Secure signup and login using JSON Web Tokens (JWT).
* **Product Catalog:** Browse products, view details, and categorize items.
* **Shopping Cart:** Add, remove, and manage items in the cart before checkout.
* **Order Processing & Payments:** Full checkout flow integrated with the Razorpay API.
* **Admin Dashboard:** A dedicated interface for administrators to manage products, categories, and user accounts.
* **Responsive Design:** A beautiful, modern interface that works across devices.

---

## 🔒 Security Note
* Never commit real production database passwords or active Payment API Secret Keys to GitHub.
* If deploying to production, use Environment Variables to inject secrets into `application.properties`.

---

## 📸 Screenshots

*(Add your screenshots here. You can drag and drop images directly into GitHub to upload them!)*

---

## 🔮 Future Enhancements

* **Wishlist:** Allow users to save favorite items for later.
* **Product Reviews & Ratings:** Enable customers to rate and review products.
* **Order Tracking:** Real-time updates for delivery status.
