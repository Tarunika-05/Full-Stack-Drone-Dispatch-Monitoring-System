# 🚁 **Drone Delivery DBMS**
### *Full-Stack Drone Delivery Tracking & Management Platform*

---

## 📌 **Overview**

The **Drone Delivery DBMS** is a full-stack logistics management system designed to handle drone delivery operations.  
It includes modules for managing:

* 🛩️ **Drones** — fleet status, battery, max load  
* 👨‍✈️ **Operators** — certifications & contact details  
* 📦 **Packages** — dimensions, priority, sender/receiver  
* 🚚 **Deliveries** — assignment + status tracking  
* 🏠 **Addresses** — sender/receiver lookup  

Built using **React + Vite** (frontend) and **Node.js + Express + PostgreSQL** (backend).

---

## 🧱 **Tech Stack**

### **Frontend**
* React 19  
* React Router DOM  
* Vite  
* Tailwind CSS  
* ESLint  

### **Backend**
* Node.js (ES Modules)  
* Express 5  
* PostgreSQL (`pg`)  
* dotenv, cors  

### **Database Tables**
* drone  
* operator  
* package  
* delivery  
* address  
* delivery_package (junction table)

---

## 📂 **Project Structure**

    DBMS/
    │
    ├── frontend/                     # React + Vite SPA
    │   ├── src/
    │   │   ├── components/
    │   │   │   ├── Dashboard.jsx
    │   │   │   ├── Drones.jsx
    │   │   │   ├── Operators.jsx
    │   │   │   ├── Deliveries.jsx
    │   │   │   └── Packages.jsx
    │   │   ├── App.jsx
    │   │   └── main.jsx
    │   ├── index.html
    │   └── package.json
    │
    └── server/                       # Node.js backend
        ├── server.js                 # API routes + Express config
        ├── db.js                     # PostgreSQL Pool connection
        ├── operations.js             # SQL logic for all modules
        └── package.json

---

## 🚀 **Features**

### 🛩️ *Drone Module*
* Add, edit, delete drones  
* Update battery, capacity, status  
* Track availability in real time  

### 👨‍✈️ *Operator Module*
* Manage certified drone operators  
* Update contact details  

### 📦 *Package Module*
* Register packages with dimensions, weight, priority  
* Link sender/receiver addresses  

### 🚚 *Delivery Module*
* Assign drone + operator  
* Update delivery status  
* Auto-clean related delivery_package records  

### 🏠 *Address Module*
* Centralized sender/receiver address list  

### 📊 *Dashboard*
* Drone, operator, package, delivery counts  
* Status summaries  
* Quick navigation cards  

---

## 🛠️ **Installation & Setup**

### **1️⃣ Backend Setup**

    cd server
    npm install
    node server.js

Create a `.env` file:

    DB_HOST=your-host
    DB_PORT=5432
    DB_NAME=your-db
    DB_USER=your-user
    DB_PASSWORD=your-password
    PORT=5000

---

### **2️⃣ Frontend Setup**

    cd frontend
    npm install
    npm run dev

Frontend URL:  
👉 http://localhost:5173

Backend URL:  
👉 http://localhost:5000

---

## 🔌 **API Endpoints**

### **Drones**
    GET    /drones
    POST   /drones
    PUT    /drones/:id
    DELETE /drones/:id

### **Operators**
    GET    /operators
    POST   /operators
    PUT    /operators/:id
    DELETE /operators/:id

### **Packages**
    GET    /packages
    POST   /packages
    PUT    /packages/:id
    DELETE /packages/:id

### **Deliveries**
    GET    /deliveries
    POST   /deliveries
    PUT    /deliveries/:id
    DELETE /deliveries/:id

### **Addresses**
    GET    /addresses

---

## 🎯 **Typical Workflow**
* View system overview in Dashboard  
* Add drones & operators  
* Register packages with details  
* Assign deliveries  
* Track delivery status  

---

## 📘 **Future Improvements**
* JWT authentication  
* Map integration (Google Maps API)  
* Real-time drone telemetry  
* Analytics dashboard  
* Auto-assignment algorithm  

---
