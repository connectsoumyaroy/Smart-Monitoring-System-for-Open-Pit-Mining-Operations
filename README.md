# 🚜 Open-Pit Mining Operations Optimization – Capstone Project

This project is part of a Supply Chain Analytics Capstone initiative focused on improving operational efficiency in open-pit mining through advanced data analysis and real-time monitoring solutions.

## 📌 Synopsis

The open-pit mine is facing problems of inefficient production and is losing customers' trust as they are unable to meet demands despite no surge in order volume. Due to the vast expanse of the mine, operators cannot manually track all activities in real-time.

As an analyst at Smart Consultancy, I was approached to build a smart live monitoring system and uncover the root causes of production inefficiency. This included tracking ground-level operations, equipment usage, and cycle movement across diggers, trucks, and crushers.

## 🎯 Problem Statement

- Understand operational challenges using client-shared mining data
- Clean and preprocess data in a non-technical, stakeholder-friendly format
- Load data into MySQL Workbench and write stored procedures to derive KPIs
- Create live dashboards (Tableau) to visualize key metrics and trends
- Present findings in a professional presentation to senior stakeholders

## 🔄 Data Methodology

1. **Data Cleaning & Preprocessing**  
   - Raw datasets (`CycleData.csv`, `DelayData.csv`, `LocationData.csv`) were cleaned in Python (Jupyter Notebook)
   - Exploratory data analysis performed using Pandas and visualization libraries

2. **MySQL Workbench (8.0)**  
   - Cleaned tables imported into MySQL
   - Stored procedures created to calculate equipment metrics and enable fast querying

3. **Key KPI Formulas (OEE Components)**  
   - **Availability** = (Net Available Time - Downtime) / Net Available Time  
   - **Performance** = (Operating Time - Speed Losses) / Operating Time  
   - **Quality** = (Net Operating Time - Defect Losses) / Net Operating Time  
   - **OEE** = Availability × Performance × Quality

4. **Tableau Dashboarding**  
   - Integrated SQL output with Tableau dashboards
   - Visualized key metrics: Equipment Production, Efficiency, Accuracy, Defects, and Performance Tiers

## 🛠️ Tools & Technologies

| Tool       | Usage                                |
|------------|--------------------------------------|
| **Python** | Data cleaning, preprocessing         |
| **Pandas** | Data wrangling, summarization        |
| **MySQL**  | Data structuring, stored procedures  |
| **Tableau**| Dashboard creation, KPI visualization|
| **Excel**  | Exploratory analysis and validation  |

## 📂 Dataset Overview

- `CycleData.csv`: Records of truck cycles including durations, routes, and payloads
- `DelayData.csv`: Equipment-level delay logs with timestamped causes
- `LocationData.csv`: Geo-coordinates of mining points (diggers, crushers, stockpiles)

## 📊 Key Insights

- **Truck Classes** handled ~90% of operational load but had only ~51% availability
- Machines like **DZ8085** and **GR7000** had high cycle durations, reducing throughput
- Loaders **EX8047**, **EX7021**, and **EX7026** ranked highest in loading accuracy
- Auxiliary vehicles had the highest defect ratios and lowest operational efficiency

## ✅ Recommendations

- Prioritize preventive maintenance on high-downtime machines (e.g., EX5108, WL6011)
- Optimize truck routing to reduce fuel consumption per cycle
- Maintain buffer queues at both digger and crusher ends to prevent production halts

## 📈 Dashboard Preview

> A dynamic Tableau dashboard was developed to track:
> - Equipment availability and performance
> - Real-time cycle monitoring
> - Loading accuracy
> - Downtime analytics by machine type

*(Screenshots or link to Tableau Public if hosted)*

## 📁 Project Structure

```bash
.
├── data/
│   ├── CycleData.csv
│   ├── DelayData.csv
│   └── LocationData.csv
├── scripts/
│   ├── OPEN_PIT_MINING_CAPSTONE_PROJECT.ipynb
│   └── Open_Pit_Mining_Capstone_Project.sql
├── presentation/
│   ├── Capstone_Presentation_With_Notes.pptx
│   └── Final_Presentation_Script_SoumyaRoy.pdf
└── README.md
