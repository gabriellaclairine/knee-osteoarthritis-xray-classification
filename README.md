# 🦵 Knee Osteoarthritis X-ray Classification

This project builds a **Convolutional Neural Network (CNN)** model to classify knee X-ray images into osteoarthritis severity levels.  
The notebook covers the complete workflow, from dataset preparation and exploratory analysis to model building, training, and evaluation.

---

## 📊 Dataset

The dataset consists of **knee X-ray images** labeled according to the **Kellgren–Lawrence (KL) grading system**:

* **Normal** – No signs of osteoarthritis  
* **Doubtful** – Minimal osteophytes, possible joint space narrowing  
* **Mild** – Definite osteophytes, possible narrowing of joint space  
* **Moderate** – Multiple osteophytes, definite narrowing, some sclerosis  
* **Severe** – Large osteophytes, marked narrowing, severe sclerosis and deformity  

Images are organized in directories corresponding to each class label.

---

## ⚙️ Project Workflow

1. **Exploratory Data Analysis (EDA)**:
   * Visualized sample X-ray images for each severity class.
   * Checked dataset balance across the five classes.

2. **Data Preprocessing**:
   * Resized and normalized X-ray images.
   * Applied one-hot encoding to class labels.
   * Optionally used data augmentation (rotation, flips, zoom) to improve generalization.

3. **Modeling**:
   * Built a CNN using `Keras Sequential API`.
   * Architecture included convolutional layers, pooling layers, dropout, and dense layers.
   * Compiled with `categorical_crossentropy` loss and Adam optimizer.

4. **Training & Evaluation**:
   * Split data into training, validation, and test sets.
   * Trained for multiple epochs with batch optimization.
   * Evaluated performance with accuracy, confusion matrix, and classification report.

---

## 📈 Results and Conclusion

- The CNN achieved good accuracy in classifying osteoarthritis severity from X-rays.  
- Class imbalance posed a challenge, particularly for **Moderate** vs **Severe** cases.  
- Data augmentation improved generalization on underrepresented classes.  

**Future improvements**:
- Use pre-trained models (e.g., ResNet, EfficientNet) for transfer learning.  
- Incorporate Grad-CAM for medical interpretability.  
- Collect more balanced datasets for better performance.  
