# RupaID

**RupaID** is a Python-based application designed to classify the denomination of Indonesian Rupiah banknotes using **Local Binary Pattern (LBP)** for feature extraction and **Naïve Bayes** for classification.  
It includes image preprocessing with data augmentation and evaluates model performance through **K-Fold Cross Validation**.

---

## 📦 Dataset

The original dataset consists of **120 grayscale images** of Indonesian Rupiah banknotes from 8 denominations:

- Rp1,000
- Rp2,000
- Rp5,000
- Rp10,000
- Rp20,000
- Rp50,000
- Rp75,000
- Rp100,000

Each class contains **15 original images**, captured using a smartphone camera positioned above HVS paper for a clean, consistent background.

### 🔄 Data Augmentation

To improve model generalization, each original image is augmented **5 times** using the `imgaug` library. The augmentation techniques include:

- Horizontal flipping
- Small rotations (±10°)
- Slight scaling (zoom in/out)
- Brightness adjustments
- Addition of Gaussian noise

After augmentation, the total dataset expands to **840 images** (120 original + 720 augmented), evenly distributed across all classes.

---

## ⚙️ Features

- 🔍 Identify Rupiah banknotes (from Rp1,000 to Rp100,000)
- 🧠 Feature extraction using **Local Binary Pattern (LBP)**
- 📊 Classification with **Naïve Bayes**
- 📈 Model evaluation using **5-Fold Stratified Cross Validation**
- 🖼️ Image visualization and LBP histogram display
- 🖥️ GUI-based interface using **Tkinter**
- 🧪 Prediction from uploaded test images

---

## 🧪 Classification Accuracy

Using 5-fold cross-validation, the model achieves an average classification accuracy of approximately **92.78%**, with some classes like Rp75,000 and Rp100,000 showing near-perfect separation due to distinct texture patterns.

---

## 🚀 How to Run

You can run the RupaID project in **two ways**, depending on your workflow:

---

### 🧠 Option 1: Run from `.ipynb` (Train + Predict)

1. **Clone the repository:**
   ```bash
   git clone https://github.com/avilariz/RupaID.git
   cd RupaID

2. **Open the notebook**
   ```bash
   Use Google Colab or Jupyter Notebook to open rupa-id.ipynb.

3. **Run each cell**
   ```bash
   Includes: loading dataset, image augmentation, training the Naïve Bayes model, and testing prediction.

### ⚡ Option 2: Use Pretrained Model (rupiah_model_gnb.pkl)
1. **Clone the repository:**
   ```bash
   git clone https://github.com/avilariz/RupaID.git
   cd RupaID

2. **Install required libraries:**
   ```bash
   pip install -r requirements.txt

3. **Skip the training section**
   ```bash
   Jump directly to the section that loads the pretrained model (rupiah_model_gnb.pkl) and performs classification.

This will directly load the pretrained Naïve Bayes model and launch the Rupiah classification interface.

---

## 🙋‍♂️ Author
Developed as part of a Computer Vision project at **Politeknik Caltex Riau**.

---

## 📁 Folder Structure
   ```bash
   rupaid/
   │
   ├── DATASET_UANG/                         # Original images
   ├── DATASET_UANG_AUGMENTED/              # Augmented images
   ├── rupiah_model_gnb.pkl
   ├── rupa-id.ipnyb
   ├── requirements.txt
   └── README.md
