# 🎬 Movie Success Prediction Using XGBoost

A Flask-based web application that predicts the likelihood of a movie being **Not Successful**, **Average**, or a **Success** using a trained XGBoost model. The application includes secure user authentication, password reset functionality, and a responsive, modern user interface.

---

## 🚀 Features

- 🎥 **Movie Success Prediction**\
  Predicts a movie's success category based on year, duration, genre, director, and lead actor.

- 🔐 **User Authentication**\
  Secure user registration and login using PostgreSQL and Bcrypt for password hashing.

- 🔁 **Password Reset**\
  Simple password recovery system with a demo reset link implementation.

- 🖥️ **Responsive UI**\
  Clean and modern front-end with real-time form validation and mobile-friendly design.

---

## 🧰 Prerequisites

Make sure the following are installed:

- Python 3.8+
- PostgreSQL 13+
- Git

---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/MRNICEGUY10/Movie_Success_Prediction_Using_XGBoost.git
cd Movie_Success_Prediction_Using_XGBoost
```

### 2. Create and Activate Virtual Environment

```bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Set Up PostgreSQL Database

Ensure PostgreSQL is installed and running. Then:

#### Create Database

```sql
CREATE DATABASE movie_app_db;
```

#### Create Users Table

Replace `your_postgres_user` with your PostgreSQL username and run:

```bash
psql -d movie_app_db -U your_postgres_user -c "
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(100) UNIQUE NOT NULL,
  password VARCHAR(255) NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);"
```

### 5. Run the Application

```bash
python app.py
```

Visit the application at:\
🔗 [http://localhost:5000](http://localhost:5000)
