# Project 1: Classification

This folder contains classification projects implemented using both Keras/TensorFlow and PyTorch frameworks.

## 📁 Structure

```
Project1-Classification/
│
├── keras_version/
│   ├── model.ipynb                    # Breast Cancer Classification
│   ├── breast_cancer.csv              # Breast Cancer Dataset
│   ├── mobile_price_model.ipynb       # Mobile Price Classification
│   └── mobiles.csv                    # Mobile Price Dataset
│
├── pytorch_version/
│   ├── model.ipynb                    # Mobile Price Classification
│   └── mobiles.csv                    # Mobile Price Dataset
│
└── README.md                          # This file
```

## 🎯 Projects

### 1. Breast Cancer Classification (Keras)

**File**: `keras_version/model.ipynb`  
**Dataset**: `keras_version/breast_cancer.csv`

- **Task**: Binary classification to predict breast cancer diagnosis (Malignant/Benign)
- **Features**: 30 numerical features (radius, texture, perimeter, area, etc.)
- **Target**: Diagnosis (M/B)
- **Model**: Sequential Neural Network with Dense layers
- **Architecture**: 
  - Input: 30 features
  - Hidden Layer 1: 16 neurons (ReLU)
  - Hidden Layer 2: 8 neurons (ReLU)
  - Output: 1 neuron (Sigmoid)
- **Performance**: ~98% accuracy

**Key Steps**:
1. Data loading and EDA
2. Label encoding for target variable
3. Feature scaling using MinMaxScaler
4. Train-test split (90-10)
5. Model training with validation split
6. Evaluation using confusion matrix and classification report

### 2. Mobile Price Classification (Keras)

**File**: `keras_version/mobile_price_model.ipynb`  
**Dataset**: `keras_version/mobiles.csv`

- **Task**: Multi-class classification to predict mobile phone price ranges
- **Features**: 20+ features (battery_power, blue, clock_speed, dual_sim, etc.)
- **Target**: Price range (categorical)
- **Framework**: Keras/TensorFlow
- **Preprocessing**: StandardScaler for feature normalization

### 3. Mobile Price Classification (PyTorch)

**File**: `pytorch_version/model.ipynb`  
**Dataset**: `pytorch_version/mobiles.csv`

- **Task**: Multi-class classification to predict mobile phone price ranges
- **Features**: 20+ features (battery_power, blue, clock_speed, dual_sim, etc.)
- **Target**: Price range (categorical)
- **Framework**: PyTorch
- **Preprocessing**: StandardScaler for feature normalization
- **Data Loading**: Uses PyTorch DataLoader and TensorDataset

## 📊 Dataset Information

### Breast Cancer Dataset
- **Source**: UCI Machine Learning Repository (Wisconsin Breast Cancer Dataset)
- **Samples**: 569
- **Features**: 30 numerical features
- **Classes**: 2 (Malignant, Benign)

### Mobile Price Dataset
- **Samples**: 2000
- **Features**: 21 features (battery_power, blue, clock_speed, dual_sim, fc, four_g, int_memory, m_dep, mobile_wt, n_cores, pc, px_height, px_width, ram, sc_h, sc_w, talk_time, three_g, touch_screen, wifi, price_range)
- **Classes**: 4 price ranges (0, 1, 2, 3)

## 🔗 Data-Code Linking

Each notebook is linked to its corresponding dataset:
- `model.ipynb` → `breast_cancer.csv` (same directory)
- `mobile_price_model.ipynb` → `mobiles.csv` (same directory)
- `pytorch_version/model.ipynb` → `mobiles.csv` (same directory)

All data files use relative paths, ensuring the notebooks work when the repository is cloned.

## 📝 Important Notes

1. **Data Paths**: All notebooks use relative paths (e.g., `'breast_cancer.csv'`) to ensure portability
2. **Dependencies**: 
   - Keras projects require: `tensorflow`, `pandas`, `numpy`, `scikit-learn`, `matplotlib`, `seaborn`
   - PyTorch projects require: `torch`, `pandas`, `numpy`, `scikit-learn`
3. **Model Saving**: Keras models are saved as `.h5` files (legacy format) or `.keras` files (recommended)
4. **Reproducibility**: Random seeds are set where applicable (e.g., `random_state=42`)

## 🚀 Running the Projects

1. Navigate to the desired version folder:
   ```bash
   cd keras_version
   # or
   cd pytorch_version
   ```

2. Ensure the dataset is in the same directory as the notebook

3. Open and run the notebook:
   ```bash
   jupyter notebook model.ipynb
   ```

4. Install required packages if needed:
   ```bash
   pip install tensorflow pandas numpy scikit-learn matplotlib seaborn
   # For PyTorch:
   pip install torch pandas numpy scikit-learn
   ```

