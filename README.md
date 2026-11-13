
# Brain Tumour MRI Classification Using Machine Learning

## Project Overview

This project focuses on Brain Tumour Classification using traditional Machine Learning techniques and MRI image processing.

It uses image texture features extracted through GLCM (Gray-Level Co-occurrence Matrix) and LBP (Local Binary Pattern) to classify brain MRI images into four categories:

- Glioma
- Meningioma
- No Tumor
- Pituitary

The project also includes statistical analysis and visualization of the MRI image dataset.

## Project Structure

The repository contains two Jupyter notebooks:

### 1. Brain_Tumor_ML_Pipeline.ipynb

This notebook implements the complete machine learning pipeline, including:

- Loading and preprocessing MRI images.
- Resizing images to 128 × 128 pixels.
- Converting images into grayscale.
- Extracting GLCM texture features.
- Extracting LBP histogram features.
- Combining GLCM and LBP features.
- Feature scaling using StandardScaler.
- Training and comparing machine learning models.

### 2. Statistical_Description_of_Image_Dataset.ipynb

This notebook performs statistical analysis of the MRI image dataset.

It includes:

- Image dimensions analysis.
- Grayscale mean and median.
- Variance and standard deviation.
- Skewness and kurtosis.
- Histogram entropy and energy.
- RGB channel statistics.
- Statistical visualizations.
- Training and Testing dataset comparisons.

## Machine Learning Algorithms

The project implements and compares three machine learning algorithms:

1. Gaussian Naive Bayes
2. Support Vector Machine (SVM) with RBF Kernel
3. K-Nearest Neighbors (KNN)

For KNN, different values of K are evaluated:

- K = 3
- K = 5
- K = 7
- K = 9

The preferred model identified in the notebook is:

**GLCM + LBP + SVM (RBF Kernel)**

## Feature Extraction Techniques

### GLCM (Gray-Level Co-occurrence Matrix)

GLCM extracts texture-based features from MRI images.

The following features are calculated:

- Contrast
- Dissimilarity
- Homogeneity
- Energy
- Correlation
- Angular Second Moment (ASM)

### LBP (Local Binary Pattern)

LBP is used to capture local texture patterns in MRI images.

Configuration:
- Radius: 3
- Number of Neighbour Points: 24
- Method: Uniform

The extracted LBP histogram features are combined with GLCM features to create the final feature vector.

## Dataset Structure

The project uses a Brain Tumour MRI Dataset containing four classes.

Expected directory structure:

```text
Brain_Tumor_MRI_Dataset/
│
├── Training/
│   ├── glioma/
│   ├── meningioma/
│   ├── notumor/
│   └── pituitary/
│
└── Testing/
    ├── glioma/
    ├── meningioma/
    ├── notumor/
    └── pituitary/
```

## Technologies Used

- Python
- Jupyter Notebook
- OpenCV
- NumPy
- Pandas
- Scikit-learn
- Scikit-image
- Matplotlib
- Seaborn
- SciPy
- TQDM

## Installation

Install the required Python libraries:

```bash
pip install opencv-python scikit-image scikit-learn numpy pandas matplotlib seaborn tqdm scipy ipywidgets
```

## How to Run the Project

1. Clone this repository:

```bash
git clone <YOUR_REPOSITORY_URL>
```

2. Navigate to the project directory:

```bash
cd <YOUR_REPOSITORY_FOLDER>
```

3. Download and extract the Brain Tumour MRI dataset.

4. Update the dataset path in both Jupyter notebooks according to your system.

5. Install the required dependencies.

6. Open Jupyter Notebook:

```bash
jupyter notebook
```

7. Run the notebooks sequentially.

## Key Implementation Details

| Parameter | Configuration |
|---|---|
| Image Size | 128 × 128 |
| Image Format | Grayscale |
| GLCM Distances | 1 and 3 |
| GLCM Angles | 0°, 45°, 90°, 135° |
| LBP Radius | 3 |
| LBP Neighbour Points | 24 |
| LBP Method | Uniform |
| Classification Models | Naive Bayes, SVM, KNN |
| Feature Scaling | StandardScaler |

## Future Improvements

- Experiment with additional machine learning algorithms.
- Implement deep learning architectures such as CNN.
- Perform cross-validation.
- Improve model generalization.
- Evaluate performance on independent datasets.
- Develop a user-friendly interface for MRI image classification.

## Disclaimer

This project is developed for educational and research purposes only. It is not a clinically validated diagnostic system and should not be used as a substitute for professional medical diagnosis.
