🚗 Vehicle Price Prediction
🎯 Objective

The aim of this project is to build a machine learning system that predicts vehicle prices based on specifications such as make, model, year, engine, mileage, transmission, body type, and other features. This system can help buyers and sellers estimate fair market values of vehicles.

📊 Dataset

The dataset contains 1002 vehicle records with 17 features.

Columns Description:

name → Full name of the vehicle (make, model, trim).

description → Brief description including selling points.

make → Manufacturer (e.g., Ford, Toyota, Jeep).

model → Model of the vehicle.

year → Year of manufacture.

price → Price of the vehicle (target variable).

engine → Engine type & specifications.

cylinders → Number of engine cylinders.

fuel → Fuel type (Gasoline, Diesel, Electric, etc.).

mileage → Vehicle mileage.

transmission → Transmission type (Automatic, Manual, CVT, etc.).

trim → Trim level.

body → Body style (SUV, Sedan, Pickup, etc.).

doors → Number of doors.

exterior_color → Exterior color of the vehicle.

interior_color → Interior color.

drivetrain → Drivetrain (All-wheel Drive, FWD, RWD, etc.).

🔎 Data Preprocessing

Handled missing values →

Numeric columns → filled with median.

Categorical columns → filled with mode.

Dropped low-correlation features (year, doors).

Applied OneHotEncoding to categorical features → expanded to 1998 features.

Standardized data with StandardScaler.

📈 Exploratory Data Analysis (EDA)

Distribution plots for numeric features (price, mileage, cylinders).

Correlation heatmap → identified cylinders as moderately correlated with price.

Majority vehicles are SUVs, followed by Pickup Trucks and Sedans.

Fuel types: Gasoline (dominant), Hybrid, Electric, Diesel.

🏗️ Model Building

Two regression models were implemented and compared:

1️⃣ Linear Regression

Simple baseline model.

Performance:

MAE: 5860.56

RMSE: 9964.92

R²: 0.6877

2️⃣ Random Forest Regressor

Ensemble model with better feature handling.

Performance:

MAE: 4501.03

RMSE: 7797.73

R²: 0.8088

✅ Random Forest performed significantly better than Linear Regression.

🔑 Feature Importance (Random Forest)

Top predictors for price include:

make (manufacturer)

model

engine

trim

body type

📊 Results Visualization

Actual vs Predicted plots for both Linear Regression & Random Forest.

Top 10 feature importance plot using Random Forest.

⚙️ Tech Stack

Language: Python 🐍

Libraries: Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn

Models: Linear Regression, Random Forest Regressor

🚀 Future Improvements

Use Gradient Boosting / XGBoost for better accuracy.

Apply feature selection / dimensionality reduction (since OHE expands features).

Build a web app (Flask/Streamlit) for real-time price prediction.

Integrate NLP on descriptions to extract useful signals.
