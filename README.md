# 🍅 Tomato — Food Ordering System (Low-Level Design)

**Tomato** is a Java-based Low-Level Design (LLD) project that models the core functionality of a food ordering and delivery platform similar to Zomato. It demonstrates how real-world applications can be designed using Object-Oriented Programming (OOP) principles, SOLID-oriented design, and commonly used design patterns.

The project focuses on building a modular, maintainable, and extensible system by separating business logic into models, managers, factories, strategies, and services.

## 🚀 Features

- **Restaurant Search:** Search for restaurants based on location.
- **Menu Management:** Maintain restaurant menus and their food items.
- **Shopping Cart:** Add food items to a cart and calculate the total order cost.
- **Order Management:** Create and manage food orders.
- **Multiple Order Types:** Support delivery and pickup orders.
- **Scheduled Orders:** Support immediate and scheduled order creation.
- **Flexible Payment Methods:** Implement UPI and credit card payments.
- **Order Notifications:** Display order summaries and payment information.
- **Singleton Managers:** Use centralized managers for restaurant and order management.

## 🛠️ Tech Stack

- **Language:** Java
- **Core Concepts:** Object-Oriented Programming (OOP), Abstraction, Encapsulation, Inheritance, and Polymorphism
- **Design Patterns:** Singleton, Factory Method, and Strategy
- **Date and Time:** Java Date-Time API

## 🏗️ Design Patterns Used

### 1. Singleton Pattern
Used in `RestaurantManager` and `OrderManager` to provide a centralized manager instance.

### 2. Factory Pattern
The `OrderFactory` abstraction and its implementations, `NowOrderFactory` and `ScheduledOrderFactory`, create different types of orders without placing all construction logic in the main application flow.

### 3. Strategy Pattern
The `PaymentStrategy` interface allows different payment implementations, including:
- UPI Payment
- Credit Card Payment

This design makes it easier to introduce additional payment methods without changing the core order structure.

## 📂 Project Structure

```text
Tomato-Project/
├── factories/
│   ├── OrderFactory.java
│   ├── NowOrderFactory.java
│   └── ScheduledOrderFactory.java
├── managers/
│   ├── OrderManager.java
│   └── RestaurantManager.java
├── models/
│   ├── User.java
│   ├── Restaurant.java
│   ├── MenuItem.java
│   ├── Cart.java
│   ├── Order.java
│   ├── DeliveryOrder.java
│   └── PickupOrder.java
├── services/
│   └── NotificationService.java
├── strategies/
│   ├── PaymentStrategy.java
│   ├── UpiPaymentStrategy.java
│   └── CreditCardPaymentStrategy.java
├── utils/
│   └── TimeUtils.java
├── Main.java
└── TomatoApp.java
```

## ⚙️ How to Run

### Prerequisites
- Java Development Kit (JDK) 8 or later
- A terminal or Java-compatible IDE

### Steps

**1. Clone the repository**

```bash
git clone <your-repository-url>
```

**2. Navigate to the project directory**

```bash
cd Tomato-Project
```

**3. Compile the Java files**

```bash
javac Main.java TomatoApp.java models/*.java managers/*.java factories/*.java strategies/*.java services/*.java utils/*.java
```

**4. Run the application**

```bash
java Main
```

The application demonstrates a sample food ordering workflow, from searching for a restaurant to selecting menu items, creating an order, processing payment, and displaying an order notification.

## 🎯 Learning Objectives

This project demonstrates how to:

- Apply OOP principles to model real-world entities and their relationships.
- Use design patterns to separate responsibilities and reduce tight coupling.
- Design interchangeable payment strategies.
- Separate data models, business logic, object creation, and notification services.
- Structure a Java application for readability and maintainability.
- Practice LLD concepts commonly discussed in software engineering interviews.

## 🔮 Future Improvements

- Add order cancellation and order status tracking.
- Introduce a menu and restaurant availability system.
- Add discounts, coupons, taxes, and delivery charges.
- Implement stronger validation and exception handling.
- Improve thread safety in Singleton implementations.
- Add unit tests using JUnit.
- Introduce persistent storage using a database.
- Build REST APIs to expose the system's functionality.

## 👩‍💻 Author

Developed as a hands-on project to explore **Low-Level Design, Java, Object-Oriented Programming, and Design Patterns** through a real-world food ordering use case.

---

⭐ If you find this project useful for learning Java LLD and design patterns, consider giving the repository a star!
