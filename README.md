# Play Tennis Classification using Decision Tree

This repository implements a **Decision Tree Classifier** using Scikit-Learn to predict whether conditions are favorable to play tennis based on weather features such as Outlook, Temperature, Humidity, and Wind.

---

## 📌 Project Overview

- **Problem Type**: Binary Classification
- **Algorithm**: Decision Tree Classifier
- **Dataset**: `tennis_anyone_1000.xlsx` (1,000 samples)
- **Target Variable**: `Play Tennis` (`Yes` / `No`)

---

## 📊 Dataset & Features

The dataset contains environmental and weather metrics recorded over 1,000 days:

| Feature Name | Description | Values / Categories |
| :--- | :--- | :--- |
| `Outlook` | Weather condition | `Overcast`, `Rain`, `Sunny` |
| `Temperature` | Thermal condition | `Cool`, `Hot`, `Mild` |
| `Humidity` | Relative moisture level | `High`, `Normal` |
| `Wind` | Wind strength | `Strong`, `Weak` |
| `Play Tennis` | Target class (Output) | `Yes` (651), `No` (349) |

*Note: The metadata column `Day ID` is dropped during feature extraction.*

---

## ⚙️ Workflow & Architecture

1. **Data Loading**: Read dataset using `pandas` and `openpyxl`.
2. **Preprocessing**:
   - Dropped identifier columns (`Day ID`).
   - Categorical feature encoding via `sklearn.preprocessing.LabelEncoder`.
3. **Data Splitting**:
   - Train-Test Split ratio: **80% Training / 20% Testing** (`test_size=0.2`, `random_state=1`).
4. **Model Architecture**:
   - `sklearn.tree.DecisionTreeClassifier`

---

## 🚀 Installation & Setup

### 1. Prerequisites
Ensure you have Python 3.8+ installed along with `pip`.

### 2. Install Dependencies
```bash
pip install pandas numpy scikit-learn openpyxl
