# Breast Tumor Classification: Malignant or Benign

A machine learning project that uses Logistic Regression to classify breast tumors as malignant (M) or benign (B) based on cell nuclei features extracted from digitized images of fine needle aspirates (FNA) of breast masses.

## Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project implements a binary classification model to predict whether a breast tumor is malignant or benign. Early and accurate diagnosis of breast cancer is crucial for effective treatment, and machine learning models can assist medical professionals in making informed decisions.

The project includes:
- Data preprocessing and cleaning
- Exploratory data analysis with correlation heatmaps
- Feature selection and engineering
- Model training using Logistic Regression
- Comprehensive model evaluation with multiple metrics

## Dataset

The project uses the **Wisconsin Breast Cancer Dataset**, which contains:
- **569 samples** of breast tumor data
- **32 features** computed from digitized images
- **Target variable**: Diagnosis (M = malignant, B = benign)

Each feature describes characteristics of cell nuclei present in the image, including:
- Radius (mean of distances from center to points on the perimeter)
- Texture (standard deviation of gray-scale values)
- Smoothness (local variation in radius lengths)
- Compactness (perimeter^2 / area - 1.0)
- Concavity (severity of concave portions of the contour)
- Concave points (number of concave portions of the contour)
- Symmetry
- Fractal dimension ("coastline approximation" - 1)

For each characteristic, three values are computed:
- Mean
- Standard error
- Worst (largest mean value)

## Features

The following features are used in the analysis:

| Feature Type | Description |
|--------------|-------------|
| radius_mean | Mean radius of the tumor cells |
| texture_mean | Mean texture of the tumor cells |
| smoothness_mean | Mean smoothness of the tumor cells |
| compactness_mean | Mean compactness of the tumor cells |
| concavity_mean | Mean concavity of the tumor cells |
| concave points_mean | Mean number of concave portions |
| symmetry_mean | Mean symmetry of the tumor cells |
| fractal_dimension_mean | Mean fractal dimension |
| *_se | Standard error measurements |
| *_worst | Worst/largest measurements |

## Installation

1. Clone this repository:
```bash
git clone https://github.com/shoutingraven369/Breast_tumor_malignant_or_not.git
cd Breast_tumor_malignant_or_not
```

2. Install the required dependencies:
```bash
pip install pandas matplotlib seaborn scikit-learn category_encoders
```

3. Ensure you have the dataset file `data.csv` in the project directory.

## Usage

1. Open the Jupyter notebook:
```bash
jupyter notebook Breast_cancer_prediction_T4.ipynb
```

2. Alternatively, run in Google Colab by clicking the "Open in Colab" badge in the notebook.

3. Execute the cells sequentially to:
   - Load and preprocess the data
   - Visualize feature correlations
   - Train the Logistic Regression model
   - Evaluate model performance

## Model Performance

The model is evaluated using the following metrics:

| Metric | Description |
|--------|-------------|
| Confusion Matrix | Shows true positives, true negatives, false positives, and false negatives |
| Precision | Ratio of correctly predicted positive observations to total predicted positives |
| Recall | Ratio of correctly predicted positive observations to all actual positives |
| F1 Score | Weighted average of Precision and Recall |
| ROC-AUC Score | Area under the Receiver Operating Characteristic curve |

## Project Structure

```
Breast_tumor_malignant_or_not/
|-- Breast_cancer_prediction_T4.ipynb   # Main Jupyter notebook
|-- data.csv                             # Dataset file
|-- README.md                            # Project documentation
```

## Technologies Used

- **Python 3.x** - Programming language
- **Pandas** - Data manipulation and analysis
- **Matplotlib** - Data visualization
- **Seaborn** - Statistical data visualization
- **Scikit-learn** - Machine learning algorithms and tools
  - LogisticRegression
  - train_test_split
  - StandardScaler
  - LabelEncoder
  - Classification metrics
- **Category Encoders** - Categorical variable encoding
- **Google Colab** - Cloud-based Jupyter environment

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -m 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Open a Pull Request

## License

This project is open source and available under the MIT License.

---

**Note**: This project is intended for educational purposes and should not be used as a substitute for professional medical diagnosis.
