# StockSense

**StockSense** is an AI-powered stock trading platform that empowers investors with real-time insights, automated trading, sentiment analysis, and advanced portfolio management. The project is modular, consisting of four main components:

- **Frontend**: Modern React-based dashboard and UI.
- **Backend**: FastAPI backend for trading logic, signals, and data APIs.
- **Model**: Deep learning models for stock price prediction.
- **Sentiment Analysis**: NLP models for market sentiment from news and social media.

---

## Table of Contents

- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Tech Stack](#tech-stack)
- [License](#license)

---

## Features

- 📈 **Stock Price Prediction**: ML/DL models for future price forecasting.
- 📰 **Sentiment Analysis**: Real-time sentiment from news and tweets.
- 🛠️ **Automated Trading Signals**: Buy/Sell/Neutral recommendations.
- 💼 **Portfolio Management**: Track and analyze your investments.
- 🌐 **Live Market Data**: Real-time indices and stock prices.
- 🔒 **Authentication**: Secure login and signup.
- 🎨 **Modern UI**: Responsive dashboard with charts and insights.

---

## Project Structure

```
StockSense/
├── Backend_StockSense/           # FastAPI backend & trading logic
├── Frontend_StockSense/          # React dashboard & UI
├── Model_StockSense/             # Deep learning models & API
├── Sentiment_Analysis_StockSense/# NLP sentiment analysis & API
```

- **Backend**: [Backend_StockSense/README.md](Backend_StockSense/README.md)
- **Frontend**: [Frontend_StockSense/README.md](Frontend_StockSense/README.md)
- **Model**: [Model_StockSense/README.md](Model_StockSense/README.md)
- **Sentiment Analysis**: [Sentiment_Analysis_StockSense/README.md](Sentiment_Analysis_StockSense/README.md)

---

## Getting Started

### 1. Clone the Repository

```sh
git clone https://github.com/yourusername/StockSense.git
cd StockSense
```

### 2. Setup Backend

```sh
cd Backend_StockSense
python -m venv .venv
.venv\Scripts\activate
pip install -r app/requirements.txt
uvicorn app.main:app --reload --port 8000
```

### 3. Setup Model API

```sh
cd Model_StockSense
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python src/etl_pipeline.py
python src/model.py --db_path data/stock_data.db --ticker AAPL --epochs 50 --batch_size 32
uvicorn api.main:app --reload --port 8001
```

### 4. Setup Sentiment Analysis API

```sh
cd Sentiment_Analysis_StockSense
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python src/model.py
uvicorn api.main:app --reload --port 8002
```

### 5. Setup Frontend

```sh
cd Frontend_StockSense
npm install
npm run dev
```

---

## Tech Stack

- **Frontend**: React, TypeScript, Tailwind CSS, Vite
- **Backend**: FastAPI, Python
- **Model**: TensorFlow/Keras, scikit-learn
- **Sentiment Analysis**: NLTK, scikit-learn, FastAPI
- **Database**: SQLite (for model training)
- **APIs**: RESTful endpoints for integration

---

## License

This project is licensed under the MIT License.
