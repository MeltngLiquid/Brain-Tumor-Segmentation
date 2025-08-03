**Brain Tumor Segmentation with U-Net (BraTS Dataset)**

This project implements a U-Net architecture using TensorFlow/Keras to perform semantic segmentation on 2D MRI slices from the BraTS dataset. The goal is to accurately localize and delineate brain tumor regions from the scans.

---

## What This Project Does

* **Reads Medical Imaging Data**: The notebook processes `.nii` (NIfTI) files from the BraTS dataset to extract 2D axial slices containing tumor regions.

* **Preprocessing**:

  * Normalizes intensity values
  * Selects relevant slices (e.g., with visible tumor regions)
  * Performs resizing and padding to ensure uniform input shape

* **Model Implementation**:

  * Defines a symmetric U-Net architecture using `Conv2D`, `MaxPooling2D`, `Conv2DTranspose`, and skip connections
  * Designed to preserve spatial information for pixel-level segmentation

* **Training Details**:

  * Uses a combined **Dice Loss + Binary Crossentropy** for handling class imbalance
  * Optimized using **Adam** optimizer
  * Trained using Keras on batches of image-mask pairs

* **Evaluation Metrics**:

  * **Dice Coefficient**: Measures overlap between predicted and ground truth masks
  * **IoU (Intersection over Union)**: Evaluates segmentation accuracy
  * Visual outputs show segmented tumor regions overlaid on original scans

* **Output Examples**:

  * Ground truth masks vs predicted masks shown side-by-side
  * Qualitative assessment of how well the model captures tumor boundaries

---

This notebook is suitable for anyone looking to understand how medical image segmentation works using deep learning, and is particularly focused on tumor detection in brain MRI scans. All components—from data loading to model evaluation—are implemented in a single notebook for clarity and reproducibility.
