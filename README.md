# Flight Price Prediction

A machine learning project that predicts airline ticket prices based on flight details such as airline, source, destination, stops, and travel duration.

# Project Overview

This project uses a **Random Forest Regressor** to predict flight prices for Indian domestic airlines. The model was trained on real flight booking data and achieves an **R² score of ~0.82**, meaning it explains about 82% of the variance in ticket prices.

# Dataset

The dataset (`Data_Train.xlsx`) contains the following features:

| Column | Description |
|---|---|
| `Airline` | Name of the airline (e.g. IndiGo, Air India, Jet Airways) |
| `Date_of_Journey` | Date of the flight |
| `Source` | Departure city |
| `Destination` | Arrival city |
| `Route` | Full flight route with stopovers |
| `Dep_Time` | Departure time |
| `Arrival_Time` | Arrival time |
| `Duration` | Total flight duration |
| `Total_Stops` | Number of stops (non-stop, 1 stop, 2 stops, etc.) |
| `Additional_Info` | Extra info about the flight |
| `Price` | **Target variable** — ticket price in INR |

## Technologies Used

- Python 3
- Pandas & NumPy — data manipulation
- Matplotlib & Seaborn — data visualization
- Scikit-learn — machine learning (Random Forest Regressor)
- Pickle — model saving and loading

## Project Workflow

1. **Data Loading** — Load training data from Excel file
2. **Data cleaning** 
3. **Exploratory Data Analysis (EDA)** — Explore and visualize the dataset
4. **Data Preprocessing** — Handle missing values, encode categorical variables, extract features from dates and times
5. **Model Training** — Train a Random Forest Regressor on the processed data
6. **Model Evaluation** — Evaluate using R² score (~0.82)
7. **Model Saving** — Save the trained model using Pickle for future use

##  Model Performance

| Metric | Score |
|---|---|
| R² Score | 0.8167 |

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/airline-project.git
   cd airline-project
   ```

2. Install the required libraries:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn openpyxl
   ```

3. Place the `Data_Train.xlsx` file in the project directory.

4. Open and run the notebook:
   ```bash
   jupyter notebook project_1_airline_.ipynb
   ```

##  Project Structure

```
airline-project/
│
├── project_1_airline_.ipynb   # Main Jupyter notebook
├── Data_Train.xlsx            # Training dataset
├── rf_random.pk1              # Saved Random Forest model
└── README.md                  # Project documentation
```

## 📝 Notes

- The dataset contains flights from Indian cities including Bangalore, Delhi, Kolkata, Cochin, and others.
- Airlines in the dataset include IndiGo, Air India, Jet Airways, Vistara, and more.
- `pickle` is a built-in Python module and does **not** need to be installed via pip.
