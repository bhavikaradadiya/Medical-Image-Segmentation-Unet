
# 🩺Kidney Stone Segmentation using ResUNet++
Kidney Stone Segmentation using ResUNet++

This project performs semantic segmentation of kidney stones from CT scan images using a ResUNet++ deep learning model, trained on the publicly available dataset:

- **Dataset:** Kidney Stone Segmentation Dataset

- **Source:** Kaggle

- **Type:** CT images (.jpg) + segmentation masks (.png)

- **Goal:** Detect very small kidney stones using pixel-wise segmentation.

---

## 🚀 Project Overview
Kidney stones are usually very small in CT images, making segmentation a challenging task.
This project uses ResUNet++, an advanced architecture that improves:

Residual connections

Attention mechanisms

Multi-scale feature extraction

This makes it effective for detecting tiny regions such as kidney stones.

---

## 🧠 Model Used:Model Used: ResUNet++

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

## 📊 Dataset
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

## 📈 Results
| Metric | Description | Performance |
|:-------:|:-------------|:-------------|
| **Dice Score** | Overlap between predicted and true masks | High |
| **IoU** | Intersection over Union | High |
| **Loss** | BCE + Dice | ~0.56 |

The model performed well in detecting small kidney stones, even with limited data.

---

## 🧩 Requirements

pip install -r Requirements.txt

---

## 🧩 Run The Project

python medical_image_segmentation_unet.py


## 🧾 Evaluation Metrics

Dice Coefficient: Measures overlap accuracy

IoU (Intersection over Union): Measures prediction correctness

BCE + Dice Loss: Combined loss for small object segmentation


## 🌍 Practical Use

Faster and more accurate kidney stone detection

Helps doctors focus on decision-making instead of manual marking

Adaptable for tumors, organs, and other medical segmentation tasks

## 👩‍💻 Author

Bhavika Bavchandbhai Radadiya
MSc Data Analytics (2025)

## 📄 License

This project is licensed under the MIT License – see the LICENSE
 file for details.
