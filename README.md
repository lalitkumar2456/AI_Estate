AI-Estate: Real Estate Price Prediction System

A full-stack machine learning project for predicting real estate prices using the California Housing dataset, powered by FastAPI (backend) and Streamlit (frontend).
The project integrates Hugging Face Transformers, PyTorch/TensorFlow, and a database for storing predictions.

📌 Features

Data Preprocessing & Analytics – Cleaning, feature engineering, and exploratory analysis.

Machine Learning Model – Trained using scikit-learn / PyTorch / TensorFlow.

FastAPI Backend – Provides prediction API endpoints.

Streamlit Frontend – User-friendly web app for input and visualization.

Secure Configuration – .env & config.py manage Hugging Face token, secret key, DB URL.

Database Integration – Store user inputs and predictions.

⚙️ Tech Stack

Frontend: Streamlit

Backend: FastAPI (served with Uvicorn)

ML Frameworks: PyTorch / TensorFlow, Hugging Face Transformers

Database: PostgreSQL / SQLite

Environment Management: Python venv + pip

📂 Project Structure
AI_Estate/
│── backend/                 # FastAPI backend
│   ├── api/
│   │   ├── endpoints.py     # API routes
│   │   ├── models.py        # ML models
│   │   ├── database.py      # DB connection
│   ├── main.py              # FastAPI entrypoint
│
│── frontend/                # Streamlit app
│   ├── app.py               # Streamlit entrypoint
│
│── config.py                # Config (HF token, DB URL, secret key)
│── requirements.txt         # Python dependencies
│── README.md                # Project documentation
│── .env                     # Environment variables

🔑 Configuration

Create a .env file in project root:

HF_TOKEN=your_huggingface_token_here
SECRET_KEY=your_secret_key_here
DATABASE_URL=postgresql://user:password@localhost:5432/ai_estate


Your config.py should load from .env.

🚀 Installation
# 1. Clone the repo
git clone https://github.com/yourusername/AI_Estate.git
cd AI_Estate

# 2. Create virtual environment
python -m venv venv
source venv/bin/activate   # macOS/Linux
venv\Scripts\activate      # Windows

# 3. Install dependencies
pip install -r requirements.txt

▶️ Running the Project
Start FastAPI Backend
uvicorn backend.main:app --reload


By default, runs at:
👉 http://127.0.0.1:8000

Start Streamlit Frontend
cd frontend
streamlit run app.py
