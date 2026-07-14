# 🏪 ShelfSense – AI-Powered Retail Shelf Intelligence System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-blue.svg"/>
  <img src="https://img.shields.io/badge/YOLOv8-Object%20Detection-red.svg"/>
  <img src="https://img.shields.io/badge/OpenCV-Computer%20Vision-green.svg"/>
  <img src="https://img.shields.io/badge/FastAPI-Backend-009688.svg"/>
  <img src="https://img.shields.io/badge/Streamlit-Dashboard-FF4B4B.svg"/>
  <img src="https://img.shields.io/badge/SQLite-Database-blue.svg"/>
</p>

---

# 📌 Overview

ShelfSense is an AI-powered retail shelf intelligence system that automates inventory monitoring using computer vision. The system detects products from shelf images or live camera feeds, estimates stock levels, identifies low-stock and out-of-stock shelves, and generates real-time inventory insights through an interactive dashboard.

The project combines object detection, backend services, inventory analytics, and decision-making to simulate a real-world smart retail solution.

---

# 🚀 Key Features

- 📷 Real-time shelf monitoring using live camera feeds
- 🎯 Object detection using YOLOv8
- 📦 Detection of 8+ product categories
- 📊 Inventory analytics dashboard
- ⚠️ Automatic low-stock and out-of-stock detection
- 🔄 Rule-based restock recommendations
- 📈 Product-wise inventory statistics
- 💾 Inventory history stored using SQLite
- 🔗 REST API powered by FastAPI
- 🖥️ Interactive Streamlit dashboard

---

# 🏗️ System Architecture

```
                          ShelfSense

                 ┌──────────────────────┐
                 │     Streamlit UI     │
                 │                      │
                 │ Dashboard            │
                 │ Live Detection       │
                 │ Inventory Status     │
                 │ Reports              │
                 │ Analytics            │
                 └──────────┬───────────┘
                            │
                            │ REST API
                            ▼
                 ┌──────────────────────┐
                 │       FastAPI        │
                 │                      │
                 │ API Gateway          │
                 └──────────┬───────────┘
                            │
      ┌─────────────────────┼─────────────────────┐
      │                     │                     │
      ▼                     ▼                     ▼
 Camera Service     Object Detection      Inventory Service
                         Service
      │                     │                     │
      ▼                     ▼                     ▼
 OpenCV Capture        YOLOv8 Model      Inventory Database
                                            (SQLite)
      │                     │
      ▼                     ▼
 Frame Processing     Product Detection
                            │
                            ▼
                    Counting Engine
                            │
                            ▼
                 Inventory Decision Engine
                            │
                            ▼
        In Stock • Low Stock • Out of Stock
        Restock Recommendation
                            │
                            ▼
                Inventory Analytics Engine
                            │
                            ▼
         Trends • Reports • Category Analytics
                            │
                            ▼
                    Streamlit Dashboard
```

---

# ⚙️ Workflow

### Step 1 — Image Acquisition

- Capture images from a webcam or uploaded image using OpenCV.

↓

### Step 2 — Image Processing

- Resize image
- Normalize input
- Convert to YOLO format

↓

### Step 3 — Object Detection

YOLOv8 detects products and returns:

- Product Class
- Bounding Box
- Confidence Score

↓

### Step 4 — Inventory Counting

The counting engine computes:

- Product Count
- Shelf Occupancy
- Empty Shelf Detection

↓

### Step 5 — Decision Engine

Inventory levels are compared against predefined thresholds to classify products as:

- ✅ In Stock
- ⚠️ Low Stock
- ❌ Out of Stock

The system then generates automated restock recommendations.

↓

### Step 6 — Database

Inventory snapshots are stored in SQLite, including:

- Product Information
- Detection History
- Stock Status
- Timestamp

↓

### Step 7 — Analytics Dashboard

Streamlit visualizes:

- Inventory Status
- Product Distribution
- Category Analytics
- Detection History
- Restock Recommendations

---

# 🧠 Technology Stack

| Category | Technologies |
|----------|--------------|
| Programming | Python |
| Computer Vision | OpenCV |
| Object Detection | YOLOv8 |
| Backend | FastAPI |
| Dashboard | Streamlit |
| Database | SQLite |
| APIs | REST API |
| Version Control | Git, GitHub |

---

# 📂 Project Structure

```
ShelfSense/

├── app/
│   ├── main.py
│   ├── routes.py
│   └── config.py
│
├── detection/
│   ├── detector.py
│   ├── inference.py
│   └── preprocessing.py
│
├── decision_engine/
│   ├── inventory_rules.py
│   └── recommendations.py
│
├── analytics/
│   ├── reports.py
│   └── charts.py
│
├── database/
│   ├── models.py
│   └── sqlite.db
│
├── dashboard/
│   └── streamlit_app.py
│
├── datasets/
│
├── models/
│
├── requirements.txt
│
└── README.md
```

---

# 📊 Dashboard Modules

- Live Camera Feed
- Product Detection
- Inventory Overview
- Category Analytics
- Restock Recommendations
- Detection History
- Reports

---

# 🎯 Future Enhancements

- Multi-camera support
- Barcode integration
- OCR-based product recognition
- Cloud database support (PostgreSQL)
- Email/SMS restock alerts
- Product expiry detection
- Employee analytics
- Mobile dashboard

---

# 👨‍💻 Contributors

**Divyanshu Garg**

**Arpit Chouhan**

bejbj-



B.Tech – Artificial Intelligence & Machine Learning

National Institute of Technology Kurukshetra




