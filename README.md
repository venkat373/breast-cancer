# 🩺 Breast Cancer Classification using SVM

## 📌 Project Overview
This project applies **Support Vector Machines (SVM)** to the Breast Cancer dataset to classify tumors as **Benign (0)** or **Malignant (1)**.  
Both **Linear** and **RBF kernels** are tested, and **hyperparameter tuning** is performed using GridSearchCV with cross-validation.  
Decision boundaries are visualized in **2D PCA space**.

---

## 📂 Dataset
- **Source:** Breast Cancer Wisconsin (Diagnostic) dataset  
- **Target column:** `diagnosis`  
  - `B` → Benign (encoded as 0)  
  - `M` → Malignant (encoded as 1)  
- **Features:** 30 numerical features (mean, se, worst values of tumor characteristics)  

---

## ⚙️ Steps Performed
1. **Data Loading & Preprocessing**
   - Dropped irrelevant `id` column
   - Encoded target labels (`B`=0, `M`=1)
   - Train-test split (80/20) with stratification
   - Applied **StandardScaler** inside pipeline  

2. **Model Training**
   - Trained two baseline models:  
     - **Linear SVM**
     - **RBF SVM (γ = scale)**  

3. **Evaluation**
   - Accuracy, Confusion Matrix, Classification Report  

4. **Hyperparameter Tuning**
   - GridSearchCV with 5-fold CV  
   - Tuned `C` and `gamma` for both kernels  

5. **Visualization**
   - PCA (2 components) for dimensionality reduction  
   - Plotted decision boundaries for Linear & RBF kernels  

---

## 📊 Results

### Baseline Accuracy
| Model       | Accuracy |
|-------------|----------|
| Linear SVM  | ~0.96    |
| RBF SVM     | ~0.97    |

### Confusion Matrix (example RBF SVM)
