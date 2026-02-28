# ANN Projects Repository

This repository contains Artificial Neural Network (ANN) projects organized by problem type (Classification and Regression) and framework implementation (Keras/TensorFlow and PyTorch).

## 📁 Repository Structure

```
Project-ANN/
│
├── Project1-Classification/
│   ├── keras_version/
│   │   ├── model.ipynb                    # Breast Cancer Classification (Keras)
│   │   ├── breast_cancer.csv              # Dataset for Breast Cancer
│   │   ├── mobile_price_model.ipynb       # Mobile Price Classification (Keras)
│   │   └── mobiles.csv                    # Dataset for Mobile Price
│   ├── pytorch_version/
│   │   ├── model.ipynb                    # Mobile Price Classification (PyTorch)
│   │   └── mobiles.csv                    # Dataset for Mobile Price
│   └── README.md                          # Classification Project Details
│
├── Project2-Regression/
│   ├── keras_version/
│   │   ├── model.ipynb                    # Car Purchasing Prediction (Keras)
│   │   └── car_purchasing.csv             # Dataset for Car Purchasing
│   ├── pytorch_version/
│   │   └── (Future PyTorch implementations)
│   └── README.md                          # Regression Project Details
│
└── README.md                               # This file
```

## 🎯 Projects Overview

### Project 1: Classification
- **Breast Cancer Classification** (Keras): Binary classification to predict breast cancer diagnosis
- **Mobile Price Classification** (Keras & PyTorch): Multi-class classification to predict mobile phone price ranges

### Project 2: Regression
- **Car Purchasing Prediction** (Keras): Regression model to predict car purchase amounts

## 📋 Important Notes for GitHub

### Before Pushing to GitHub

1. **Data Files**: 
   - All CSV data files are included in the repository
   - Ensure data files are in the same directory as their corresponding notebooks
   - Update file paths in notebooks to use relative paths (e.g., `'data.csv'` instead of `/content/data.csv`)

2. **Notebook Outputs**:
   - Consider clearing notebook outputs before committing to reduce repository size
   - Use `jupyter nbconvert --ClearOutputPreprocessor.enabled=True --inplace *.ipynb` to clear outputs

3. **Dependencies**:
   - Create a `requirements.txt` file listing all Python packages needed
   - Include versions for reproducibility (e.g., `tensorflow==2.x.x`, `torch==x.x.x`)

4. **Git Configuration**:
   - Add `.gitignore` to exclude:
     - `__pycache__/`
     - `*.pyc`
     - `.ipynb_checkpoints/`
     - `*.h5` or `*.keras` (model files if too large)
     - Virtual environment folders

5. **Documentation**:
   - Each project folder has its own README.md with specific details
   - Include dataset descriptions and model performance metrics
   - Document any preprocessing steps or data transformations

6. **File Naming**:
   - Use consistent naming conventions
   - Keep filenames descriptive and lowercase with underscores

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd Project-ANN
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Navigate to a specific project:
   ```bash
   cd Project1-Classification/keras_version
   # or
   cd Project2-Regression/keras_version
   ```

4. Open the notebook:
   ```bash
   jupyter notebook model.ipynb
   ```

## 📊 Framework Comparison

Each project may have implementations in both Keras/TensorFlow and PyTorch to:
- Compare framework approaches
- Learn both ecosystems
- Understand different API designs

## 🤝 Contributing

When adding new projects:
1. Determine if it's Classification or Regression
2. Place it in the appropriate `ProjectX-*` folder
3. Create implementations in both `keras_version` and `pytorch_version` if possible
4. Update the relevant README.md files
5. Ensure data files are properly linked


