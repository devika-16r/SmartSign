# SmartSign

### 📌 Overview

**SmartSign** is a machine learning-based system designed to detect forged signatures using handcrafted features and a neural network classifier. It employs image preprocessing techniques and feature engineering to classify signatures as **genuine** or **forged**, making it suitable for secure offline verification in domains like banking, legal documentation, and identity management.


### 🧠 Technologies Used

* **Programming Language:** Python
* **Libraries & Frameworks:** NumPy, scikit-learn, TensorFlow (MLP), Matplotlib, scikit-image
* **Tools:** Jupyter Notebook, Google Colab


### 🛠️ Key Features

* Image preprocessing using grayscale conversion, Gaussian blur, and Otsu thresholding
* Feature extraction: centroid, eccentricity, solidity, skewness, kurtosis, and ink pixel ratio
* Multi-Layer Perceptron (MLP) neural network for binary classification
* Custom CSV-based training and testing dataset generation
* Prediction pipeline for real-time signature verification


### 📁 Project Structure

```
SmartSign/
│
├── Preprocessing/           # Image to binary conversion & cropping
├── FeatureExtraction/       # Extract 9 handcrafted features
├── ModelTraining/           # MLP neural network model
├── Prediction/              # Evaluate new signature
├── Data/                    # Genuine and forged signature datasets
├── Notebooks/               # Jupyter notebooks for each phase
└── README.md                # Project documentation
```


### 📊 How It Works

1. **Preprocessing:**

   * Convert signature image from RGB to grayscale
   * Apply Gaussian blur & Otsu thresholding for binarization
   * Crop the region containing the signature

2. **Feature Extraction:**

   * Calculate 9 numerical features from the binary image
   * Save features to CSV for training and testing

3. **Model Training:**

   * Use a Multi-Layer Perceptron (MLP) with 3 hidden layers
   * Train on labeled feature vectors (genuine = 1, forged = 0)

4. **Prediction:**

   * Pass features of new signature into trained MLP
   * Output: “Genuine” or “Forged” based on softmax probability


### 🧪 Sample Output

```
Input: test_signature.png  
Prediction: Forged  
```


### 🚀 Future Improvements

* Replace MLP with CNN or Siamese Networks for direct image-based verification
* Expand dataset for better generalization
* Build a web interface for user-friendly access


### 🙋‍♀️ Author

**Devika R**
[LinkedIn](https://www.linkedin.com/in/devika-rajangam/)


