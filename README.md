# Air Quality Classification using Machine Learning

## 📘 Overview
This project implements and compares several machine learning classification models to predict **Air Quality** based on multiple environmental attributes.  
It demonstrates model evaluation using metrics such as **accuracy**, **precision**, **recall**, and **F1 scores** through **cross-validation**.

## 👤 Author
**Chengze Liu**  
University of Houston  
UH ID: 2316609  

---

## 🧠 Models Implemented
The project evaluates a series of supervised learning models:

### Task 1 – K-Nearest Neighbors (K-NN)
- Explores multiple values of *k* (2, 5, 10, 50)
- Comparison between normalized and unnormalized features  
- Shows how normalization improves KNN performance  

### Task 2 – Decision Tree Classifier
- Trains trees with various maximum depths (3, 5, 10, 30, 50)
- Evaluates bias–variance tradeoff  
- Plots the decision tree and interprets feature splits  

### Task 3 – Support Vector Machine (SVM)
- Tests different kernel functions: linear, polynomial, RBF, and sigmoid  
- Analyzes performance across kernels  

### Task 4 and 5 – Ensemble Models
- **Bagging** (Decision Tree base estimator, 100 estimators)  
- **Gradient Boosting** (100 estimators)  
- **LightGBM** (100 estimators)  
- Compares model accuracy, precision, recall, and F1-scores  

---

## ⚙️ Methodology
1. **Data Preprocessing**
   - Categorical `Air Quality` converted to numerical labels  
   - Features normalized using `StandardScaler`  
   - Dataset split for **5-fold cross-validation**

2. **Performance Metrics**
   - Accuracy  
   - Precision  
   - Recall  
   - Macro-F1 and Micro-F1  

3. **Model Evaluation**
   - Models trained and validated across folds  
   - Average performance metrics reported for comparison  

---

## 📊 Key Findings
| Model | Accuracy | Precision | Recall | Macro-F1 | Notes |
|--------|-----------|------------|---------|-----------|-------|
| K-NN (k=10, normalized) | 0.9310 | 0.9168 | 0.8895 | 0.9010 | Normalization crucial for distance-based models |
| Decision Tree (depth=10) | 0.9274 | 0.8994 | 0.8922 | 0.8955 | Deeper trees capture complex patterns |
| SVM (RBF kernel) | **0.9456** | 0.9267 | 0.9160 | 0.9209 | Best performance among single models |
| Bagging (DT base) | 0.9512 | 0.9318 | 0.9241 | 0.9277 | Reduces variance, improves generalization |
| Gradient Boosting | **0.9558** | **0.9415** | **0.9316** | **0.9363** | Best overall ensemble model |
| LightGBM | 0.9554 | 0.9396 | 0.9302 | 0.9345 | Comparable to Gradient Boosting |

**Conclusion:**  
- Boosting models outperform individual classifiers due to their ability to reduce both bias and variance.  
- Gradient Boosting achieved the highest overall accuracy and F1-score, making it the best performer in this task.  

---

## 🧩 Technologies Used
- Python 3.x  
- NumPy, Pandas  
- Scikit-learn  
- LightGBM  
- Matplotlib, Seaborn  

---

## 🚀 How to Run
- download "air_quality.csv" and "classfication.ipynb"
- Open "classfication.ipynb" with Jupyter
- Install all related python packages
- Make sure the folder structure is as followed
- Hit "run all"!

## 📁 File Structure

├── classification.ipynb&nbsp;&nbsp;&nbsp;&nbsp;# Main notebook with all models\
├── air_quality.csv&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;# Dataset used for training/testing\
├── report.pdf&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                # report of this project\
└── README.md&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;                 # Project documentation

