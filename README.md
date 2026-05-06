# 🍔 Galle Food Delivery System (C++ DSA Project)

A comprehensive Food Delivery System built entirely in C++ as a **Data Structures and Algorithms (DSA)** project. The application features a robust backend API, a fully functional text-based Console Mode, and a polished modern Web UI. 

All routing and delivery logistics are based on a real-world graph map of **Galle, Sri Lanka**.

## 🚀 Features

* **Dual Interface**: Run as a text-based console application or launch the embedded HTTP server to use the modern browser-based web dashboard.
* **Role-based Dashboards**: Specific views and capabilities for **Users** (browsing, ordering), **Admins** (processing queue, undoing orders), and **Drivers** (viewing assigned orders and delivery routes).
* **Real-time Routing**: Calculates the shortest delivery path from the restaurant to various zones in Galle using Dijkstra's algorithm.

## 🧠 Data Structures Implemented

This project avoids standard library containers where possible to demonstrate fundamental DSA concepts:

1. **Graph (Dijkstra's Algorithm)**: Represents the city map of Galle. Used to calculate the shortest delivery route and distance from the restaurant to the customer.
2. **Hash Map (with Chaining)**: Used for secure user authentication, storing credentials, and managing active sessions.
3. **Doubly Linked List**: Powers the shopping cart, allowing $O(1)$ time complexity for adding items, and utilizing the `prev` pointers for efficient removals.
4. **Trie (Prefix Tree)**: Enables ultra-fast, real-time search functionality for the food menu.
5. **Priority Queue**: Manages the restaurant's order queue. VIP orders are given higher priority and processed before standard orders.
6. **Stack**: Maintains an order history, allowing administrators to "Undo" the last processed order (LIFO).
7. **Sorting (Selection Sort)**: Used in the analytics engine to determine the most popular menu items.

## 🗺️ City Map (Galle, Sri Lanka)

The delivery graph is pre-configured with the following major nodes:
* Galle Restaurant (Start)
* Kalegana & Kahaduwawaththa (Main Junctions)
* Hapugala & Galle Hospital (Hubs)
* Engineering Faculty, Wakwella, Karapitiya Medical Faculty, Allied Health Campus, Hikkaduwa (Delivery Zones)

## 🛠️ Build & Run Instructions

**Prerequisites**: You need `g++` (GCC) installed on your system (e.g., via MSYS2 or MinGW on Windows).

1. **Compile**:
   Run the included build script to compile the project:
   ```cmd
   .\build.bat
   ```
2. **Run**:
   Start the executable:
   ```cmd
   .\food_server.exe
   ```
3. **Interact**:
   * You can use the text-based menu directly in your terminal.
   * Or, press `0` to launch the web server, then open your browser to: **http://localhost:8080/login.html**

## 🔐 Demo Accounts

| Role | Login Instructions |
|---|---|
| **User** | Click "Register", create any username/password, then login. |
| **Admin** | Select the "Admin" role. Password is: `admin123` |
| **Driver** | Select the "Driver" role. Enter ID: `101`, `102`, or `103` |

## 📁 Project Structure

* `/ds/` - Core Data Structure implementations (Graph, Trie, HashMap, Cart, etc.)
* `/models/` - Data models (Order structure)
* `/Services/` - Business logic (Auth, Orders, Drivers)
* `/public/` - Frontend HTML/CSS/JS for the Web UI
* `main.cpp` - Entry point, console UI, and HTTP server routing

---
*Developed for educational purposes to demonstrate the practical application of Data Structures and Algorithms.*
