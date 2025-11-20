
# 🩺Kidney Stone Segmentation using ResUNet++
Kidney Stone Segmentation using ResUNet++

This project performs semantic segmentation of kidney stones from CT scan images using a ResUNet++ deep learning model, trained on the publicly available dataset:

- **Dataset:** Kidney Stone Segmentation Dataset

- **Source:** Kaggle

- **Type:** CT images (.jpg) + segmentation masks (.png)

- **Goal:** Detect very small kidney stones using pixel-wise segmentation.

---

## 🚀1. Project Overview
Kidney stones are usually very small in CT images, making segmentation a challenging task.
This project uses ResUNet++, an advanced architecture that improves:

Residual connections

Attention mechanisms

Multi-scale feature extraction

This makes it effective for detecting tiny regions such as kidney stones.

---

## 🧠 2. Model Used:Model Used: ResUNet++

ResUNet++ provides:

✔ Deep residual learning

✔ Squeeze-and-Excitation blocks

✔ Attention gates

✔ Better detection of small structures

- **Loss function used:**

Dice Loss (handles class imbalance)

Focal Loss (focuses on tiny kidney stones)

Optimizer: Adam
Image size: 256 × 256

---

## 📊 3. Dataset
- **Source:** [Kidney Stone Segmentation Dataset](https://www.kaggle.com/datasets/bemorekgg/kidney-stone-segmentation-dataset)
- **Data Type:** `.jpg` medical images and corresponding `.png` masks, 
TXT files: YOLO annotations (not used in this project)
- **Split:** 80% training, 20% testing

---

## 🚀 4. How to Run the Project (Google Colab)

- **Step 1: Install Libraries** 

 
!pip install segmentation-models-pytorch albumentations opencv-python

- **Step 2: Extract dataset**

Upload kidney-stone.zip and run:

import zipfile
zip_path = "/content/kidney-stone.zip"
with zipfile.ZipFile(zip_path, 'r') as zip_ref:
zip_ref.extractall("/content/")

- **Step 3: Train the model**

Training code includes:

Dataset pairing

Augmentations

Dataloaders

ResUNet++ model

Custom loss functions

Training & validation loops

Full code is included in Medical-image-segmentation.ipynb.

---

## 📈 5. Results

Example output:

<img width="1342" height="457" alt="Screenshot 2025-11-21 010156" src="https://github.com/user-attachments/assets/519fa1f3-5e4c-4602-add6-ca80e0e7869e" />


The model successfully detects kidney stones even when the target area is extremely small.

## 🌍 6. Practical Use

Faster and more accurate kidney stone detection

Helps doctors focus on decision-making instead of manual marking

Adaptable for tumors, organs, and other medical segmentation tasks


## 🔍 7. Challenges

Kidney stones occupy very few pixels in the image.

Dataset masks were generated using YOLO + SAM (may contain noise).

Strong class imbalance → requires special loss (Dice + Focal).

## 📝 8. Future Improvements

Use UNet++, DeepLabV3+, or Swin-UNet

Add more CT preprocessing (CLAHE, windowing)

Post-processing with morphological operations

Integrate detection + segmentation pipeline (YOLO → ResUNet++)

## 🙌 9. Author
Bhavika Bavchandbhai Radadiya

MSc Data Analytics (2025)

## 10. License

This project is licensed under the MIT License – see the LICENSE
 file for details.
