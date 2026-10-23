# 📦 Inventory Management System

A web-based inventory and order management application built with **Python, Flask, and MongoDB**, featuring user authentication, inventory operations, order processing, and graph-based delivery route optimization.

## 📌 Overview

The Inventory Management System provides a web interface for managing products, tracking stock quantities, and processing orders.

The application combines a Flask backend, MongoDB database, and frontend interface. It also includes graph algorithms for finding routes between factories, warehouses, and users.

## ✨ Features

### 🔐 User Authentication

* User registration and login.
* Password hashing for stored user credentials.
* Session-based access control for protected pages.
* Password validation during registration.

### 📦 Inventory Management

* Create and retrieve inventory records.
* Update and delete products.
* Search products by name, category, or description.
* Track stock quantities and product information.
* Record creation and update timestamps.

### 🚚 Order Management

* Process factory-to-warehouse orders.
* Process warehouse-to-user orders.
* Validate product availability before dispatch.
* Update inventory quantities during supported order operations.
* Store order records in MongoDB.

### 🗺️ Route Optimization

* Dijkstra's algorithm for shortest-path calculations.
* Kruskal's algorithm for minimum spanning tree calculations.
* Graph-based representation of factories, warehouses, and users.
* Nearby-user searches based on route distances.

### 🌐 Web Interface

* Flask-rendered HTML pages.
* CSS styling and JavaScript functionality.
* Dashboard, inventory, orders, routes, login, and signup pages.

## 🛠️ Technologies Used

| Technology     | Purpose                        |
| -------------- | ------------------------------ |
| Python         | Application logic              |
| Flask          | Web application and routing    |
| MongoDB        | Database                       |
| PyMongo        | MongoDB integration            |
| HTML           | Page structure                 |
| CSS            | Styling                        |
| JavaScript     | Frontend interactions          |
| Flask-CORS     | Cross-origin resource handling |
| Git and GitHub | Version control                |

## 📂 Project Structure

```text
Inventory-Management-System/
├── app.py
├── requirements.txt
├── test_api.py
├── users.json
├── backend/
│   ├── algorithms/
│   │   ├── graph.py
│   │   ├── mst.py
│   │   └── order_routing.py
│   ├── config/
│   │   ├── config.py
│   │   ├── database.py
│   │   └── init_db.py
│   ├── models/
│   │   ├── inventory.py
│   │   └── order.py
│   └── routes/
│       └── inventory.py
├── frontend/
│   ├── static/
│   │   ├── css/
│   │   └── js/
│   └── templates/
└── README.md
```

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/bramhayyachar018/Inventory-Management-System.git
cd Inventory-Management-System
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate the environment on Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

Install Flask-CORS if it is not already included in the dependency file:

```bash
pip install flask-cors
```

**Dependency note:** The current application imports `flask_cors`, but the provided `requirements.txt` does not list `flask-cors`. Add it to `requirements.txt` so fresh installations work correctly.

### 4. Configure MongoDB

Make sure MongoDB is running locally or that you have access to a MongoDB deployment.

Create a `.env` file in the project root:

```env
MONGO_URI=mongodb://localhost:27017
MONGO_DBNAME=inventoryDB
SECRET_KEY=replace_with_a_long_random_secret
```

For MongoDB Atlas, use your database connection string as `MONGO_URI`.

Keep your `.env` file private. Never commit database credentials or production secrets to GitHub.

### 5. Run the application

```bash
python app.py
```

The application is configured to use port `5000` in its local API test script. Check the startup configuration in `app.py` if the server uses a different port.

Open the local address displayed by the application in your browser.

## 🧪 API Testing

The repository includes `test_api.py`, a script that sends requests to the inventory API.

After starting the application, open another terminal and run:

```bash
python test_api.py
```

The script attempts to create a test inventory item and retrieve inventory records.

The test script uses `requests`, so install it if needed:

```bash
pip install requests
```

## 🧠 Algorithms Implemented

### Dijkstra's Shortest-Path Algorithm

Used to calculate shortest paths between locations represented in a weighted graph.

### Kruskal's Minimum Spanning Tree Algorithm

Used to select edges with minimum total weight without introducing cycles, using a Union-Find data structure.

These algorithms demonstrate how graph theory can be applied to logistics and delivery-routing problems.

## 🎯 Learning Outcomes

* Developing a web application with Flask.
* Integrating Python applications with MongoDB.
* Implementing session-based authentication.
* Designing inventory and order-processing operations.
* Working with REST-style API endpoints.
* Applying graph algorithms to route optimization.
* Testing API requests using Python.

## 👨‍💻 Author

**Bramhayya Achari**

GitHub: [bramhayyachar018](https://github.com/bramhayyachar018)

