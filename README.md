# 🌊 Climate change Alert System

**Tech Stack:** Next.js · FastAPI · Python · Scikit-learn · Leaflet · MySQL

## 🚀 Overview

The Coastal Threat Alert System is an intelligent, real-time monitoring and early-warning platform designed to protect coastal regions from:

- 🌪 Cyclones
- 🌊 Storm Surges
- 🏖 Coastal Erosion
- 🧪 Water Pollution
- 🚨 Illegal Coastal Activities

It combines AI/ML predictions with geospatial visualization to provide alerts and actionable insights for vulnerable coastal zones.

---

## 🔧 Features

- **Real-Time Map Interface:** Live threat markers using Mapbox, color-coded (Green: Safe, Yellow: Warning, Red: Alert).
- **Dynamic API Integration:** Every 10 seconds, fetches latest sensor and model predictions from FastAPI.
- **Smart Alert System:** Triggers notifications based on threat level, region, and severity.
- **Threat Popups:** Detailed view of each location with timestamp, threat type, intensity, and recommended action.
- **ML Models:** Trained models to predict cyclone formation, pollution level, erosion risk, and storm surge potential.

---

## 📦 Project Structure
/BACKEND
├── CYCLONE_MODEL
├── POLLUTION_MODEL
├── COASTALEROSION_MODEL
├── STORM_MODEL
└── shared utils & APIs
/FRONTEND
└── Next.js app with Mapbox integration


---

## 🧠 Machine Learning

Each model uses historical and sensor data:
- `RandomForestClassifier` for cyclone formation
- Pollution risk level classified by chemical indicators (pH, COD, BOD, etc.)
- Erosion prediction based on wind, wave, and coastal structure data

---

## 🗺️ Leaflet Integration

- Receives JSON API data every 10s
- Icons/Markers change color dynamically
- Flash animation on high-risk zones
- Popups show: **Threat Type**, **Timestamp**, **Intensity**, **Region**, **Action**

---

## ⚙️ Setup Instructions

1. **Clone Repo**
   ```bash
   git clone https://github.com/your-username/Coastal-Threat-Alert-System.git
   cd Coastal-Threat-Alert-System

2. Start Backend (FastAPI for each model)
   uvicorn CYCLONE_MODEL.cyclone_app:app --port 8001 --reload
uvicorn POLLUTION_MODEL.pollution_app:app --port 8002 --reload
uvicorn COASTALEROSION_MODEL.coastalErosion_app:app --port 8003 --reload
uvicorn STORM_MODEL.storm_app:app --port 8004 --reload

3.Start Frontend
cd FRONTEND
npm install
npm run dev

📈 Future Enhancements

Integration with IoT sensor hardware

SMS/email alert system

User dashboard with login & threat history

AI-based illegal activity detection from satellite images


