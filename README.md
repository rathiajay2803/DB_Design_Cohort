# 🛍️ Thrift & Handmade Instagram Store – ER Diagram

## 📌 Overview

This project contains the Entity-Relationship (ER) diagram for a small-scale Instagram-based e-commerce business that sells:

- Thrifted fashion items (unique, single-piece products)
- Handmade products (multi-quantity, batch-produced items)

Initially, orders are managed via Instagram DMs and WhatsApp, but as the business grows, a structured database design is required to handle:

- Product management
- Inventory tracking
- Customer orders
- Payments
- Shipping and delivery tracking

---

## 🎯 Objective

The goal of this ER diagram is to design a **normalized and scalable database structure** that supports:

- Unique and reusable inventory models
- Order and product relationships
- Customer management
- Payment tracking
- Shipping lifecycle

---

## 🧩 Entities Included

The following core entities are part of the system:

### 1. Customer
Stores customer details such as:
- Name, email, phone
- Address information
- Purchase behavior (VIP, last purchase date)

---

### 2. Orders (orders_history)
Represents each order placed by a customer:
- Linked to a customer
- Contains pricing, discount, and delivery info
- Tracks cancellations

---

### 3. Order Items (order_item)
Junction table to support:
- Many-to-many relationship between orders and products
- Stores quantity and price at purchase time

---

### 4. Product
Represents items being sold:
- Supports both **thrift** and **handmade**
- Includes attributes like size, color, condition, price, brand

---

### 5. Inventory
Handles stock management:
- Tracks available quantity
- Supports both unique and bulk items
- Decoupled from product for flexibility

---

### 6. Shipping Details
Tracks delivery lifecycle:
- Status (pickup → delivered)
- Tracking ID
- Delivery timestamps
- Damage and delay tracking

---

### 7. Payment
Handles transaction records:
- Payment mode (UPI, cash, etc.)
- Success/failure status
- Linked to orders

---

## 🔗 Relationships & Cardinality

- One **Customer** can place multiple **Orders**
- One **Order** can contain multiple **Products** (via Order Items)
- One **Product** can appear in multiple **Orders**
- One **Order** has one **Shipping Detail**
- One **Order** can have multiple **Payments**
- One **Product** can have multiple **Inventory records**

---

## 🧠 Key Design Decisions

- **Order Items** used as a junction table to support many-to-many relationship
- **Inventory separated from Product** for better stock management
- **Support for unique thrift items and bulk handmade items**
- **Shipping and Payment handled as separate entities** for flexibility
- **Normalized schema to avoid redundancy and inconsistency**

---

## 📷 Diagram

👉 The ER diagram is included in this repository / linked board.

---

## 🚀 Future Improvements

- Support for multiple shipments per order
- Product variants (size/color combinations)
- Coupon and promotion system
- Return and refund management
- Inventory locking to prevent overselling

---

## 🛠️ Tools Used

- Eraser / Draw.io / Excalidraw (whichever you used)

---

## 📌 Notes

This design is intended for **real-world scalability** while keeping the system simple enough for a growing small business.

---

## 👨‍💻 Author

Ajay Rathi