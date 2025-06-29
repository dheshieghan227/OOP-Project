# OOP-Project

# Kamal BookStore Inventory Management System

### Authors:
- **DHESHIEGHAN A/L SARAVANA MOORTHY A23CS0072**
- **PRAVINRAJ A/L SIVABATHI A23CS0171**
- **MIKHAIL BIN YASSIN A21EC0053**

---

## SECTION A: PROJECT DESCRIPTION

### 1. Problem Statement and Project Overview

Although online applications and platforms have been widely embraced for book purchases and inventory management, small-town or rural bookshops still depend on conventional, face-to-face interactions. One such bookstore is **Kamal Book Store**.

Mr. Kamal faces many challenges in uplifting his bookstore sales and managing store operations efficiently. He currently uses manual filing to keep track of book records, stock quantity, customer details, and restocking schedules. This results in inventory discrepancies, out-of-stock issues, and difficulties in forecasting demand — ultimately affecting customer satisfaction and business growth.

To address these issues, we propose the **Kamal BookStore Inventory Management System** — a user-friendly and efficient system tailored to streamline the daily operations of Kamal Book Store.

---

## System Objectives

The system is designed for three types of users:
- **Admin (Mr. Kamal)**
- **Book Suppliers**
- **Customers**

### Admin Perspective:
- Reduce the need for additional human resources.
- Automate repetitive and time-consuming tasks.
- Focus on important actions such as adding or editing book information and monitoring stock levels.
- View comprehensive reports such as best-selling books and total profits.
- Place restocking orders efficiently to ensure optimal inventory levels.
- Enjoy secured authentication with restricted access based on user roles.

### Customer Perspective:
- Seamless registration and login process.
- Browse a wide range of book catalogues.
- Add books to cart and view orders with ease.
- Experience a smooth, user-friendly interface.

### Supplier Perspective:
- Secure login access.
- View pending orders placed by the admin.
- Approve or reject orders with ease.
- Quickly search and manage orders.

---

## Conclusion

The Kamal BookStore Inventory Management System enhances operational efficiency for Mr. Kamal’s bookstore. It provides:
- A simple and secure platform for customers to order books.
- A smooth ordering process for both customers and suppliers.
- A centralized and user-friendly inventory management solution for the administrator.

By integrating technology into the bookstore’s workflow, Mr. Kamal can reduce manual work, improve inventory accuracy, increase customer satisfaction, and ultimately boost his bookstore’s profitability.

Implementation of OOP Concepts (Ch5–Ch9)  
1. Encapsulation & Data Hiding (Ch5)  
What We Did:  
Used private attributes with public getter/setter methods to protect internal class data.  

Example:  

class Name {  
    private String fName, lName;  
    public String getFName() { return fName; }  
    public void setFName(String f) { fName = f; }  
}  

Why: To protect internal states and ensure controlled access to object properties.  

2. Inheritance (Ch6)  
What We Did:  
Created a User superclass for shared attributes. Admin, Customer, and BookSupplier extend this base class.  

Example:  

class Admin extends User {  
    private Vector<Book> books;  
    // Uses inherited methods from User  
}  

Why: To promote reusability and establish parent-child relationships between objects.  

3. Polymorphism (Ch7)  
What We Did:  
Used abstract class Menu with overridden methods depending on user type.  

Example:  

abstract class Menu {  
    abstract int viewMenu();  
}  

class Admin extends User {  
    @Override int viewMenu() { /* Admin-specific menu */ }  
}  

Why: To allow different behaviors depending on object types at runtime.  

4. Composition & Aggregation (Ch8)  
Composition:  

A User has a Name object (lifespan is tied).  

Example:  

class User {  
    private Name name;  
    User(...) { name = new Name(fName, lName); }  
}  

Aggregation:  

Admin contains a collection of Book objects (independent entities).  

Example:  

class Admin {  
    private Vector<Book> books; // Books exist outside Admin  
}  

Why: To model part-whole relationships accurately based on ownership strength.  

5. Exception Handling & File Operations (Ch9)  
Exception Handling:  

Prevented crashes using try-catch blocks for file and input-related errors.  

Example:  

try {  
    FileWriter file = new FileWriter("booksDatabase.txt");  
} catch (IOException e) {  
    System.out.println("File error!");  
}  

File Operations:  

Implemented methods like addBooksIntoFile(), readBooksFromFile() for data persistence.  

Why: To ensure error-resilient application behavior and maintain data integrity.


