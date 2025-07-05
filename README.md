# 🌆 Smart City Analysis

A data-driven analysis project focusing on improving urban living conditions by studying traffic patterns, accident zones, and air pollution levels across a smart city framework.

---

## 📌 Project Objective

To analyze and visualize datasets related to:

- 🚗 Traffic congestion patterns  
- ⚠️ Road accidents and high-risk zones  
- 🌫️ Air pollution concentration levels  

The goal is to extract insights that can guide smart city planning, improve citizen safety, and optimize city resources.

---

## 🛠 Tools & Technologies

- **Power BI** – for dashboards and KPI visualizations  
- **Python (Pandas, Seaborn)** – for data cleaning and charting  
- **Excel** – for initial data merging and filtering  

---

## 📊 Data Sources

- [🚦 Traffic Flow Report](https://drive.google.com/file/d/15AJcpva0xW4FcQ1XDwZHvVgtcn78KANq/view?usp=sharing)  
- [🛣️ Road Accident Logs](https://drive.google.com/file/d/1kqqTtBh7NlUtnmKUPGcFLGRrq-t4UEdi/view?usp=sharing)  
- [🌫️ Air Pollution Levels](https://drive.google.com/file/d/12l7Q-tmy3ZrnliCZlSLMuAIJZnIcJWHZ/view?usp=drive_link)  

---

## 🧠 Key DAX Measures Used

```DAX
-- Total number of recorded accidents
Total Accidents = COUNT('Road Accident Dataset'[Accident_ID])

-- Average Air Quality Index
Average AQI = AVERAGE('Air Pollution Dataset'[AQI])

-- Count of fatal accidents only
Fatal Accidents = 
CALCULATE(
    COUNT('Road Accident Dataset'[Accident_ID]),
    'Road Accident Dataset'[Severity] = "Fatal"
)

-- Percentage of High Congestion Levels
High Congestion % = 
DIVIDE(
    COUNTROWS(
        FILTER('Traffic Condition', 'Traffic Condition'[Congestion_Level] = "High")
    ),
    COUNTROWS('Traffic Condition')
)

-- Average speed recorded in traffic
Average Speed = AVERAGE('Traffic Condition'[Speed])

## 🔍 Key Insights

- 🚦 **Traffic**: Identified peak traffic hours (8–10 AM, 5–8 PM) and major bottlenecks in Tier 1 cities
- ⚠️ **Accidents**: High-risk zones were mapped near intersections with poor visibility and high congestion
- 🌫️ **Air Pollution**: Found strong correlation between traffic volume and spikes in AQI (PM2.5, NO2)
- 🏙️ **Urban Planning**: Tier 2 and Tier 3 cities had better average air quality but poorer road safety metrics
- 📈 **Insight Impact**: Dashboard allows policymakers to prioritize resources toward high-risk locations

