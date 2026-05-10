# 📦 Instagram Store ER Diagram

## 📌 Overview
This project presents the **Entity-Relationship (ER) diagram** for a small Instagram-based business that sells **thrifted fashion items and handmade products**.

The goal of this design is to model a database that can handle:
- Product management  
- Inventory tracking  
- Customer orders  
- Payment handling  
- Shipping lifecycle  

---

## 🧠 Design Approach

The system is designed to reflect real-world business behavior:

- **Thrifted products** are unique (single quantity)  
- **Handmade products** can have multiple units  
- Orders can contain multiple products  
- Customers can place multiple orders  
- Payment and shipping are handled as separate processes  

The database is kept **normalized and scalable**, avoiding unnecessary data duplication.

---

## 🧩 Entities Included

### 1. Customer
Stores customer details such as name, phone number, Instagram handle, and address.

### 2. Product
Represents items being sold, including attributes like:
- type (thrifted / handmade)  
- size, color, condition  
- price and category  

### 3. Inventory
Tracks stock availability:
- Thrifted items → quantity = 1  
- Handmade items → quantity > 1  

### 4. Order
Represents a purchase made by a customer, including:
- order date  
- total amount  
- order status  

### 5. Order_Items (Junction Table)
Handles the many-to-many relationship between orders and products:
- One order can have multiple products  
- One product can appear in multiple orders  

### 6. Payment
Stores payment-related details:
- payment status  
- payment method  
- payment date  

### 7. Shipping
Tracks delivery lifecycle:
- shipping status  
- tracking number  
- shipped and delivered dates  

---

## 🔗 Relationships

- **Customer → Order** → One-to-Many  
- **Order → Order_Items** → One-to-Many  
- **Product → Order_Items** → One-to-Many  
- **Product → Inventory** → One-to-One  
- **Order → Payment** → One-to-One  
- **Order → Shipping** → One-to-One  

---

## 🎯 Key Features of the Design

- Handles both **unique and bulk inventory**  
- Supports **multiple items per order**  
- Separates **payment and shipping logic**  
- Maintains **data consistency and scalability**  
- Captures important business attributes like condition, size, and category  

---

## 🛠 Tools Used
- ER Diagram created using **Eraser**

---

## 📷 Output
The ER diagram image is included in this repository.
<img width="1116" height="1293" alt="Insta_thrift_DB_Design" src="https://github.com/user-attachments/assets/7bab8dbd-6074-4428-8d51-3a57574d70ac" />
---

## 🚀 Conclusion
This design provides a **clean, structured, and scalable database model** suitable for a growing Instagram-based store. It balances simplicity with real-world practicality and allows future expansion.
