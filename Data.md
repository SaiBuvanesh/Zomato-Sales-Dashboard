# 📂 The Data

Let's break down the raw materials that power this dashboard. We worked with six core Excel datasets, each representing a crucial piece of the Zomato ecosystem. 

By tying these tables together, we crafted a robust data model capable of highlighting deep, meaningful trends.

---

## 🗃️ Datasets & Features

### 1. `users.xlsx`
Contains demographic and personal information about the customers.
- **Features:** User ID, Name, Age, Gender, City, Registration Date.
- **Value:** Essential for understanding *who* is ordering. Helps us segment our audience and tailor insights by demographics or geography.

### 2. `restaurant.xlsx`
Details about the restaurants listed on the platform.
- **Features:** Restaurant ID, Name, City, Rating, Cuisine Types, Cost for Two.
- **Value:** Vital for tracking which restaurants are performing best, spotting geographic trends, and grouping by average price point.

### 3. `menu.xlsx`
The bridge between restaurants and the food they serve. 
- **Features:** Menu ID, Restaurant ID, Food ID, Price, Availability.
- **Value:** Allows us to analyze pricing strategies, availability changes, and restaurant-specific offerings across different locales.

### 4. `food.xlsx`
Information about individual food items.
- **Features:** Food ID, Item Name, Category (Veg/Non-Veg), Diet Type.
- **Value:** Powerful for tracking the popularity of specific dishes or food categories over time, understanding shifting consumer palates.

### 5. `orders.xlsx`
The heart of our sales data. Every transaction goes here.
- **Features:** Order ID, User ID, Restaurant ID, Order Date, Total Amount, Rating.
- **Value:** The primary **Fact Table** for calculating revenue, volume flow, user satisfaction, and financial growth over time. 

### 6. `orders_Type.xlsx`
Details on how the order was fulfilled.
- **Features:** Order ID, Fulfillment Type (Delivery, Dine-in, Pickup), Payment Method.
- **Value:** Gives us logistics insights. We can analyze user preferences on delivery versus dine-in, as well as preferred payment channels.

---

## 🏗️ Data Architecture

All these tables are connected inside Power BI using a **Star/Snowflake schema**.
- **The Core (Fact):** `orders` acts as the central hub of our analysis, capturing the events.
- **The Context (Dimensions):** `users`, `restaurant`, `food`, `menu`, and `orders_Type` wrap around the core, allowing us to slice the sales data by any context we need.
