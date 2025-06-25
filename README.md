# Weather-prediction-model-comparison
A machine learning project for weather condition classification using real-world Seattle weather data.

## ⚙️ How to Run the Code Without Hassle in google colab

Follow the steps below to get started easily:

1. 📥 **Run the following cell in the notebook:**

   ```python
   from google.colab import files
   files.upload()
2.🔐 Upload your Kaggle token (kaggle.json) when prompted.

3.✅ Now the code is ready to run — all necessary permissions and access will be set up!
## ⚙️ How to Set Up the Project Locally (Kaggle API Method)

Follow these steps if you want to use the Kaggle API to download the dataset directly:

1. 🔑 **Get Your Kaggle API Credentials**  
   - Go to your [Kaggle Account Settings](https://www.kaggle.com/account)
   - Click on **"Create New API Token"**
   - This will download a file called `kaggle.json`

2. 📁 **Place the Token File**  
   - Move `kaggle.json` to the `.kaggle` folder:
     - On Windows: `C:\Users\<YourUsername>\.kaggle\kaggle.json`
     - On macOS/Linux: `~/.kaggle/kaggle.json`

3. 🧠 **Use the Following Code to Programmatically Download the Dataset**

   ```python
   import os
   import kaggle

   # Set Kaggle credentials (optional if kaggle.json is correctly placed)
   os.environ['KAGGLE_USERNAME'] = 'your_username'
   os.environ['KAGGLE_KEY'] = 'your_key'

   # Download and unzip the dataset
   kaggle.api.dataset_download_files('dataset', path='.', unzip=True)
## 📊 Project Overview

The goal is to predict weather categories such as **Rain**, **Clear**, **Fog**, etc., based on features like:
- Precipitation
- Max and Min Temperatures
- Wind speed

After preprocessing, several classification models are trained and evaluated, including:
- **K-Nearest Neighbors (KNN)**
- **Decision Tree**
- **Logistic Regression**

Performance is assessed using:
- Accuracy score
- Confusion matrix
- Classification report

---

## 🛠️ Tech Stack

- **Python 3**
- **Pandas, NumPy** – Data handling
- **Matplotlib, Seaborn** – Visualization
- **Scikit-learn** – ML models and evaluation

---

## 📁 File Structure

📦 Weather_Prediction_Model_Comparison
├── weather_prediction.ipynb # Jupyter Notebook with full workflow
├── README.md # Project documentation
└── seattle-weather.csv # Dataset used

---

## 📌 Key Highlights

- Encoded categorical weather labels using `LabelEncoder`
- Visualized weather class distribution and feature relationships
- Cleaned data using IQR-based outlier detection
- Applied Pearson correlation to analyze relationships
- Compared models using confusion matrix and accuracy

---
