# 🚖 NYC Rideshare Data Analysis Using PySpark

## 📌 Project Overview

This project analyzes **80GB of NYC rideshare data** to gain insights into **fare structures, passenger demand, and urban mobility patterns**. By leveraging **Google Cloud Platform (GCP) and PySpark**, the project efficiently processes large-scale datasets and applies **machine learning techniques** to extract valuable insights.

### **Key Highlights**
- ✅ **Processed 80GB of rideshare data** using **PySpark** for scalable analysis.
- ✅ **Implemented Gradient Boosting Regression**, achieving an **R² of 0.7** to predict **base passenger fares**.
- ✅ **Used PageRank Algorithm** to identify the most densely populated and high-traffic areas at different times of the day.
- ✅ **Enabled data-driven decision-making** for **rideshare companies and urban planners**.

---

## 📂 Dataset Details

- **Source:** NYC Rideshare Data (2017-2024)
- **Size:** 80GB (processed 50GB for training and validation)
- **Features:**
  - `pickup_datetime`: Timestamp of ride pickup
  - `dropoff_datetime`: Timestamp of ride dropoff
  - `pickup_location`: Geospatial coordinates of pickup points
  - `dropoff_location`: Geospatial coordinates of dropoff points
  - `passenger_count`: Number of passengers in the ride
  - `fare_amount`: Total fare charged for the ride
  - `trip_distance`: Total trip distance (miles)
  - `payment_type`: Payment method used (cash, credit, etc.)

---

## 🏗️ Data Processing & Feature Engineering

✔ **Data Cleaning:**
- Removed **duplicate records** and handled **missing values**.
- Converted timestamps to **datetime objects** and extracted **hour, day, and month** features.
- Filtered out **outliers** (e.g., negative fares, excessive trip distances).

✔ **Feature Engineering:**
- Created **rush-hour flags** to analyze demand spikes.
- Generated **geospatial clusters** using H3 indexing for location-based analysis.
- Engineered **distance-based fare estimations** to enhance model accuracy.

---

## 📊 Machine Learning Models & Techniques

### **1️⃣ Gradient Boosted Regression (GBRT)**
- **Objective:** Predict **base passenger fares**.
- **Implementation:** Used `pyspark.ml.regression.GBTRegressor`.
- **Performance:**
  - **R² Score:** 0.7
  - **MAE (Mean Absolute Error):** $1.15
  - **RMSE (Root Mean Squared Error):** $2.3
- **Insights:**
  - Distance, trip time, and passenger count **strongly correlate with fares**.
  - Peak-hour rides tend to have **higher surge pricing**.

### **2️⃣ PageRank Algorithm for Location Analysis**
- **Objective:** Identify the most frequently visited areas and analyze traffic patterns.
- **Implementation:** Applied **PageRank on ride origin-destination (OD) pairs** to detect **hotspots of activity**.
- **Key Findings:**
  - **Times Square & Midtown Manhattan** are **top-ranked pickup locations**.
  - **Morning rush hour (7-9 AM) and evening rush (5-8 PM) see the highest rideshare demand**.

---

## 🚀 Technologies Used

| **Technology**  | **Purpose** |
|---------------|-------------|
| **PySpark** | Data processing & machine learning |
| **Google Cloud Platform (GCP)** | Cloud storage & computation |
| **H3 Indexing** | Geospatial clustering |
| **PageRank Algorithm** | Identifying high-demand regions |
| **Gradient Boosting Regression** | Predicting fare amounts |

---

## 📈 Key Insights & Business Impact

📌 **Fare Prediction Optimization:**  
- Using **Gradient Boosting Regression**, rideshare companies can **predict fares** based on distance and passenger demand, improving pricing strategies.

📌 **Peak Demand Identification:**  
- The **PageRank analysis** helps **optimize ride availability** in high-traffic zones, reducing **wait times** and improving **fleet management**.

📌 **Urban Planning Recommendations:**  
- The insights from this study can assist **city planners** in **optimizing public transportation routes** and improving congestion control.

---

## 🏗️ Future Work

🔹 **Deep Learning for Fare Prediction:** Explore **LSTMs and Transformer models** to capture **sequential dependencies** in rideshare trends.  
🔹 **Real-Time Demand Forecasting:** Integrate **live data streams** for dynamic rideshare pricing recommendations.  
🔹 **Weather & Traffic Impact Analysis:** Add **weather and real-time traffic conditions** to enhance demand forecasting accuracy.  

---

## 🔧 How to Run the Project

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/nyc-rideshare-analysis.git
   cd nyc-rideshare-analysis

