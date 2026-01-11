# Tumor Spread Estimation in Lungs using Medical Image Segmentation

 1. Introduction
Lung cancer is one of the leading causes of cancer-related deaths worldwide, and accurate estimation of tumor spread plays a crucial role in diagnosis and treatment planning. Medical imaging, particularly Computed Tomography (CT), provides detailed anatomical information required for detecting lung tumors.

This project focuses on **automated lung tumor segmentation** using **deep learning-based medical image segmentation**. A **U-Net architecture** is employed to segment tumor regions from lung CT images obtained from the **Medical Segmentation Decathlon dataset**. The goal is to reduce manual intervention, improve accuracy, and assist clinicians in analyzing tumor spread efficiently.

This work was carried out as part of the **MSc Data Science Final Project (7PAM2002)** at the **University of Hertfordshire**.

---

2. Preprocessing
Preprocessing is a critical step to ensure consistency and improve model performance. The following preprocessing techniques are applied:

- Resizing CT images to a fixed input size
- Normalization of pixel intensity values
- Conversion of images to grayscale (if required)
- Data augmentation techniques such as:
  - Rotation
  - Flipping
  - Scaling
- Splitting data into:
  - Training set
  - Validation set
  - Test set

These steps help improve generalization and reduce overfitting.

---

 3. Data Creation
The dataset used in this project is sourced from the **Medical Segmentation Decathlon**, which provides:

- Lung CT scan images
- Corresponding ground-truth tumor segmentation masks

Data creation involves:
- Loading CT images and annotation masks
- Pairing each CT image with its corresponding mask
- Organizing data into structured directories
- Preparing data generators for efficient batch loading during training

This structured dataset enables supervised learning for tumor segmentation.

---

 4. Model
The project uses a **U-Net architecture**, which is widely used in biomedical image segmentation tasks.

### Key Features of the Model:
- Encoder–Decoder structure
- Convolutional layers for feature extraction
- Max-pooling layers for downsampling
- Upsampling layers for reconstruction
- Skip connections to preserve spatial information
- Sigmoid activation in the final layer for binary segmentation

The U-Net model efficiently captures both local and global features, making it suitable for lung tumor segmentation.

---

 5. Training
Model training is performed using the prepared dataset with the following approach:

- Input: Preprocessed CT images
- Output: Binary tumor segmentation masks
- Loss Function: Optimized for segmentation tasks
- Optimizer: Adaptive optimizer (e.g., Adam)
- Evaluation Metrics:
  - Dice Coefficient
  - Accuracy
  - Precision
  - Recall

The model is trained on the training dataset and validated using the validation dataset to ensure good generalization.


 6. Visualization
Visualization plays a key role in evaluating segmentation performance. The following visual outputs are generated:

- Ground truth tumor masks
- Validation mask segmentation
- Test mask segmentation
- Predicted tumor segmentation results

- 

Comparing predicted masks with ground truth masks helps in both **qualitative and quantitative evaluation** and makes the results easier to interpret for clinical applications.




