# Imbalanced-Class-Classification

This project aims to classify cast parts as "Good" or "Bad" based on temperature readings from multiple sensors during the casting process. The implementation tackles class imbalance, applies feature engineering techniques, and uses PCA for effective feature reduction. The model's performance is evaluated using cross-validation with SMOTE oversampling to address data imbalance issues.

---

## Project Highlights

- **Data Preprocessing:**
  - Handling of missing values and outliers using z-scores and IQR methods.
  - Feature extraction with window-based sliding techniques for temperature readings.
  
- **Exploratory Data Analysis (EDA):**
  - Identified outliers in temperature readings and visualized their distribution using box plots.
  - Examined label imbalance and addressed it using Synthetic Minority Oversampling Technique (SMOTE).

- **Feature Engineering:**
  - Aggregated statistical features (`max`, `min`, `std`) for temperature sensors over sliding windows.
  - Reduced dimensionality using Principal Component Analysis (PCA) with 99% variance retention.

- **Modeling:**
  - Implemented Random Forest Classifier with SMOTE to address label imbalance.
  - Evaluated model performance using 5-fold cross-validation for accuracy and F1-score.

---

## Key Steps

### 1. Data Preprocessing
- Data was cleaned by removing missing values and handling outliers using robust statistical methods.
- Outliers were identified using z-scores and Interquartile Range (IQR) methods.

### 2. Feature Engineering
- Features were extracted by aggregating statistical measures over sliding windows (e.g., `max`, `min`, `std`).
- A total of 12 engineered features were generated for four temperature sensors.

### 3. Dimensionality Reduction
- PCA was applied to reduce dimensionality, retaining 99% of the variance in the data.

### 4. Model Training & Evaluation
- Random Forest Classifier was trained and evaluated using 5-fold cross-validation.
- SMOTE was applied to handle the class imbalance during model training.
- The performance was assessed using metrics such as **Accuracy** and **F1-score**.

---

## Results

The base model chose was Logisitc Regeression which performance was:

- **Average F1-Score:** `0.12` 

After experiementing with different models, with 5-fold cross-validation after hyperparamter tuning the final model Random Forest achieved the following performance:

- **Average F1-Score:** `0.99` 

---

## Requirements

The project relies on the following Python libraries:

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scipy`
- `imblearn`
- `scikit-learn`
- `scikit-learn-intelex` (for Intel optimizations)

To install all requirements, run:
```bash
pip install -r requirements.txt
```

---

## Setup

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/Imbalanced-Class-Classification.git
    cd Imbalanced-Class-Classification
    ```

2. Open Notebook and execute the cell
    

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Contribution
Feel free to contribute by submitting pull requests or reporting issues. For questions or suggestions, contact the repository maintainer.

