# ShelfSense – AI-Powered Retail Shelf Intelligence System

## Overview

ShelfSense is an AI-powered retail shelf intelligence system that uses computer vision to monitor supermarket shelves automatically. It detects products, counts inventory, identifies out-of-stock items, verifies product placement against a predefined planogram, and provides shelf analytics to help retail staff maintain well-stocked and organized shelves.

## Features

* Product detection using YOLO
* Automatic inventory counting
* Out-of-stock detection
* Planogram (shelf layout) verification
* Shelf compliance reporting
* Interactive Streamlit dashboard
* Inventory analytics and reporting

## Tech Stack

| Category                | Technologies     |
| ----------------------- | ---------------- |
| Programming Language    | Python           |
| Computer Vision         | OpenCV           |
| Object Detection        | Ultralytics YOLO |
| Dashboard               | Streamlit        |
| Data Processing         | Pandas           |
| Visualization           | Matplotlib       |
| Image Processing        | Pillow           |
| Deep Learning Framework | PyTorch          |

## Project Structure

```text
ShelfSense/
│
├── dataset/
├── images/
├── outputs/
├── models/
├── detect.py
├── count.py
├── planogram.py
├── app.py
├── requirements.txt
└── README.md
```

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/ShelfSense.git
cd ShelfSense
```

Install the required packages:

```bash
pip install -r requirements.txt
```

## Usage

### 1. Add Shelf Images

Place shelf images inside the `images/` directory.

### 2. Detect Products

```bash
python detect.py
```

The processed image with detected products will be saved in the `outputs/` directory.

### 3. Count Inventory

```bash
python count.py
```

Example output:

```text
Bottle : 12
Can    : 8
Snack  : 15
```

### 4. Verify Shelf Layout

```bash
python planogram.py
```

The system compares detected products with the expected shelf arrangement and reports misplaced products.

### 5. Launch the Dashboard

```bash
streamlit run app.py
```

## Workflow

```text
Shelf Image
      │
      ▼
Product Detection (YOLO)
      │
      ▼
Inventory Counting
      │
      ▼
Out-of-Stock Detection
      │
      ▼
Planogram Verification
      │
      ▼
Shelf Compliance Report
      │
      ▼
Streamlit Dashboard
```

## Future Enhancements

* OCR-based price tag recognition
* Barcode detection
* Real-time video processing
* Multi-camera support
* Low-stock prediction
* REST API using FastAPI
* Cloud deployment
* Email or SMS alerts
* Historical inventory analytics

## Applications

* Retail stores
* Supermarkets
* Convenience stores
* Warehouses
* Smart retail automation

## Sample Output

The system detects products on store shelves, counts inventory automatically, identifies out-of-stock and misplaced items, and generates shelf compliance reports through an interactive dashboard.

## Author

Developed as a computer vision and deep learning project using Python, OpenCV, YOLO, and Streamlit.
