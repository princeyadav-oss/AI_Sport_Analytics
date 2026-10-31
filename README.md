# 🏆 AI-Powered Sports Analytics & Performance Platform

An AI-powered sports analytics platform built using **Python, TensorFlow/Keras, CNN, ANN, LSTM, and Streamlit**.

The project analyzes sports player data and images to detect players, recognize activities, predict player performance, predict match outcomes, and forecast future performance.

---

## 🚀 Project Overview

**AI Sports Analytics** combines Computer Vision and Machine Learning to provide multiple sports analytics capabilities through an interactive Streamlit application.

### 🤖 AI Modules

| Module | Technology | Purpose |
|---|---|---|
| 👤 Player Detection | CNN | Detect whether an image contains a player |
| 🏃 Activity Recognition | CNN | Recognize player activities |
| 📊 Player Performance Prediction | ANN | Predict player performance score |
| ⚽ Match Outcome Prediction | ANN | Predict Team A win, Team B win, or Draw |
| 📈 Performance Forecasting | LSTM | Forecast the next performance score |

---

## ✨ Features

- 👤 **Player Detection**
  - Upload a sports image
  - Detect Player / Non-Player
  - Display prediction confidence

- 🏃 **Activity Recognition**
  - Upload player image
  - Classify activities such as:
    - Running
    - Walking
    - Shooting
    - Passing
    - Standing

- 📊 **Player Performance Prediction**
  - Enter player statistics
  - Predict overall performance score
  - Uses an Artificial Neural Network

- ⚽ **Match Outcome Prediction**
  - Enter team statistics
  - Predict:
    - Team A Wins
    - Team B Wins
    - Draw
  - Display outcome probabilities

- 📈 **Performance Forecasting**
  - Uses an LSTM model
  - Forecasts the next performance score
  - Displays recent performance trend

- 🖥️ **Interactive Web Application**
  - Built with Streamlit
  - Simple sidebar navigation
  - Real-time predictions

---

## 🧠 Machine Learning Architecture

### 1. Player Detection — CNN

A Convolutional Neural Network is trained to classify images into:

```text
Player
Non-Player
```

Architecture:

```text
Input Image
     ↓
Conv2D
     ↓
MaxPooling
     ↓
Conv2D
     ↓
MaxPooling
     ↓
Conv2D
     ↓
MaxPooling
     ↓
Flatten
     ↓
Dense
     ↓
Output
```

---

### 2. Activity Recognition — CNN

The CNN classifies player activities into five categories:

```text
Running
Walking
Shooting
Passing
Standing
```

Architecture:

```text
Input Image
     ↓
Convolution Layers
     ↓
MaxPooling
     ↓
Flatten
     ↓
Dense Layer
     ↓
Softmax
     ↓
Activity Class
```

---

### 3. Player Performance Prediction — ANN

The ANN uses player statistics such as:

- Speed
- Goals
- Assists
- Pass Accuracy
- Stamina
- Shots
- Tackles

```text
Player Statistics
       ↓
StandardScaler
       ↓
Dense(64)
       ↓
Dense(32)
       ↓
Dense(16)
       ↓
Output
       ↓
Performance Score
```

---

### 4. Match Outcome Prediction — ANN

The model uses:

- Team A Score
- Team B Score
- Team A Possession
- Team B Possession
- Team A Shots
- Team B Shots
- Team A Ranking
- Team B Ranking

Output:

```text
Team B Wins
Team A Wins
Draw
```

---

### 5. Performance Forecasting — LSTM

The LSTM model analyzes a sequence of previous performance scores and predicts the next performance score.

```text
Previous Performance Scores
          ↓
       LSTM 64
          ↓
       LSTM 32
          ↓
       Dense 16
          ↓
       Output
          ↓
Next Performance Score
```

---

## 🛠️ Technologies Used

### Programming
- Python

### Machine Learning
- TensorFlow
- Keras
- Scikit-learn

### Deep Learning
- CNN
- ANN
- LSTM

### Data Processing
- NumPy
- Pandas

### Visualization
- Matplotlib
- Seaborn

### Web Application
- Streamlit

### Development Environment
- Jupyter Notebook
- VS Code
- Git & GitHub

---

## 📂 Project Structure

```text
AI_Sport_Analytics/
│
├── app.py
├── AI_Sport_Analytics.ipynb
├── requirements.txt
│
├── Datasets/
│   ├── player_data.csv
│   ├── performance_data.csv
│   └── match_data.csv
│
├── Models/
│   ├── player_detection.h5
│   ├── activity_model.h5
│   ├── performance_model.h5
│   ├── match_model.h5
│   └── lstm_model.h5
│
└── images/
    ├── player/
    ├── non_player/
    │
    └── activity/
        ├── running/
        ├── walking/
        ├── shooting/
        ├── passing/
        └── standing/
```

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/AI_Sport_Analytics.git
```

### 2. Open the Project

```bash
cd AI_Sport_Analytics
```

### 3. Install Dependencies

```bash
python -m pip install -r requirements.txt
```

---

## ▶️ Run the Streamlit Application

Run:

```bash
python -m streamlit run app.py
```

The application will open at:

```text
http://localhost:8501
```

---

## 📓 Run the Jupyter Notebook

Start Jupyter Notebook:

```bash
jupyter notebook
```

Then open:

```text
AI_Sport_Analytics.ipynb
```

The notebook contains the complete workflow including:

```text
Data Generation
      ↓
Data Analysis
      ↓
Image Preprocessing
      ↓
CNN Training
      ↓
ANN Training
      ↓
LSTM Training
      ↓
Model Evaluation
      ↓
Interactive Dashboard
```

---

## 📊 Datasets

The project currently uses datasets created for the prototype.

### Player Dataset

Contains player information such as:

```text
Player ID
Age
Speed
Goals
Assists
Pass Accuracy
Stamina
Shots
Tackles
```

### Performance Dataset

Contains player statistics and calculated performance scores.

### Match Dataset

Contains:

```text
Match ID
Team Scores
Possession
Shots
Team Rankings
Match Result
```

---

## 📈 Application Workflow

```text
                 AI SPORTS ANALYTICS
                         │
        ┌────────────────┼────────────────┐
        │                │                │
   Computer Vision    Player Data     Match Data
        │                │                │
   ┌────┴────┐       ┌───┴────┐          │
   │         │       │        │          │
Player    Activity Performance Forecast Match
Detection Recognition Prediction       Prediction
   │         │       │        │          │
   CNN       CNN     ANN      LSTM       ANN
   │         │       │        │          │
   └─────────┴───────┴────────┴──────────┘
                         │
                 Streamlit Dashboard
```

---

## 🎯 Future Improvements

- 🎥 Real-time player detection from video
- 📹 Real-time activity recognition
- 🏟️ Real match/video analysis
- 👥 Multiple-player tracking
- 📍 Player position tracking
- 📊 Advanced player comparison
- 🧠 Larger real-world datasets
- ⚡ Real-time prediction dashboard
- ☁️ Cloud deployment
- 📱 Mobile-friendly application

---

## ⚠️ Current Limitations

This is a **prototype/academic project**.

The current datasets are synthetic/demo datasets, and the image datasets are relatively small. Therefore, model predictions should be considered demonstrations of the AI pipeline rather than production-level sports analytics.

The LSTM prototype currently forecasts from the available performance-score sequence rather than a complete historical match-by
