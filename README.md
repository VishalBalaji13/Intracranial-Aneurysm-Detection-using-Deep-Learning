# Intracranial-Aneurysm-Detection-Using-DeepLearning

This repository contains the implementation of a hybrid deep learning approach for detecting intracranial aneurysms from 3D volumetric data (MRI or CT scans). The system leverages a Mesh Convolutional Neural Network (Mesh CNN) to perform accurate segmentation of complex blood vessel structures and localized aneurysm detection. 

##  Problem Statement
An aneurysm is a bulge in a blood vessel caused by a weakness in the blood vessel wall, usually where it branches. As blood passes through the weakened vessel, blood pressure causes a small area to bulge outwards. Effective and highly accurate detection of brain aneurysms is vital for timely medical intervention. However, existing methods often struggle with precision and reliability. This project aims to automate the detection of intracranial brain aneurysms to enhance diagnostic accuracy, treatment planning, and patient outcomes.

##  Methodology & Architecture
To overcome the challenges of traditional detection methods, we developed a hybrid approach integrating **Mesh CNN** for both segmentation and detection. 
* The algorithm effectively processes 3D volumetric data from MRI or CT scans.
* It performs accurate segmentation by capturing the complex shapes and geometries of blood vessels and aneurysms.
* The model then detects and localizes the aneurysms within the segmented regions with high precision.

##  Dataset
The model was trained and evaluated using a dataset of **116 aneurysm 3D object models**. The dataset was split to ensure robust testing:
* **Training Set:** 92 object models
* **Testing Set:** 24 object models

Volume of ground truth (VGT) was delineated by neuroradiologists using MITK software, which was then compared against the volume of the CNN prediction results (VCNN).

##  Model Evaluation & Results
The segmentation model was evaluated using standard medical imaging metrics, achieving an **overall test accuracy of 86.73%**. 

**Detailed Segmentation Metrics:**

| Metric | Result |
| :--- | :--- |
| **Dice Similarity Coefficient (DSC)** | 0.5961 |
| **Intersection over Union (IoU)** | 0.5458 |
| **Recall (Sensitivity)** | 0.4193 |
| **Precision** | 0.3760 |
| **F1 Score** | 0.3964 |
