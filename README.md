# 💎 Diamond Price Prediction using Machine Learning & Deep Learning

## 📌 Project Overview
This project implements an end-to-end machine learning pipeline to predict diamond prices using a dataset of over 50,000 samples. The workflow covers data preprocessing, feature engineering, model training, evaluation, and optimization using both classical machine learning algorithms and deep learning models.

The objective is to compare multiple regression techniques and identify the most accurate and robust model for price prediction.

---

## 📊 Dataset Description
The dataset contains structured information about diamonds, including both numerical and categorical features:

### Features:
- **Numerical:** carat, depth, table, x, y, z  
- **Categorical:** cut, color, clarity  

### Target:
- `price` (continuous variable)

---

## ⚙️ Methodology

### 1. Data Preprocessing
- Handled missing values using **SimpleImputer (median strategy)**
- Converted categorical variables using **OneHotEncoder**
- Applied feature scaling using:
  - StandardScaler
  - MinMaxScaler (custom scaling approach)

A full preprocessing pipeline was built using:
- `Pipeline`
- `ColumnTransformer`

---

### 2. Feature Engineering
- Separated numerical and categorical features
- Built modular pipelines for scalable preprocessing
- Ensured consistency between training and testing data

---

### 3. Machine Learning Models
The following regression models were implemented and evaluated:

- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor ✅ *(Best performing)*  
- K-Nearest Neighbors (KNN)  
- ElasticNet  
- Ridge Regression  
- Lasso Regression  

---

### 4. Model Evaluation
Models were evaluated using:

- Mean Squared Error (**MSE**)  
- Root Mean Squared Error (**RMSE**)  
- R² Score  
- Cross-validation (K-Fold)

---

## 🧠 Best Model
The **Random Forest Regressor** achieved the best performance:

- Lowest MSE among all models  
- Strong ability to capture non-linear relationships  
- Robust against overfitting compared to simpler models  

---

## 🔍 Hyperparameter Optimization
- Used **RandomizedSearchCV**
- Tuned parameters such as:
  - Number of trees (`n_estimators`)
  - Tree depth (`max_depth`)
  - Feature selection (`max_features`)
- Improved model performance after tuning

---

## 🤖 Deep Learning Model (TensorFlow)
A neural network model was also implemented to explore deep learning approaches:

### Architecture:
- Input normalization layer  
- Dense layers with ReLU activation  
- Dropout layers for regularization  
- L2 regularization  

### Training Techniques:
- Early stopping  
- Batch training  
- Validation split  

### Outcome:
- Reduced overfitting  
- Improved generalization performance  

---

## 📈 Results & Visualization
The project includes several visualizations:

- Scatter plot of **Actual vs Predicted values**
- Residual analysis
- Model comparison plots

These visualizations demonstrate the performance and accuracy of different models.

---

## 🛠️ Tech Stack
- **Programming:** Python  
- **Libraries:**  
  - Scikit-learn  
  - TensorFlow / Keras  
  - Pandas, NumPy  
  - Matplotlib, Seaborn  

---

## 📁 Project Structure

diamond-price-prediction-ml/
│
├── notebooks/
│ └── diamond_price_prediction.ipynb
│
├── data/
│ └── diamonds.csv
│
├── results/
│ └── plots/
│
├── README.md
├── requirements.txt


---

## 🚀 How to Run

### 1. Install dependencies
```bash
pip install -r requirements.txt
2. Run the notebook
jupyter notebook notebooks/diamond_price_prediction.ipynb
📌 Key Contributions
Built a complete ML pipeline using Scikit-learn
Compared multiple regression algorithms systematically
Applied hyperparameter tuning for performance improvement
Implemented a deep learning model for regression
Developed visualization tools for model evaluation
📬 Future Work
Deploy model using FastAPI or Flask
Integrate with a web-based prediction interface
Experiment with advanced models:
XGBoost
LightGBM
Optimize neural network architecture further
👤 Author

Mohammad Saleem
M.Sc. Computer Science Student
Machine Learning & AI Enthusiast
