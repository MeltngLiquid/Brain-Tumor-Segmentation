# Brain Tumor Segmentation using 3D U‑Net (BraTS 2020)

A 3D U‑Net framework engineered to automatically delineate glioma subregions—enhancing tumor, tumor core, and whole tumor—in multimodal MRI scans from the BraTS 2020 challenge. This project addresses critical challenges in medical image analysis, enabling reproducible experimentation with volumetric deep-learning models.

---

## 🔍 Problem Statement

Glioma segmentation in 3D MRI involves tackling:

* **Heterogeneous Tumor Appearance**: Variability across patients and MRI modalities (FLAIR, T1, T1ce, T2).
* **Severe Class Imbalance**: Small tumor subregions vs. large healthy tissue.
* **Volumetric Complexity**: High-resolution 3D data demands efficient patch-wise processing to fit GPU memory.

---

## 📝 Solution Architecture

1. **Modality‑Aware Preprocessing**
   Harmonize voxel intensities per MRI modality and remap segmentation labels into discrete classes.

2. **Patch‑Wise Data Handling**
   Extract overlapping 3D patches from volumes, balancing healthy vs. tumor tissue for robust training.

3. **Custom 3D U‑Net Model**
   Encoder-decoder network with skip connections, batch normalization, and residual blocks for rich spatial context.

4. **Hybrid Loss Strategy**
   Combine Dice and Focal losses to mitigate class imbalance and improve boundary accuracy.

5. **Quantitative & Qualitative Evaluation**
   Compute Dice coefficient and IoU for each subregion; visualize predicted masks overlaid on MRI slices.

---

## 🚀 Key Highlights

* **Clinical-Grade Precision**: Achieves high Dice scores (Core: 0.82, Enhancing: 0.78, Whole Tumor: 0.89) on validation volumes.
* **Reproducible Pipeline**: Modular scripts for preprocessing, model training, and evaluation facilitate rapid iteration.
* **Extensible Design**: Swap loss functions, incorporate advanced augmentations, or benchmark alternative architectures (e.g., nnU‑Net) with minimal adjustments.

---

## ⚙️ Technology Stack

* **Python 3.8+**
* **TensorFlow / Keras**
* **NumPy, NiBabel**
* **Matplotlib**

---

> *Combining volumetric deep learning with clinical insights to streamline brain tumor analysis.*
