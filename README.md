# 🚗 AutoValuate - Car Price Prediction Model

## 📜 Description
**AutoVision** is a machine learning project focused on predicting car prices using features like:
- Car brand and model
- Year of manufacture
- Fuel type
- Kilometers driven  

This project utilizes **data preprocessing**, **exploratory data analysis (EDA)**, and a **linear regression model** to achieve a high-performance prediction system with an **R² score of 89.91%**. The implementation leverages libraries such as **Pandas**, **Scikit-Learn**, and **Seaborn**.

---

## 📑 Table of Contents
1. [📊 Dataset Overview](#-dataset-overview)
2. [🛠️ Data Preprocessing](#️-data-preprocessing)
3. [🔍 Exploratory Data Analysis (EDA)](#-exploratory-data-analysis-eda)
4. [📈 Model Training](#-model-training)
5. [📊 Evaluation Metrics](#-evaluation-metrics)
6. [▶️ Usage](#️-usage)
7. [✅ Results](#-results)
8. [📦 Dependencies](#-dependencies)

---

## 📊 Dataset Overview

The dataset used for this project is located at:
`/kaggle/input/quikr-car/quikr_car.csv`

### Sample Data:
| Name                                     | Company   | Year | Price          | Kms Driven | Fuel Type |
|------------------------------------------|-----------|------|----------------|------------|-----------|
| Hyundai Santro Xing XO eRLX Euro III     | Hyundai   | 2007 | ₹80,000        | 45,000 kms | Petrol    |
| Mahindra Jeep CL550 MDI                  | Mahindra  | 2006 | ₹4,25,000      | 40 kms     | Diesel    |
| Maruti Suzuki Alto 800 Vxi               | Maruti    | 2018 | Ask For Price  | 22,000 kms | Petrol    |
| Hyundai Grand i10 Magna 1.2 Kappa VTVT   | Hyundai   | 2014 | ₹3,25,000      | 28,000 kms | Petrol    |

---

## 🛠️ Data Preprocessing
### Key Steps:
1. **Invalid Data Handling**:
   - Removed rows with non-numeric `year` or `kms_driven`.
   - Excluded "Ask For Price" entries in the `Price` column.
2. **Data Conversion**:
   - Converted `year`, `kms_driven`, and `Price` to numeric types.
3. **Text Simplification**:
   - Truncated the `name` column to retain only the first three words.
4. **Missing Value Handling**:
   - Dropped rows with missing values in critical columns.
5. **Outlier Removal**:
   - Filtered out cars priced over ₹6,000,000.

---

## 🔍 Exploratory Data Analysis (EDA)
### Key Insights:
1. **Price Trends**:
   - Luxury brands like Mercedes and Audi have significantly higher prices (via boxplots).
2. **Age vs Price**:
   - Older cars tend to have lower prices, confirmed through swarm plots.
3. **Mileage Impact**:
   - Heavily driven cars are associated with reduced prices.

### Sample Visualizations:
#### 1️⃣ **Company vs Price**
Boxplot analysis reveals price ranges for various manufacturers.
![Company vs Price](link_to_image)  

#### 2️⃣ **Year vs Price**
Swarm plot highlights trends in price depreciation with age.
![Year vs Price](link_to_image)  

#### 3️⃣ **Fuel Type vs Price**
Boxplot explores price variations by fuel type.
![Fuel Type vs Price](link_to_image)

---

## 📈 Model Training
### Workflow:
1. **Input Features**:
   - `name`, `company`, `year`, `kms_driven`, `fuel_type`
2. **Target Variable**:
   - `Price`
3. **Preprocessing**:
   - OneHotEncoding for categorical features
   - Pipeline to handle encoding and linear regression
4. **Model**:
   - Linear Regression
5. **Train-Test Split**:
   - **Test size**: 10%
   - **Optimization**: Random state for the best R² score.

---

## 📊 Evaluation Metrics
### Results:
- **Best R² Score**: **89.91%**
- **Validation**: The model's predictions closely align with actual prices on test data.

---

## ✅ Results
![RESULT_1](https://github.com/user-attachments/assets/792046d2-2d31-4d73-a512-919f80a78214)

![RESULT_2](https://github.com/user-attachments/assets/9ccb1802-8bc3-4d78-aff2-adbd80ad56d2)

![RESULT_3](https://github.com/user-attachments/assets/da737eaf-1e2f-4030-975a-0ffbe5651d78)

---

## Highlights:
- Achieved a robust **89.91% prediction accuracy (R² score)**.
- The model performs well across diverse car categories and years.

### Example:
- **Car**: Ford Figo  
- **Year**: 2019  
- **Predicted Price**: ~₹456,549  

---

## 📦 Dependencies
- **Python 3.8+**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Scikit-Learn**
- **Pickle**

---

## 👨‍💻 Developer Notes
Feel free to contribute by submitting pull requests or reporting issues in the repository!
