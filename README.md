# Vancouver Rain Forecast - Machine Learning Project

This project is a **machine learning-based weather prediction system** that forecasts rainfall in Vancouver. It leverages real-time weather data from the **Open-Meteo API**, processes the data using **PyTorch**, and serves predictions via a **Flask API**. The frontend displays predictions using **HTML, CSS, and JavaScript**.

## Features

-   **Machine Learning Model**: A Multi-Layer Perceptron (MLP) classifier predicts rainfall categories (No Rain, Light Rain, Moderate/Heavy Rain).
-   **Live Weather Data**: Fetches real-time hourly weather data from the **Open-Meteo API**.
-   **Data Preprocessing**: Normalization, categorization, and aggregation of data.
-   **Flask API**: Provides an endpoint (`/predict`) to serve predictions.
-   **Frontend UI**: Displays predictions and compares them with actual weather data.

## Technologies Used

-   **Python** (Flask, PyTorch, Pandas, NumPy, Open-Meteo API)
-   **JavaScript** (Fetch API for calling Flask backend)
-   **HTML & CSS** (Frontend for displaying predictions)

## Installation & Running Locally

### 1. Clone the Repository

```sh
git clone https://github.com/mujeebullah-khan/rainfall-ML-forecast
cd rainfall-ML-forecast
```
### 2. Install Dependencies

```sh
pip install flask flask-cors torch pandas numpy requests requests-cache retry-requests openmeteo-requests
```

### 3. Run the Flask Server

```sh
python server.py
```


### 4. Run the Frontend

-   Open `index.html` directly in a browser

## How It Works

1.  **Data Fetching**: The Flask server fetches weather data from the Open-Meteo API.
2.  **Preprocessing**:
    -   Normalizes numerical features.
    -   Categorizes rainfall into 3 classes.
    -   Aggregates every 2-hour data points.
3.  **Prediction**:
    -   The MLP model processes the input features.
    -   Outputs a classification (No Rain, Light Rain, Moderate/Heavy Rain).
4.  **Results Display**:
    -   Predictions are served via Flask API.
    -   JavaScript fetches and displays them in `index.html`.
