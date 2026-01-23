# Project 2: Regression

This folder contains regression projects implemented using Keras/TensorFlow and PyTorch frameworks.

## 📁 Structure

```
Project2-Regression/
│
├── keras_version/
│   ├── model.ipynb                    # Car Purchasing Prediction
│   └── car_purchasing.csv             # Car Purchasing Dataset
│
├── pytorch_version/
│   └── (Future PyTorch implementations)
│
└── README.md                          # This file
```

## 🎯 Projects

### 1. Car Purchasing Prediction (Keras)

**File**: `keras_version/model.ipynb`  
**Dataset**: `keras_version/car_purchasing.csv`

- **Task**: Regression to predict car purchase amounts
- **Features**: 
  - Age
  - Annual Salary
  - Credit Card Debt
  - Net Worth
- **Target**: Car Purchase Amount (continuous value)
- **Model**: Sequential Neural Network with Dense layers
- **Architecture**: 
  - Input: 4 features
  - Hidden Layer 1: 10 neurons (ReLU)
  - Hidden Layer 2: 10 neurons (ReLU)
  - Output: 1 neuron (Linear activation)
- **Loss Function**: Mean Squared Error (MSE)
- **Optimizer**: Adam
- **Performance Metrics**: 
  - MSE: ~0.004
  - MAE: ~0.05
  - R² Score: ~0.82

**Key Steps**:
1. Data loading and EDA
2. Feature selection (removing non-numerical columns: customer name, email, country, gender)
3. Feature and target scaling using MinMaxScaler
4. Train-test split (80-20)
5. Model training with validation split (20% of training data)
6. Evaluation using MSE, MAE, and R² score
7. Visualization of actual vs predicted values
8. Model architecture visualization

## 📊 Dataset Information

### Car Purchasing Dataset
- **Samples**: 500
- **Features**: 9 columns (customer name, email, country, gender, age, annual salary, credit card debt, net worth, car purchase amount)
- **Used Features**: 4 (age, annual salary, credit card debt, net worth)
- **Target**: Car purchase amount (continuous)
- **Encoding**: Latin-1 encoding used for CSV reading

## 🔗 Data-Code Linking

The notebook is linked to its corresponding dataset:
- `model.ipynb` → `car_purchasing.csv` (same directory)

The data file uses a relative path, ensuring the notebook works when the repository is cloned.

## 📝 Important Notes

1. **Data Path**: The notebook uses relative path `'car_purchasing.csv'` for portability
2. **Encoding**: The CSV file uses Latin-1 encoding, specified in `pd.read_csv()`
3. **Preprocessing**: 
   - Both features (X) and target (y) are scaled using MinMaxScaler
   - Target is reshaped to 2D array: `y.values.reshape(-1,1)`
4. **Dependencies**: 
   - `tensorflow` (Keras)
   - `pandas`
   - `numpy`
   - `scikit-learn`
   - `matplotlib`
5. **Model Evaluation**: 
   - Uses regression metrics: MSE, MAE, R²
   - Visualizes training/validation loss over epochs
   - Compares actual vs predicted values
6. **Reproducibility**: Random state is set to 42 for train-test split

## 🚀 Running the Project

1. Navigate to the keras_version folder:
   ```bash
   cd keras_version
   ```

2. Ensure the dataset is in the same directory as the notebook

3. Open and run the notebook:
   ```bash
   jupyter notebook model.ipynb
   ```

4. Install required packages if needed:
   ```bash
   pip install tensorflow pandas numpy scikit-learn matplotlib
   ```

## 🔮 Future Additions

- PyTorch implementation of Car Purchasing Prediction
- Additional regression projects (house price prediction, stock price prediction, etc.)

