# Brain Tumour Detection Using Deep Learning

## Overview
This project implements a **deep learning-based approach** for detecting brain tumours from MRI scans. Two models are trained and compared:
1. **Custom CNN (Convolutional Neural Network)**
2. **VGG16 (Transfer Learning)**

The models classify MRI images as either **"Tumour" or "No Tumour"**, leveraging **image preprocessing, data augmentation, and deep learning architectures** to improve classification accuracy.

## Features
- **Automated MRI classification** for brain tumours.
- **Custom CNN & VGG16 models** for comparison.
- **Data preprocessing pipeline** (cropping, resizing, grayscale conversion, augmentation).
- **Evaluation metrics:** Accuracy, Precision, Recall, F1-score, Confusion Matrix, ROC Curve.
- **Early stopping & learning rate adjustment** to prevent overfitting.

## Dataset
The dataset consists of MRI scans labeled as:
- `Yes` (Tumour present)
- `No` (No tumour detected)

**Preprocessing steps applied:**
- Resized all images to **224x224 pixels**.
- Converted to **grayscale** for uniform processing.
- Applied **data augmentation** (rotation, flipping, brightness adjustment).
- Ensured all images were in **JPG format** with standardised filenames.

## Model Architectures
### **1️⃣ Custom CNN**
A custom CNN with:
- **3 convolutional layers** with ReLU activation & MaxPooling.
- **Flatten layer** to convert feature maps.
- **Dense layers with dropout (0.3)** to prevent overfitting.
- **Final sigmoid layer** for binary classification.

### **2️⃣ VGG16 (Transfer Learning)**
- Uses **pretrained VGG16 convolutional layers** (ImageNet weights).
- Custom **fully connected layers** with dropout (0.5) for classification.

## Installation & Setup
### **Prerequisites**
Ensure you have **Python 3.7+** and install dependencies using:
```bash
pip install -r requirements.txt
```
### **Run the Project**
1. **Preprocess the dataset:**
   ```bash
   python preprocess.py
   ```
2. **Train the models:**
   ```bash
   python train.py --model cnn   # For Custom CNN
   python train.py --model vgg16  # For VGG16
   ```
3. **Evaluate performance:**
   ```bash
   python evaluate.py
   ```
4. **Make a prediction on a single MRI scan:**
   ```bash
   python predict.py --image test_mri.jpg
   ```

## Results & Evaluation
| **Metric** | **Custom CNN** | **VGG16** |
|------------|--------------|----------|
| **Accuracy** | 94% | 97% |
| **F1-Score** | 94% | 97% |
| **AUC Score** | *Insert AUC* | *Insert AUC* |

- **VGG16 achieved higher accuracy and lower false positives**.
- The **ROC curve** and confusion matrix show **better generalisation for VGG16**.

## Future Improvements
- Fine-tuning VGG16 instead of keeping it frozen.
- Collecting more MRI data to improve generalisation.
- Exploring **other architectures (ResNet, EfficientNet)** for better results.

## Contributors
- **[Yousuf Ahmed]** (Lead Developer)

## License
This project is **open-source** and available under the **MIT License**.

---
🚀 **For questions or contributions, feel free to reach out!**

