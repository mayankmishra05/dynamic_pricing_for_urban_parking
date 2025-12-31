# 🚗 **REAL-TIME DYNAMIC PARKING PRICING SYSTEM**
================================================

**Project Type:** Real-Time Data Analytics & Pricing Optimization  
**Core Skills Demonstrated:** Streaming Data | Demand Modeling | Visualization | Pricing Strategy

------------------------------------------------

## 📌 **PROJECT OVERVIEW**
------------------------

This project implements a **real-time dynamic pricing system for urban parking lots** using live-streamed data.  
The system intelligently adjusts parking prices based on **demand signals, congestion indicators, and nearby competition**, simulating how pricing engines operate in modern **smart-city and mobility platforms**.

The entire solution is built **fully in Python** and runs in **Google Colab**, using:

• **Pathway** for real-time data streaming  
• **Bokeh** for interactive, live price visualizations  

🎯 **Objective:**  
Optimize parking utilization and pricing by dynamically responding to real-world conditions such as occupancy, traffic, queue length, and competitive pressure.

------------------------------------------------

## 🔍 **KEY FEATURES**
---------------------

✔ Real-time data ingestion using **Pathway streaming pipelines**  
✔ Three pricing strategies implemented and compared  
✔ Demand normalization with bounded pricing logic  
✔ Competitive pricing using geographic proximity (latitude–longitude)  
✔ Live, interactive price trend visualization using **Bokeh**

------------------------------------------------

## 🧠 **PRICING MODELS IMPLEMENTED**
---------------------------------

### 📈 **MODEL 1: BASELINE LINEAR PRICING (REFERENCE MODEL)**

A simple rule-based pricing model where parking price increases proportionally with occupancy.

Used strictly as a **benchmark** to evaluate advanced pricing strategies.

**Simplified Formula:**  
Price = Base Price + α × Occupancy Rate

**Purpose:**  
Provides a baseline with no demand awareness.

------------------------------------------------

### 📊 **MODEL 2: DEMAND-BASED PRICING (CORE MODEL)**

This model dynamically adjusts prices using a **composite demand score** derived from multiple real-world factors:

• Occupancy rate  
• Queue length  
• Traffic conditions (Low / Medium / High)  
• Vehicle type (Car / Bike / Truck)  
• Special day indicator (Holiday / Event)

**Demand Score (Normalized 0–1):**  
Demand = w₁·Occupancy + w₂·Queue + w₃·Traffic + w₄·Vehicle + w₅·SpecialDay

**Price Constraints:**  
Minimum Price: ₹5  
Maximum Price: ₹25  

✔ Reacts faster to congestion  
✔ More stable during peak hours  

------------------------------------------------

### 📍 **MODEL 3: COMPETITIVE PRICING (MARKET-AWARE MODEL)**

Introduces **competitive intelligence** by factoring in nearby parking lots.

• Uses latitude–longitude data  
• Adjusts price relative to nearby competitors  
• Prevents overpricing when alternatives exist  

**Logic Used:**  
• Distance-based comparison (Haversine approach)  
• Competitor occupancy-based price adjustment  

------------------------------------------------

## 📊 **NUMERICAL HIGHLIGHTS**
----------------------------

Simulated Parking Records     : 1,000+  
Pricing Models Implemented   : 3  
Price Range                 : ₹5 – ₹25  
Demand Score Range          : 0 – 1  
Data Ingestion Mode         : Real-time Streaming  
Visualization Engine        : Bokeh  

**Observed Outcomes:**  
✔ Demand-based pricing reduced price volatility  
✔ Competitive pricing prevented extreme price spikes  
✔ Higher average utilization during peak traffic periods  

------------------------------------------------


## 📂 **PROJECT STRUCTURE**
--------------------------

dynamic_pricing_for_urban_parking.ipynb  
→ Main notebook with all models and visualizations  

dynamic_pricing_for_urban_parking.csv  
→ Simulated real-time parking dataset  

requirements.txt  
→ Project dependencies  

README.md  
→ Project documentation  

------------------------------------------------

## 📈 **VISUALIZATIONS**
-----------------------

All visualizations are created using **Bokeh**:

✔ Real-time pricing trend plots  
✔ Model 1 vs Model 2 comparison  
✔ Competitive pricing behavior visualization  

(Animated or static based on Colab performance)

------------------------------------------------

## 🧪 **ASSUMPTIONS**
--------------------

• Prices are bounded between ₹5 and ₹25  
• Demand scores are normalized between 0 and 1  
• Data is streamed using Pathway to simulate live input  
• Traffic, vehicle type, and special-day flags influence demand  
• Geographic proximity determines competitive pressure  

------------------------------------------------

## ▶️ **HOW TO RUN**
-------------------

1. Open `dynamic_pricing_for_urban_parking.ipynb` in Google Colab  
2. Upload `dynamic_pricing_for_urban_parking.csv`  
3. Install required packages:

!pip install pathway==0.6.6 bokeh==3.4.1 pandas==2.2.2 numpy==1.24.4

4. Run all notebook cells sequentially  
5. Observe live pricing updates in Bokeh plots  

------------------------------------------------

## 🏗 **ARCHITECTURE FLOW**
--------------------------

Parking Data CSV  
→ Pathway Streaming Engine  
→ Model 1 (Linear Pricing UDF)  
→ Model 2 (Demand-Based Pricing UDF)  
→ Model 3 (Competitive Pricing UDF)  
→ Output Streams  
→ Bokeh Visualizations  
→ Final Model Comparison Dashboard  

------------------------------------------------

## 💡 **WHY THIS PROJECT MATTERS**
---------------------------------

This project demonstrates strong hands-on capability in:

✔ Real-time data streaming  
✔ Demand modeling & pricing optimization  
✔ Data-driven decision-making  
✔ End-to-end analytics pipeline design  
✔ Live visualization of analytical outputs  

