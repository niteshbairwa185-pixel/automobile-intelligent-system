# 🚗 Automobile Intelligent System

An end-to-end **Automobile Intelligence System** designed to analyze used-car data and provide intelligent, data-driven insights for buyers and sellers.

The project is being developed as a collection of independent modules, with each module solving a specific automobile-related problem.

---

## 🎯 Project Goal

The goal of this project is to build a complete **Automobile Intelligence System** that can answer practical questions about used cars:

* 💰 What is the expected price of a used car?
* 🚗 Should I buy this car?
* 🤝 Which car is best for my requirements?
* ⭐ What do customers think about this car?
* 💵 What price should I list my car for?
* 🔮 What car or model might be a good future upgrade?

Each question will be handled through an independent module rather than a single model.

---
---
## Data Sources
- `cars.csv` — US used-car listings (https://www.kaggle.com/datasets/andreinovikov/used-cars-dataset/data)
- `cars_descriptions_with_details.csv` — Edmunds expert reviews, scraped (https://www.kaggle.com/datasets/ademboukhris/expert-car-reviews-dataset/data)
Place both in `data/raw/` before running the notebooks.

---

## 🧩 Project Modules

| Module                    | Purpose                              | Status |
| ------------------------- | ------------------------------------ | ------ |
| Data Collection           | Collect and organize automobile data | ✅      |
| Data Cleaning             | Improve data quality and consistency | ✅      |
| Exploratory Data Analysis | Understand data and market patterns  | ✅      |
| Feature Engineering       | Create useful ML features            | ✅      |
| Price Prediction          | Estimate used-car prices             | 🚧     |
| Recommendation System     | Find suitable cars for buyers        | 🚧     |
| Review Analysis           | Analyze customer opinions            | 🚧     |
| Listing Price Estimation  | Suggest a suitable selling price     | 🚧     |
| Future Upgrade Prediction | Identify potential future upgrades   | 🚧     |
| Application               | Combine modules into one system      | 🚧     |

---

## 📊 Current Data Pipeline

```text
Raw Data
   ↓
Data Collection
   ↓
Data Cleaning
   ↓
Exploratory Data Analysis
   ↓
Market & Buyer Analysis
   ↓
Feature Engineering
   ↓
cars_features.csv
   ↓
Machine Learning
```

---

## 🔍 Data Analysis

### Data Understanding & Quality

The dataset was inspected for:

* Missing values
* Duplicate records
* Invalid values
* Data types
* Vehicle age
* Numerical relationships
* Basic statistical patterns

### Market & Buyer Analysis

The used-car market was analyzed using:

* Brand representation
* Model popularity
* Model-level median prices
* Brand-level median prices
* Price segments
* Fuel type distribution
* Transmission distribution
* Brand distribution across price segments

---

## ⚙️ Feature Engineering

Meaningful features were created without unnecessarily increasing the complexity of the dataset.

### `mileage_per_year`

Represents the average yearly usage of a vehicle relative to its age.

### `brand_model`

Combines the standardized brand and model into a more specific vehicle identifier.

The resulting feature dataset contains:

```text
97,675 records
14 columns
0 missing values
```

Target-derived information is kept separate from model inputs to avoid **target leakage** during price prediction.

---

## 📁 Project Structure

```text
automobile-intelligent-system/
│
├── data/
│   ├── raw/
│   ├── processed/
│   └── external/
│
├── notebooks/
│   ├── 01-EDA.ipynb
│   ├── 02-EDA.ipynb
│   ├── 03-feature-engineering.ipynb
│   ├── 04-price-prediction.ipynb
│   └── 05-recommendation.ipynb
│
├── src/
│   ├── data/
│   ├── features/
│   ├── models/
│   └── recommendation/
│
├── app/
│
├── README.md
├── requirements.txt
└── .gitignore
```

---

## 🚧 Project Progress

* [x] Data collection
* [x] Data cleaning
* [x] Exploratory Data Analysis
* [x] Market & buyer analysis
* [x] Feature engineering
* [ ] Used-car price prediction
* [ ] Car recommendation system
* [ ] Customer review analysis
* [ ] Listing price estimation
* [ ] Future upgrade prediction
* [ ] Application development

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* Jupyter Notebook
* Git & GitHub

---

## 🚀 Setup

Clone the repository and install the required dependencies:

```bash
pip install -r requirements.txt
```

Then open the notebooks directory and run the notebooks in sequence.

---

## 📌 Project Status

The **data engineering and feature engineering pipeline is complete**.

The next stage is the development and evaluation of the **used-car price prediction module**.