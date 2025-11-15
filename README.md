# 🍽️ Online Food Delivery Data Management System  
### **Full-Stack MERN Application with Big-Data Simulation & MongoDB Analytics**

![MongoDB](https://img.shields.io/badge/Database-MongoDB-green)
![Express](https://img.shields.io/badge/Backend-Express.js-lightgrey)
![React](https://img.shields.io/badge/Frontend-React-blue)
![Node](https://img.shields.io/badge/Runtime-Node.js-green)
![License](https://img.shields.io/badge/License-MIT-yellow)

## 📌 Project Overview
This is a **full-stack MERN project** that manages online food delivery data using **MongoDB, Express, React, and Node.js**.  
It handles restaurants, menus, orders, deliveries, and feedback, with **big-data simulation** using thousands of records.  
The system uses **MongoDB Aggregation Pipelines** to analyze best-selling dishes, delivery performance, and customer behavior trends.

## 🚀 Features
- CRUD operations for food delivery data  
- Big-data simulation (1000+ records)  
- Aggregation pipelines for analytics  
- MERN-based modular architecture  
- MongoDB Compass visualizations  

## 🧩 Tech Stack
- React.js  
- Node.js  
- Express.js  
- MongoDB  
- JavaScript (ES6)  

## 📁 Project Structure
```
/backend
   ├── controllers/
   ├── routes/
   ├── models/
   ├── config/
   └── server.js

/frontend
   ├── src/
   ├── components/
   ├── pages/
   └── App.js
```

## ⚙️ Installation & Setup

### 1️⃣ Clone the Repository
```
git clone https://github.com/yourusername/repo-name.git
cd repo-name
```

### 2️⃣ Backend Setup
```
cd backend
npm install
```

Add `.env`:
```
MONGO_URI=mongodb://localhost:27017/food_delivery_db
PORT=5000
JWT_SECRET=your_secret_key
```

Start backend:
```
npm start
```

### 3️⃣ Frontend Setup
```
cd ../frontend
npm install
npm start
```

## 📦 Big Data Simulation
```
for (let i = 1; i <= 1000; i++) {
  db.orders.insertOne({
    order_id: i,
    dish_name: ["Pizza","Burger","Pasta"][i % 3],
    quantity: Math.ceil(Math.random()*3),
    delivery_time: Math.floor(Math.random()*50)+20,
    rating: Math.ceil(Math.random()*5)
  });
}
```

## 📊 Data Analytics Examples
```
db.orders.aggregate([
  { $group: { _id: "$dish_name", totalOrders: { $sum: 1 } } },
  { $sort: { totalOrders: -1 } }
]);
```

## 🧭 Future Enhancements
- Admin dashboard  
- Authentication  
- AI recommendations  
- Real-time tracking  
- Cloud deployment  

## 📜 License
MIT License
