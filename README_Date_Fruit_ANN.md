# Date Fruit Classification using ANN

A multiclass classification project using a feed-forward **Artificial Neural Network (ANN)** built with PyTorch to classify date fruits based on numerical and shape/color features.

## Project Objective

Train an ANN to classify date fruits into one of seven classes using the features provided in the Date Fruit dataset.

## Dataset

The notebook uses:

`DateFruit_Dataset.csv`

Dataset details from the notebook:

- Samples: 898
- Columns: 35
- Input features: 34
- Target: `Class`
- Classes: 7
- Train/test split: 80% / 20%
- Random state: 42

The seven classes in the notebook are:

- BERHI
- DEGLET
- DOKOL
- IRAQI
- ROTANA
- SAFAVI
- SOGAY

## Preprocessing

1. Separate features and target.
2. Encode the categorical class labels using `LabelEncoder`.
3. Split the dataset into training and test sets.
4. Standardize numerical features using `StandardScaler`.
5. Convert the processed data into PyTorch tensors.
6. Create PyTorch `TensorDataset` and `DataLoader` objects.

## ANN Architecture

```text
Input Layer (34 features)
        ↓
Linear (34 → 128) + ReLU
        ↓
Linear (128 → 64) + ReLU
        ↓
Linear (64 → 7)
        ↓
Predicted Class
```

## Training

- Model: Feed-forward ANN
- Loss function: Cross-Entropy Loss
- Optimizer: Adam
- Batch size: 32
- Epochs: 100
- Learning rate: PyTorch Adam default

## Evaluation

The notebook evaluates the trained model using:

- Training Cross-Entropy Loss
- Test Cross-Entropy Loss
- Training Accuracy
- Test Accuracy

> Accuracy values are calculated when the final evaluation cell is executed. No performance value is claimed in this README because the original notebook's final evaluation cell contained a variable-name error and did not record valid evaluation output.

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- PyTorch

## Repository Structure

```text
Date-Fruit-Classification-ANN/
│
├── Date_Fruit_Classification_ANN.ipynb
├── README.md
└── requirements.txt
```

## How to Run

### Google Colab

1. Upload `DateFruit_Dataset.csv` to the Colab environment.
2. Open the notebook in Google Colab.
3. Run the cells from top to bottom.

### Local Environment

Install the dependencies:

```bash
pip install -r requirements.txt
```

Place `DateFruit_Dataset.csv` in the expected working directory and run the notebook using Jupyter Notebook or JupyterLab.

## Note

The dataset file is not included here unless redistribution is permitted. The notebook uses the dataset file name `DateFruit_Dataset.csv`.
