
# 🩺 Image Segmentation in Medical Imaging Using Deep Learning (U-Net)

This project applies **deep learning (U-Net model)** for **medical image segmentation**, specifically detecting and outlining **kidney stones** in CT or MRI scans.  
It demonstrates how AI can support doctors in diagnosing diseases faster and more accurately.

---

## 🚀 Project Overview
Traditional medical image analysis is time-consuming and depends on expert interpretation.  
Using **U-Net**, this project automatically separates the kidney stone area from the rest of the image, improving diagnostic efficiency.

---

## 🧠 Model Used: U-Net
- **Type:** Encoder–Decoder Convolutional Neural Network  
- **Task:** Pixel-wise segmentation of kidney stones  
- **Key Components:**
  - Downsampling (encoder) to capture context  
  - Upsampling (decoder) to recover spatial details  
  - Skip connections to preserve fine structures  

---

## 📊 Dataset
- **Source:** [Kidney Stone Segmentation Dataset](https://www.kaggle.com/datasets/bemorekgg/kidney-stone-segmentation-dataset)
- **Data Type:** `.jpg` medical images and corresponding `.png` masks  
- **Split:** 80% training, 20% testing  

---

## ⚙️ Steps in the Pipeline
1. **Load Dataset** – Load image-mask pairs from directory.  
2. **Preprocessing** – Resize, normalize, and convert to tensors.  
3. **Model Building** – Define U-Net architecture using PyTorch.  
4. **Training** – Optimize using Binary Cross Entropy + Dice Loss.  
5. **Evaluation** – Calculate Dice Coefficient and IoU.  
6. **Visualization** – Display predicted vs. actual segmentation.

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
