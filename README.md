# 📊 CNN Graph Type Image Classifier

This project builds a **Convolutional Neural Network (CNN)** using **TensorFlow** to classify images into **10 distinct types of data visualizations/graphs** such as **Bar Graph**, **Line Graph**, **Pie Chart**, etc.

It includes **custom dataset creation from web URLs**, **image cleaning and filtering**, **data augmentation**, **CNN training**, and **model saving for deployment**.

---

## ✅ Project Highlights (Showcasing Data Engineer + ML Engineer Skills)

### 🗃️ 1. Custom Dataset Collection
- Downloaded image data programmatically using **Python's `requests` and `PIL` libraries**.
- Categorized images into **10 visualization types**.
- Resized all images to **150x150 resolution** for uniformity.

### 🚮 2. Image Cleaning and Filtering (Data Preprocessing & Quality Control)
- Wrote a custom **Python recursive file filtering function** to:
  - **Remove low-quality or tiny images** (based on both actual file size and on-disk size).
  - Ensure dataset quality before training.
- Checked for corrupted or incomplete image files.

---

## ✅ Graph Types Covered (Class Names)

1. AreaGraph
2. BarGraph
3. LineGraph
4. Map
5. ParetoChart
6. PieChart
7. RadarPlot
8. ScatterGraph
9. Table
10. VennDiagram

---

## ✅ CNN Model Architecture

- **Input Shape:** (150, 150, 3)
- **Layers:**
  - Multiple **Conv2D + MaxPooling2D** layers for feature extraction.
  - **Dropout layer** to prevent overfitting.
  - **Dense layers** for classification.
  - **Softmax output layer** for 10-class classification.

---

## ✅ Model Training Details

- **Training-validation split:** 80-20 using `ImageDataGenerator`.
- **Epochs:** 25
- **Loss function:** Categorical Crossentropy
- **Optimizer:** Adam
- **Metric:** Accuracy
- **Data Augmentation:** Handled via `ImageDataGenerator` (rescaling and split).

---

## ✅ Model Saving and Deployment

- Saved the final trained model as: cnn_area_classifier.keras
