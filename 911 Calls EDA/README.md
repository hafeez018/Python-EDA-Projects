# 🚨 911 Calls EDA

An exploratory data-analysis project focused on analyzing 911 emergency call data to uncover patterns, trends, and insights in call volumes and responses.

---

## 📌 Project Overview

This project carries out a full EDA workflow: loading and cleaning the 911 call dataset (timestamps, locations, types of emergencies, response times), conducting a variety of univariate and multivariate analyses, creating derived features (time-of-day, weekday/weekend), visualising trends, and summarising key insights. The goal is to understand call patterns and help emergency services better allocate resources.

---

## 🧰 Tech Stack

* **Language:** Python
* **Libraries:** pandas, numpy, matplotlib, seaborn
* **Environment:** Jupyter Notebook / Google Colab

---

## 🔄 Workflow Summary

### 1. Data Collection

Dataset containing 911 call records: features such as call timestamp, call type (fire, medical, traffic, etc.), location (city/neighbourhood), response times, and possibly incident outcome.

### 2. Exploratory Data Analysis (EDA)

* Distribution of call volumes by emergency type, time of day, weekday vs weekend
* Visualisations: heatmaps or bar charts of incident count by hour and by day, location clusters of high‐volume zones
* Analysis of response time distributions and their relation to call type or location
* Correlation and joint plots of features like response time vs call type, time of day
* Identifying missing data, outliers (e.g., extreme response times), and skewed distributions

### 3. Feature Engineering & Insights

* Extracted time features: hour, day of week, weekend flag
* Categorised incident types into broader groups if necessary
* Calculated derived metrics: calls per hour/day per neighbourhood, average response time per incident type and location
* Visualised peak call hours, hotspot locations, and incident type trends
* Examined temporal patterns — e.g., increased medical calls late night, traffic incidents during peak hours

### 4. Key Analytical Findings

* Certain types of incidents concentrated by hour (e.g., traffic calls during rush hour, medical emergencies at late night)
* Locations (zones/neighbourhoods) show clusters of high call volume and longer response times
* Weekend vs weekday patterns differ for incident type mix and call volumes
* Response time varies by incident type and location, suggesting resource allocation opportunities
* Seasonality/holiday spikes may exist in call volumes (if dataset includes date span)

### 5. Business/Operational Recommendations

* Resource planning: Increase staffing or ambulances/call units during peak hours and in hotspot zones
* Incident type prioritisation: Faster response lines or dedicated units for high-risk call types (medical vs traffic)
* Location route optimisation: Dispatch centres closer to high-volume hotspots to reduce response times
* Data-powered scheduling and shift planning: align workforce with observed call peaks and types

---

## 📁 Project Structure

```
911-Calls-EDA/
│── data/
│── notebooks/
│── src/
│── README.md
│── requirements.txt
```

---

## 📈 Key Findings

* Peak call hours typically occurred during evening and late night for medical emergencies
* Traffic and accident-related calls peaked during commute hours
* Specific neighbourhoods consistently generated higher call volumes, often with longer response times
* Derived features like “hour of day” and “neighbourhood call rate” significantly improved insight quality
* EDA supports emergency services in shifting from reactive to proactive resource deployment

---

## 🚀 Future Improvements

* Integrate external datasets: weather, event schedules, holidays to explain spikes in call volume
* Incorporate geospatial visualisations (heatmaps, interactive maps) to better identify location clusters and dispatch optimisation
* Build dashboards (Plotly, Streamlit) for real-time monitoring of call patterns and response-time analytics
* Extend to predictive modelling: forecast call volumes by type and location, enabling proactive resource allocation
* Perform anomaly detection for unusual incidents or call volume surges, triggering alerts for emergency planners
