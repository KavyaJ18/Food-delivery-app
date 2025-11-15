🍽️ Online Food Delivery Data Management System (MERN + MongoDB Analytics)

A professional full-stack MERN application designed to manage and analyze online food delivery data using MongoDB, Express, React, and Node.js.
The system stores large datasets such as restaurants, menus, orders, deliveries, and customer feedback while supporting big-data simulation and MongoDB Aggregation Pipeline analytics.

This project demonstrates scalable data handling, backend API design, and meaningful data insights suitable for real-world food delivery platforms.

📌 Key Features
🔹 Data Management

CRUD operations for Restaurants, Menus, Orders, Deliveries, Feedback

Flexible NoSQL schema using MongoDB collections

Real-time order and feedback storage

🔹 Big Data Simulation

Automated generation of 1000+ sample orders using JavaScript loops

Simulates realistic food delivery datasets for performance testing

🔹 Data Analytics

Best-selling dishes

Average delivery time

Customer rating trends

Restaurant performance metrics

All built using MongoDB Aggregation Pipelines

🔹 Full-Stack MERN

Frontend: React.js

Backend: Node.js + Express

Database: MongoDB

Tools: MongoDB Compass, Express Routing, JavaScript ES6

🏗️ Project Structure
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

🚀 Installation & Setup
1️⃣ Clone Repository
git clone https://github.com/yourusername/repo-name.git
cd repo-name

2️⃣ Install Backend
cd backend
npm install

3️⃣ Install Frontend
cd ../frontend
npm install

4️⃣ Add Backend Environment Variables

Create a .env file inside backend:

MONGO_URI=mongodb://localhost:27017/food_delivery_db
PORT=5000
JWT_SECRET=your_secret_key

5️⃣ Start Backend
cd backend
npm start

6️⃣ Start Frontend
cd frontend
npm start

📊 Big Data Generation (mongosh)
for (let i = 1; i <= 1000; i++) {
  db.orders.insertOne({
    order_id: i,
    dish_name: ["Pizza", "Burger", "Pasta"][i % 3],
    quantity: Math.ceil(Math.random() * 3),
    delivery_time: Math.floor(Math.random() * 50) + 20,
    rating: Math.ceil(Math.random() * 5)
  });
}

📈 Sample Analytics Query
db.orders.aggregate([
  { $group: { _id: "$dish_name", totalOrders: { $sum: 1 } } },
  { $sort: { totalOrders: -1 } }
]);

🧭 Future Enhancements

Role-based authentication (Admin/User)

Real-time order tracking

AI-driven recommendations

Admin dashboard for analytics

🏁 Conclusion

This project demonstrates how the MERN stack and MongoDB can be combined to build a scalable, data-driven food delivery management system capable of handling large datasets, performing advanced analytics, and supporting modern web UI.
