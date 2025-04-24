# Optimizing Packaging with Machine Learning

🙌 **Acknowledgements**
This project was developed in collaboration with **Simon Püschel**.

🔒 **Data Disclaimer**
The data used in this project belongs to a company and is not publicly available. All references to data in the notebooks are illustrative or based on simulated values for development and testing.

📫 **Contact**
For questions or collaboration ideas, feel free to reach out via GitHub Issues or contact me directly.

---

## Overview
This project aims to predict package sizes for e-commerce orders by leveraging a robust machine learning pipeline. The workflow encompasses feature engineering, data preprocessing, model training, and evaluation, tailored to address the complexities of item-level data. Multiple machine learning models, including CatBoost, Neural Networks, and Random Forest, are implemented to classify package sizes.

## 📁 Repository Structure

```plaintext
notebooks/
│
├── 1_feature_engineering_weight.ipynb     # Estimate item weight by category
├── 2_feature_engineering_volume.ipynb     # Estimate item volume
├── 3_feature_engineering_softness.ipynb   # Classify items as soft or hard
├── 4_feature_engineering_height.ipynb     # Extract height-specific features
├── 5_assigning_features_to_data_and_flat.ipynb # Combine and prepare features
│
├── Best_Model_(Catboost).ipynb            # Best performing model
├── Best_Neural_Network.ipynb              # Neural network approach
├── Best_Random_Forest.ipynb               # Random Forest baseline
├── Regression_Approach.ipynb              # Regression alternative formulation
│
├── environment.yml                        # Reproducible environment setup
├── *.py                                   # Supporting Python scripts (volume, weight, label dictionaries)
├── readme.md                              # Project documentation (this file)
```

## How to Run

### 1. Setup
- Create a virtual environment and install dependencies using the environment file.

### 2. Data Preparation
- Load and preprocess the raw data using feature engineering notebooks (`1_feature_engineering_weight.ipynb` to `5_assigning_features_to_data_and_flatten.ipynb`).

### 3. Model Training
- Train and evaluate models by executing corresponding notebooks (`Best Model (Catboost).ipynb`, `Best Neural Network.ipynb`, etc.).

### 4. Evaluation
- Use confusion matrices and classification reports to analyze model performance.

---

## Results
- Models are evaluated based on their ability to classify package sizes accurately.
- Comparative performance is visualized via metrics like the confusion matrix and classification reports.

---

## Future Work
- Explore additional features for improved predictions.
- Update the dictionaries with more data.
- Create a detailed classification system for products that groups items with similar physical features into consistent categories, ensuring minimal variance within each category. This system should be flexible enough to accommodate new products while avoiding excessive granularity that would tie it too closely to individual product variations.
- Extract physical features by NLP analysis of only store descriptions.
- Test predictions in real life to check how far they are.

