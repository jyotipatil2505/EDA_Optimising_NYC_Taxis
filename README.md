# 🚕 Optimising NYC Taxi Operations – EDA Case Study

This project explores and analyzes NYC Yellow Taxi data to uncover patterns, inefficiencies, and opportunities for optimizing taxi operations in New York City.

---

## 📌 Objective

To identify trends, peak demand zones, pricing inefficiencies, and passenger behaviors using Exploratory Data Analysis (EDA) — and provide data-driven recommendations for optimizing dispatching, routing, and fare structures.

---

## 📂 Dataset

- Source: [NYC Taxi & Limousine Commission Open Data](https://www.nyc.gov/site/tlc/about/tlc-trip-record-data.page)
- Format: `.parquet` files containing millions of records
- Fields: pickup/dropoff datetime, location IDs, fare, tip, distance, passenger count, etc.
- Sampled: 5% stratified sampling by hour to downsample and improve analysis efficiency

---

## 🔧 Project Workflow

### 1. Data Preparation
- Combined multi-file dataset (hourly parquet files)
- Downsampled to ~300K entries for analysis

### 2. Data Cleaning
- Removed invalid or missing values
- Handled duplicate/negative values in fares, duration, distance
- Merged redundant columns (e.g., airport fees)
- Standardized categorical variables using mappings

### 3. Outlier Detection
- Applied 99th percentile capping on:
  - `fare_amount`, `fare_per_mile`, `trip_distance`, `tip_amount`, etc.
- Recalculated consistent `fare_amount` and `total_amount`

### 4. Feature Engineering
- Created new variables: `trip_duration`, `fare_per_mile`, `pickup_hour`, `pickup_day_of_week`, etc.

### 5. Exploratory Data Analysis (EDA)
- Pickup patterns by hour, day, and month
- Zone-level trip volume and revenue analysis using GeoPandas
- Revenue vs. distance/time/passenger count
- Payment methods, tips, pricing behavior
- Heatmaps and geospatial trip analysis

---

## 📊 Key Insights

- 🚖 **JFK, Midtown, and Times Square** have the highest taxi demand
- ⏰ Trips peak between **6–8 PM**, especially on **Fridays**
- 💸 **Longer trips** have lower per-mile costs → room for pricing optimization
- 💁‍♀️ Solo passengers pay 6x more per mile than groups → promote ride-sharing
- 🎯 **Tip percentages** are highest on short, evening trips

---


## 📍 Visual Highlights

- Hourly and monthly pickup heatmaps
- Zone-wise trip distribution maps
- Correlation matrices between distance, fare, tip
- Vendor vs. fare comparisons
- Fare per mile variation by time/day


---

## 🛠️ Technologies Used

- Python 3.x
- Pandas, NumPy, Seaborn, Matplotlib
- GeoPandas, Shapely
- Jupyter Notebook
- Parquet + pyarrow
- Git & GitHub

---

## ✅ How to Run

Follow the steps below to set up and run the project locally:

```bash
# 1. Clone the repository
git clone https://github.com/jyotipatil2505/EDA_Optimising_NYC_Taxis_Jyoti_Mitkar.git
cd EDA_Optimising_NYC_Taxis

# 2. Install dependencies
pip install -r requirements.txt

# 3. Launch the notebook
jupyter notebook EDA_Optimising_NYC_Taxis/EDA_Assg_NYC_Taxi_Starter.ipynb

```

---


## 📘 Report Overview
This repository contains the case study report on NYC Taxi Operations, authored by **Jyoti Mitkar**. It includes an in-depth analysis of taxi trends, operational metrics, and data-driven insights.

📄 **Download the Full Case Study Report (PDF):**  
[🔗 Report_NYC_Taxi_Operations_Starter.pdf](https://github.com/jyotipatil2505/EDA_Optimising_NYC_Taxis/blob/main/EDA_Optimising_NYC_Taxis/Report_NYC_Taxi_Operations_Starter.pdf)


---

## 🙋‍♀️ Author

**Jyoti Patil**  
_Data Science Enthusiast | Urban Mobility Analytics_

### 🌐 Connect With Me
- [💼 LinkedIn](https://www.linkedin.com/in/jyoti-patil-9808067a/)  
- [💻 GitHub](https://github.com/jyotipatil2505)

---

## 💬 Feedback & Contributions

Feel free to:

- ⭐ **Star** the repo  
- 🍴 **Fork** it  
- 🛠️ **Raise issues**  
- 📥 **Submit pull requests**

I welcome feedback, collaboration ideas, and contributions to improve the project!
