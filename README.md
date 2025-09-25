# Bike Repositioning Optimization Plan

> Mixed-integer optimization project to improve bike-sharing operations by rebalancing station inventories.  
> Applied to Chicago’s Divvy dataset with insights for Montreal’s BIXI system.

---
## 📝 Overview
Bike-sharing networks often face asymmetric demand: some stations overflow while others empty. This project applies decision analytics to design a repositioning strategy that minimizes cost while improving service availability. Using Divvy data as a proxy for Montreal’s BIXI, we implemented a truck-routing optimization model in Python with Gurobi. Results show that repositioning needs are highly time-dependent, requiring tailored strategies. Sensitivity analysis highlights cost drivers and informs managerial recommendations.

---

## 🎯 Objective • Actions • Tasks • Conclusion

**Objective**  
- Alleviate supply–demand mismatch in bike-sharing systems by minimizing costs of truck-based bike repositioning.  

**Actions**  
- Cleaned and merged Divvy datasets.  
- Explored demand patterns by station and time window.  
- Formulated a MIP with capacity, distance, and penalty constraints.  

**Tasks**  
- Built optimization in Python with Gurobi.  
- Modeled 20 busiest stations in two windows (Mon AM, Wed PM).  
- Ran sensitivity analysis on truck fixed costs and deficit penalties.  

**Conclusion**  
- Morning peaks require light repositioning (low cost).  
- Evening peaks demand intensive, costly rebalancing.  
- Recommended strategy: proactive night moves for mornings; targeted guaranteed-service zones for evenings.  

---

## 🏗️ Architecture

flowchart TD
  A[Raw Data: Divvy Trips + Stations] --> B[Data Cleaning & Exploration]  
  B --> C[Preprocessing: demand, distances, imbalances]  
  C --> D[MIP Model Formulation (Python + Gurobi)]  
  D --> E[Optimization Engine]  
  E --> F[Truck Routes + Station Inventories]   
  F --> G[Cost Analysis & Sensitivity Scenarios]  
  G --> H[Managerial Insights & Recommendations]  

----
## 💡 Why It Matters
- Prevents empty/full stations that frustrate riders.  
- Reduces operational costs through optimized truck routes.  
- Supports sustainable urban mobility in smart cities.  

---

## 🔑 Features
- **Data cleaning & visualization**: trip duration, busiest stations, demand peaks.  
- **Optimization model**: multi-stop truck routing with capacity & penalty costs.  
- **Scenario testing**: Mon AM vs Wed PM peak demand.  
- **Sensitivity analysis**: truck cost vs penalty trade-offs.  
- **Scalable**: adaptable to any dataset/time window.  

---

## ⚙️ Tech Stack
- **Language**: Python 3.10+  
- **Optimization**: Gurobi (via gurobipy)  
- **Data**: pandas, NumPy  
- **Visualization**: matplotlib  
- **Environment**: Jupyter Notebook  
---

## 📂 Project Structure
Bike_Repositionning_Optimization_Plan/  
├─ deliverables/ # Reports & slides  
│ ├─ final_report.pdf  
│ ├─ mip_formulation.pdf  
│ └─ presentation_deck.pdf  
├─ notebooks/ # Jupyter Notebooks with code  
│ ├─ bike_repositionning_monday.ipynb  
│ └─ bike_repositionning_wednesday.ipynb  
├─ LICENSE  
├─ Project_Instructions.pdf  
├─ README.md  
└─ requirements.txt  

---
## 🔄 Reproduce or Extend
Follow the [Quickstart](#-quickstart) to set up the environment.  
You can run the notebooks to replicate our findings or adapt the model to your own dataset.  

👉 Data can be downloaded from the official Divvy system data portal:  
[https://divvybikes.com/system-data](https://divvybikes.com/system-data)  

---
## 🚀 Quickstart

### 1. Clone the repo
```bash
git clone https://github.com/tiphainelevan/Bike_Repositionning_Optimization_Plan.git
cd Bike_Repositionning_Optimization_Plan
```

### 2. Create a virtual environement
 ```bash
python -m venv .venv
source .venv/bin/activate      # On Windows: .venv\Scripts\activate
```

### 3. Install dependencies
``` bash
pip install -r requirements.txt
```

### 4. Run the Notebooks
```bash
jupyter notebook notebooks/
```
open either:
- bike_repositionning_monday.ipynb
- bike_repositionning_wednesday.ipynb








