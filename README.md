# Multivariate Time Series Activity Classification

This project focuses on **classification of human activities** using features extracted from **multivariate time series data**, typically from motion sensors embedded in mobile phones, such as:
- Accelerometer
- Gyroscope

The goal is to aggregate compatible datasets, extract a consistent set of features, and develop models (including neural networks) for robust activity classification. In this context, the use of phone sensors for Human Activity Recognition (HAR) is motivated by the desire to create models that can run efficiently on mobile devices. While deep learning typically involves feeding raw, unprocessed data to the network, similar to how shallow machine learning approaches often require feature engineering, the key difference here is that we're interested in making the model small enough to run on a phone. To achieve this, a significant portion of the computational load is moved to an earlier stage—feature extraction—before training, to reduce the model complexity during the inference phase. The goal is to strike a balance between extracting meaningful features that can aid classification and keeping the model lightweight and efficient enough for real-time use on mobile devices.

---

## 📁 Project Structure

The datasets used in this project include:

- **WISDM**
- **MotionSense**
- **Heterogeneity Activity Recognition**
- **MobiAct**

Each dataset has its own directory containing the respective raw or preprocessed data files.

---

## 🧠 Feature Extraction

There is a dedicated **Jupyter Notebook** for feature extraction for each dataset:
- `MOBY_feature_extractor.ipynb`
- `WISDM_feature_extractor.ipynb`
- `HHAR_feature_extractor.ipynb`
- `MOTION_feature_extractor.ipynb`

Each notebook:
- Loads the raw dataset
- Preprocesses the multivariate signals
- Extracts statistical, temporal, or frequency-domain features (e.g., using **CATCH22**, **TSFEL**, etc.)

---

## 🤖 Modeling & Experiments

The notebook `ProgettoApplicazioniIA.ipynb` handles:
- Aggregation of feature sets from multiple datasets (where possible)
- Dataset balancing and preprocessing
- Implementation of various **neural network architectures**
- Evaluation of performance on consistent activity labels across datasets

This stage allows experimentation with model generalization across heterogeneous data sources.

---

## 📂 Data Files

All dataset files are stored in their respective directories (e.g., `./WISDM/`, `./MotionSense/`, etc.).  
These files are **not tracked by Git**, as specified in the `.gitignore`, due to GitHub’s storage and upload size limitations.

---

## 🚀 Technologies Used

- Python  
- NumPy, Pandas  
- Scikit-learn, TensorFlow, PyTorch  
- TSFEL, Catch22  
- Jupyter Notebook, Seaborn, Matplotlib
