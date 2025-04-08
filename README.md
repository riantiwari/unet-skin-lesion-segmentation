# U-Net Skin Lesion Segmentation 🧠🩺

This project implements a U-Net-based convolutional neural network for **semantic segmentation of skin lesions** using the **ISIC 2018 Challenge Dataset**. The goal is to automate the detection of lesion boundaries in dermoscopic images — a critical step in early **melanoma detection** and **clinical decision support**.

---

## 🧪 Project Overview

- **Model**: U-Net (fully convolutional)
- **Dataset**: ISIC 2018 - Task 1: Lesion Boundary Segmentation
- **Goal**: Generate binary segmentation masks for skin lesion areas
- **Framework**: PyTorch
- **Evaluation Metrics**: Dice Score (F1 for pixels), IoU (Jaccard Index)
- **Visualization**: Matplotlib

---

## 🧬 About ISIC 2018 Challenge

The **International Skin Imaging Collaboration (ISIC)** hosted the 2018 challenge to promote AI applications in dermatology.  
**Task 1** focuses on **binary segmentation**, where models must delineate the exact area of skin lesions from input dermoscopic images.

📁 Dataset link: [https://challenge.isic-archive.com/](https://challenge.isic-archive.com/)

---

## 📸 Visual Results

| Input Image | Ground Truth | Predicted Mask |
|-------------|---------------|----------------|
| ![Input]() | ![GT]() | ![Pred]() |

*Above: Model prediction closely matches the ground truth lesion mask.*

---

## 📊 Evaluation Metrics

After training for **5 epochs**, the model achieved:

- ✅ **Average Dice Score**: `0.8494`
- ✅ **Average IoU Score**: `0.7480`

These metrics show strong overlap between predicted and actual lesion regions.

---

## 🧠 Model Architecture (U-Net)

- Contracting Path (Encoder): Repeated `Conv -> ReLU -> MaxPool`
- Expanding Path (Decoder): `Upsample -> Concat -> Conv`
- Skip connections to preserve spatial information

---

## 🛠️ Setup & Installation

```bash
# Clone this repo
git clone https://github.com/riantiwari/unet-skin-lesion-segmentation.git
cd unet-skin-lesion-segmentation

# Install dependencies
pip install -r requirements.txt

# Optional: Open notebook in Jupyter or Colab
