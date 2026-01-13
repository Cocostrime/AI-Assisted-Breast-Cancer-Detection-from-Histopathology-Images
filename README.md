# AI-Assisted-Breast-Cancer-Detection-from-Histopathology-Images

## 🎯 Objectives
- Develop a CNN-based automated system for breast cancer detection  
- Perform:
  - **Binary classification** (Benign / Malignant)
  - **Multiclass classification** (8 tumor categories)
- Combine images from **all magnification levels (40X, 100X, 200X, 400X)**
- Reduce computational cost using **transfer learning**
- Evaluate performance using standard metrics

## 🗂️ Dataset Description
The dataset consists of **approximately 7500 histopathological breast scan images** captured at four different magnification levels:
- 40X  
- 100X  
- 200X  
- 400X  

📎 **Dataset Access:**  
The dataset is privately stored and shared via a **Google Drive link** (https://drive.google.com/drive/folders/1I2EFBgeyb9Lr1sdBtAZST1reEjCpkX3k?usp=share_link).
All magnification levels are **combined during training** so that the model learns scale-invariant features.

## 🧠 Methodology
This project uses **transfer learning with the VGG16 architecture**, pretrained on the ImageNet dataset. Instead of training a CNN from scratch, VGG16 is used as a **feature extractor**, and custom classification layers are added on top.

### Why VGG16?
- Proven performance in image classification tasks  
- Simple and uniform deep architecture  
- Strong feature extraction capability  
- Suitable for medical image analysis  
- Reduces training time and hardware requirements  

## ⚙️ Tools & Technologies
- **Programming Language:** Python  
- **Deep Learning Framework:** TensorFlow, Keras  
- **CNN Model:** VGG16  
- **Platform:** Google Colab  
- **Libraries:** NumPy, Matplotlib, Scikit-learn  

## 🏗️ Model Architecture
- Pretrained **VGG16 convolutional base**
- Frozen initial layers to preserve learned features
- Custom fully connected layers for classification
- Dropout layers to prevent overfitting

### Output Layer
- **Binary classification:** Sigmoid activation  
- **Multiclass classification:** Softmax activation  

## 🧪 Training Details
- Train–Validation split: **80% / 20%**
- Optimizer: Adam
- Loss Functions:
  - Binary Crossentropy (Binary classification)
  - Categorical Crossentropy (Multiclass classification)
- Training executed on **GPU-enabled Google Colab**

## 📊 Model Evaluation
The model performance is evaluated using:
- Accuracy
- Training and Validation Loss
- Confusion Matrix
- Precision, Recall, and F1-score

These metrics are critical in medical imaging tasks to reduce false predictions.

## 🚀 How to Run the Project
1. Clone the repository  
2. Upload the dataset to Google Drive  
3. Open the notebook in Google Colab  
4. Mount Google Drive  
5. Run all cells sequentially  
6. Trained models are saved for later inference  
