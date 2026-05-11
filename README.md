# CNN-Based P2P Botnet Detection using Flow Features

## 📌 Overview
This project focuses on detecting Peer-to-Peer (P2P) Botnet attacks using a Convolutional Neural Network (CNN) model and network flow features from the UNSW BoT-IoT dataset.

Traditional security systems struggle to detect modern botnets because of their decentralized communication structure. This project uses deep learning to automatically identify malicious network traffic patterns and classify them as normal or botnet activity.

---

## 🎯 Objectives
- Detect botnet attacks using network traffic flow features
- Build a CNN-based deep learning model
- Classify traffic into normal or malicious categories
- Evaluate model performance using accuracy, precision, recall, F1-score, confusion matrix, and ROC curve

---

## 🛠 Technologies Used
- Python
- TensorFlow / Keras
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- SMOTE

---

## 📂 Dataset
Dataset Used:
- `UNSW_2018_IoT_Botnet_Final_10_Best.csv`

The dataset contains:
- Normal network traffic
- Botnet attack traffic
- Flow-based network features

---

## 🔍 Selected Features
The following 10 important features were used:

- seq
- stddev
- N_IN_Conn_P_SrcIP
- N_IN_Conn_P_DstIP
- min
- max
- mean
- state_number
- srate
- drate

---

## ⚙️ Project Workflow

### 1. Data Collection
- Load dataset from CSV file

### 2. Data Preprocessing
- Clean column names
- Encode categorical values
- Remove unnecessary columns
- Select important features

### 3. Train-Test Split
- 80% training data
- 20% testing data

### 4. Feature Reshaping
- Convert data into CNN compatible format

### 5. CNN Model Building
CNN Architecture:
- Conv1D Layer
- ReLU Activation
- MaxPooling Layer
- Flatten Layer
- Dense Layer
- Softmax Output Layer

### 6. Model Training
- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy

### 7. Prediction & Evaluation
- Accuracy
- Classification Report
- Confusion Matrix
- ROC Curve

---

## 🧠 CNN Model

```python
model = Sequential()

model.add(Input(shape=(X_train.shape[1], 1)))
model.add(Conv1D(64, 3, activation='relu'))
model.add(MaxPooling1D(2))
model.add(Flatten())
model.add(Dense(32, activation='relu'))
model.add(Dense(num_classes, activation='softmax'))
```

---

## 📊 Results
The CNN model successfully detected botnet traffic with high accuracy.

Generated outputs:
- Accuracy graph
- Loss graph
- Confusion matrix
- ROC curve
- Classification report

---

## 🚀 Future Improvements
- Improve dataset balancing
- Use larger datasets
- Real-time network traffic analysis
- Compare CNN with LSTM models
- Deploy as intrusion detection system

---

## ▶️ Installation

```bash
pip install pandas numpy matplotlib seaborn scikit-learn tensorflow imbalanced-learn
```

---

## ▶️ Run Project

```bash
python main.py
```

---

## 👨‍💻 Author
A T Pranav Varshan  
M.E - CSE (Data Science and Cyber Security)

---

## 📌 Conclusion
This project demonstrates that CNN-based deep learning models can effectively detect P2P botnet attacks using network flow features and improve automated intrusion detection systems.
