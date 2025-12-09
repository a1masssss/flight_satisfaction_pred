# ✈️ Airline Passenger Satisfaction Classification

A machine learning project that predicts airline passenger satisfaction using logistic regression. This project includes both a custom implementation of logistic regression from scratch and comparison with scikit-learn's optimized implementation.

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Results](#results)

## 🎯 Project Overview

This project aims to predict whether airline passengers are satisfied or dissatisfied based on various flight and service-related features. The analysis includes:

- **Data preprocessing and cleaning**
- **Exploratory Data Analysis (EDA)**
- **Feature engineering and encoding**
- **Custom Logistic Regression implementation from scratch**
- **Model comparison with scikit-learn**
- **Hyperparameter tuning using RandomizedSearchCV**
- **Comprehensive model evaluation metrics**

## 📊 Dataset

The dataset contains **25,893 passenger records** after cleaning, with the following characteristics:

- **Target Variable**: `satisfaction` (satisfied vs. neutral or dissatisfied)
- **Features**: 21 predictive features including demographics, flight details, and service ratings

### Key Features:

**Demographic & Flight Information:**
- Gender (Male/Female)
- Customer Type (Loyal/Disloyal)
- Type of Travel (Business/Personal)
- Class (Economy, Economy Plus, Business)
- Flight Distance
- Departure/Arrival Delay in Minutes

**Service Ratings (1-5 scale):**
- Inflight WiFi Service
- Online Boarding
- Seat Comfort
- Inflight Entertainment
- Food and Drink
- Leg Room Service
- Baggage Handling
- Check-in Service
- Cleanliness
- Gate Location
- Ease of Online Booking
- On-board Service
- Inflight Service
- Departure/Arrival Time Convenience

## 🔧 Installation

### Prerequisites

- Python 3.8+
- pip

### Setup

1. Clone the repository:
```bash
git clone <repository-url>
cd classification_demo
```

2. Create and activate a virtual environment:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

## 🚀 Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook main.ipynb
```

2. Run all cells sequentially to:
   - Load and preprocess the data
   - Perform exploratory data analysis
   - Train the custom logistic regression model
   - Compare with scikit-learn's implementation
   - Evaluate model performance

## 📈 Model Performance

### Custom Logistic Regression (from scratch)

- **Accuracy**: 86.77%
- **Precision**: 86.30%
- **Recall**: 83.51%
- **F1-Score**: 84.88%
- **ROC AUC**: 92.34%

### Optimized Scikit-learn Model (after hyperparameter tuning)

- **Accuracy**: 87.43%
- **F1-Score**: 85.50%
- **ROC AUC**: 92.84%
- **Best Parameters**: 
  - C = 0.473 (regularization strength)
  - class_weight = None

### Cross-Validation Results

- **5-Fold CV ROC AUC**: 92.52% (±0.002)

## 📁 Project Structure

```
classification_demo/
│
├── datasets/
│   └── test.csv              # Passenger satisfaction dataset
│
├── main.ipynb                # Main Jupyter notebook with analysis
├── requirements.txt          # Python dependencies
├── README.MD                 # Project documentation
│
└── venv/                     # Virtual environment (not in repo)
```

## 🛠 Technologies Used

- **Python 3.13**
- **Data Processing**: pandas, numpy
- **Visualization**: matplotlib, seaborn, plotly
- **Machine Learning**: scikit-learn, scipy
- **Development**: Jupyter Notebook, ipykernel

## 📊 Results

The project successfully demonstrates:

1. **High predictive accuracy** (>87%) in classifying passenger satisfaction
2. **Strong model performance** across multiple metrics (ROC AUC > 92%)
3. **Custom implementation** matches scikit-learn's optimized performance
4. **Feature importance analysis** through correlation heatmaps
5. **Robust evaluation** using cross-validation and multiple metrics

### Key Insights:

- **Customer Type** and **Type of Travel** are strong predictors of satisfaction
- **Online Boarding** and **Class** significantly influence passenger satisfaction
- The model achieves excellent discrimination capability (ROC AUC ~92%)
- Standardization of features improves model convergence and performance

## 📝 Notes

- The dataset had 83 missing values in the "Arrival Delay in Minutes" column, which were removed
- The 'Age' feature was dropped after correlation analysis
- Data standardization was applied to improve model performance
- Class imbalance was addressed during model optimization

## 🤝 Contributing

Feel free to fork this project and submit pull requests with improvements!

## 📄 License

This project is open source and available for educational purposes.

---

**Author**: Classification Demo Team  
**Last Updated**: December 2025

