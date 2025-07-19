# Genetic Algorithm for Diagnosing Diabetes

## 🚀 Project Overview

This project aims to enhance diabetes diagnosis accuracy using a **Genetic Algorithm (GA)** to optimize **Support Vector Machine (SVM)** hyperparameters. The approach is evaluated on the **Pima Indians Diabetes Dataset**, with the primary goal of improving predictive performance by replacing manual tuning with intelligent optimization.

---

## ❓ Problem Statement

Traditional SVM-based models often rely on fixed or manually selected parameters, leading to suboptimal results. This project addresses:
- The limitations of trial-and-error tuning
- The critical need for accurate early diabetes diagnosis
- The challenge of adapting models to varying patient data

---

## 💡 Innovation

We use a **Genetic Algorithm** to:
- Automatically optimize SVM hyperparameters (`C`, `gamma`, and `kernel`)
- Improve accuracy and adaptability
- Reduce manual effort in model tuning

---

## 🎯 Objective

To optimize SVM classifier hyperparameters using GA to **maximize classification accuracy** for diabetes prediction using the Pima dataset.

---

## 📊 Dataset

- **Source**: Kaggle / UCI Repository
- **Records**: 768 patients
- **Features**:
  - Pregnancies
  - Glucose
  - BloodPressure
  - SkinThickness
  - Insulin
  - BMI
  - DiabetesPedigreeFunction
  - Age
- **Target**: Diabetic (1) or Non-Diabetic (0)

---

## 🛠️ Libraries & Tools

| Category                | Tools/Libraries                                |
|------------------------|------------------------------------------------|
| Data Handling          | `pandas`, `numpy`                              |
| Preprocessing          | `StandardScaler` (from `sklearn`)             |
| Dimensionality Reduction | `PCA` (from `sklearn`)                     |
| Model                  | `SVC` (Support Vector Classifier from `sklearn`) |
| Optimization           | `deap` (Genetic Algorithm library)             |
| Visualization          | `matplotlib`, `seaborn`, `random`              |

---

## 🧬 Genetic Algorithm Overview

GA mimics biological evolution through:
- **Selection** (Tournament Selection)
- **Crossover** (Blend Crossover)
- **Mutation** (Gaussian Mutation)

Each **individual** in the population represents a set of SVM hyperparameters. The **fitness function** is based on classification accuracy (cross-validation).

### GA Parameters
- **Population size**
- **Crossover probability (`cxpb`)**
- **Mutation probability (`mutpb`)**

---

## 🧱 System Architecture

1. Load and preprocess the Pima dataset
2. Initialize Genetic Algorithm population
3. Evaluate individuals (SVM accuracy as fitness)
4. Apply:
   - Tournament Selection
   - Blend Crossover
   - Gaussian Mutation
5. Train final SVM with best parameters
6. Evaluate prediction accuracy

---

## 📈 Optimization Results

| Parameter    | Value   |
|--------------|---------|
| Best `C`     | 52133   |
| Best Kernel  | RBF     |
| Best Accuracy| 0.7786  |

---

## ✅ Conclusion & Key Takeaways

- **SVM + GA** provides improved and adaptive accuracy over default settings
- **GA automates hyperparameter tuning**, eliminating grid search
- **Reusable framework** for other datasets and models
- Encourages scalable and intelligent ML design

---

## 📁 Folder Structure

📦Genetic-Algorithm-Diabetes
┣ 📄README.md
┣ 📄diabetes.csv
┣ 📄svm_ga_diagnosis.py
┗ 📄requirements.txt

---

## 📌 Future Work

- Apply GA to other classifiers (e.g., Random Forest, XGBoost)
- Explore hybrid optimization techniques (GA + Grid Search)
- Use larger or more diverse healthcare datasets

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---

## 🤝 Acknowledgements

- UCI & Kaggle for the dataset
- DEAP for the Genetic Algorithm framework
- scikit-learn for modeling utilities
