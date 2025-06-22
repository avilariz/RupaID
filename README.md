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

1. **Clone the repository:**
   ```bash
   git clone https://github.com/username/rupaid.git
   cd rupaid

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt

3. **Run the application:**
   ```bash
   python Program_Identifikasi_MataUang.py

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
