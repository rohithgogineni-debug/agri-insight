🌾 Agri-Insight
AI-Powered Farmer Market, Weather & Crop Advisory Platform

Agri-Insight is a full-stack, Dockerized, AI-driven agriculture intelligence platform designed to help farmers and agri-stakeholders make informed decisions using live mandi prices, weather forecasts, machine-learning price predictions, and AI-based crop advice.

🚀 Key Features

📊 Live Mandi Prices (AGMARKNET – Government of India)

🌦️ 7-Day Weather Forecast (location-based)

🤖 AI Crop Advisor (weather + crop intelligence)

📈 ML-Based Price Prediction (Random Forest model)

🗺️ Live State → District → Market Selection

🌱 IoT Sensor Data Support (soil moisture, farm data)

⚡ FastAPI Backend with Swagger Docs

🧩 Modular, Production-Grade Architecture

🐳 Fully Dockerized (One-Command Setup)

🧠 System Architecture
React Frontend  →  FastAPI Backend  →  External APIs / ML Models
     │                     │
     │                     ├── AGMARKNET (Live Prices)
     │                     ├── Weather API
     │                     ├── ML Price Prediction
     │                     └── AI Advisory Engine
     │
     └── Docker + Nginx

🛠️ Tech Stack
Backend

Python

FastAPI

Machine Learning (Scikit-learn)

Random Forest Regression

httpx (Async API calls)

Swagger / OpenAPI

Frontend

React.js

Axios

Custom Hooks (Debounced Search)

Responsive UI

DevOps

Docker

Docker Compose

Nginx

Git & GitHub

📂 Project Structure
agri-insight/
├── backend/
│   ├── app/
│   │   ├── routers/
│   │   ├── services/
│   │   ├── ml/
│   │   ├── data/
│   │   └── main.py
│   ├── Dockerfile
│   └── requirements.txt
│
├── frontend/
│   ├── src/
│   ├── public/
│   ├── Dockerfile
│   └── nginx.conf
│
├── docker-compose.yml
└── README.md

🧪 Machine Learning Details

Model: Random Forest Regressor

Training Data: Historical mandi price data (AGMARKNET CSVs)

Prediction Inputs:

Commodity

Market

Output:

Estimated market price

Model is loaded at runtime and served through a FastAPI prediction endpoint.

🐳 Run the Project (Recommended – Docker)
1️⃣ Clone the Repository
git clone https://github.com/ravinda-dot/agri-insight.git
cd agri-insight

2️⃣ Start Everything
docker compose up --build

3️⃣ Access the App

Frontend → http://localhost:3000

Backend API → http://localhost:8000

Swagger Docs → http://localhost:8000/docs

🔍 API Documentation

The backend exposes fully documented REST APIs using Swagger.

Example endpoints:

/api/live-locations/states

/api/prices/live

/api/weather

/api/predict/price

/api/advisor/crop-suggestion

/api/iot/latest-data/{farm_id}

🔐 Security & Best Practices

.env files are excluded from Git

CORS configured for frontend access

Modular router & service layers

Clean separation of concerns

Docker-based environment consistency

🎯 Use Cases

Farmers checking today’s mandi prices

Crop planning based on weather + AI advice

Market trend analysis using ML predictions

IoT-enabled smart farming dashboards

Agriculture data experimentation & research

🧑‍💻 Author

Ravindra
GitHub: https://github.com/ravinda-gogineni

📌 Future Enhancements

Multilingual UI (Indian languages)

Price trend charts & analytics

Authentication & role-based access

Mobile app integration

Cloud deployment (AWS / Render / Railway)

⭐ If you like this project

Give it a ⭐ on GitHub — it motivates continuous improvement!
