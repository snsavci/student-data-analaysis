# Student Data Analysis and Graduate School Application Prediction

## Overview

This project focuses on analyzing student academic performance and demographic data to predict their graduate school application outcomes. Using exploratory data analysis (EDA), feature engineering, and machine learning models, the goal is to classify students into one of three categories regarding their graduate school applications:

- `0`: Failed to apply
- `1`: Success - applied inland
- `2`: Success - applied abroad

The study aims to compare different classifiers including Logistic Regression, Random Forest, and Support Vector Machines (SVM), and evaluate their performance with appropriate metrics.

---

## Dataset Description

The dataset contains 105 student records with 17 features, including:

- **Demographic information:** Gender, race, family background indicators
- **Academic scores:** GPA, and various mathematics course scores (Algebra, Calculus, Statistics, etc.)
- **Background variables:** Student origin codes and socio-economic indicators
- **Target variable:** `y` indicating graduate application outcome

All sensitive or identifying information is anonymized or censored.

---

## Project Structure

student-data-analysis/
├── notebook/
│ └── student_data_analysis.ipynb # EDA, feature engineering, modeling, and evaluation
├── data/
│ └── student_data.csv # Raw dataset file
├── requirements.txt # Python dependencies
├── README.md 

---

## Methodology

1. **Data Preprocessing:**  
   - Checked for missing values and duplicates  
   - Encoded categorical variables with one-hot and label encoding  
   - Created new features such as average math scores and flags for low performance  
   - Scaled features where required (especially for Logistic Regression and SVM)  

2. **Exploratory Data Analysis (EDA):**  
   - Visualized distributions of numeric and categorical variables  
   - Investigated class imbalances and feature correlations  

3. **Modeling:**  
   - Tested multiple classifiers (Logistic Regression, Random Forest, SVM)  
   - Used stratified train-test splits and k-fold cross-validation  
   - Applied class weighting to handle imbalance  
   - Evaluated models using accuracy, precision, recall, f1-score, and confusion matrices  

4. **Hyperparameter Tuning:**  
   - Performed grid search on Random Forest parameters, though improvements were marginal due to dataset size  

---

## Results and Insights

- **Logistic Regression** achieved the best balance across classes, performing moderately well on all classes with acceptable recall and precision.  
- **Random Forest** performed well on the majority class but struggled with minority classes, showing bias towards class 0.  
- **SVM** showed mixed results with relatively lower overall accuracy, and tended to favor the majority class.  

The overall moderate accuracy is expected given the small and imbalanced dataset. Further improvements could involve feature selection, data augmentation, or more advanced models.

---

## How to Use This Project

1. Clone the repository:

```bash
git clone https://github.com/snsavci/student-data-analysis.git
cd student-data-analysis
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open and run the notebook:

* Launch Jupyter Notebook or use VSCode to open `notebooks/student_data_analysis.ipynb`.
* Execute the cells sequentially to reproduce the analysis and modeling.

---

