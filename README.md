#PCB-Defect-Detection-Conditional-DCGAN

# PCB Defect Generation using Conditional DCGAN

## 1. Project Overview

This is a Gen AI-based project for generating PCB defect images.
We use Conditional DCGAN to generate new images of PCB defects.
The generated images are added to the original DeepPCB dataset.
This helps to increase the dataset size and reduce data imbalance.
The augmented dataset is then used for PCB defect detection.

## 2. Problem Statement

Getting enough PCB defect images for training is difficult and
time-consuming. Some defect classes also have fewer images.
This can affect the performance of the detection model.
So, we generate synthetic PCB defect images using Conditional DCGAN
to increase the available training data.

## 3. Objectives

- Generate realistic PCB defect images using Conditional DCGAN.
- Increase the diversity of the PCB dataset.
- Reduce class imbalance.
- Use the generated images for PCB defect detection.
- Improve the detection performance.

## 4. Dataset

We used the DeepPCB dataset.

The project considers six PCB defect classes:

- Open
- Short
- Mousebite
- Spur
- Copper
- Pin-hole

## 5. Methodology

DeepPCB Dataset
        ↓
Image Preprocessing
        ↓
Conditional DCGAN
        ↓
Synthetic PCB Defect Images
        ↓
Dataset Augmentation
        ↓
YOLOv12 + CBAM + BiFPN
        ↓
PCB Defect Detection

## 6. Technologies Used

- Python
- PyTorch
- Conditional DCGAN
- YOLOv12
- CBAM
- BiFPN
- DeepPCB Dataset
- Google Colab

## 7. Conditional DCGAN

The Conditional DCGAN contains a Generator and a Discriminator.

The Generator takes random noise and a defect class label and
generates a PCB defect image.

The Discriminator takes real or generated images along with the
class label and learns to distinguish between real and generated
images.

The class label allows us to generate a specific type of PCB defect.

## 8. PCB Defect Detection

The generated images are combined with the original dataset.
The augmented dataset is used for PCB defect detection.

The detection framework uses:

- ResNet18
- YOLOv12
- CBAM Attention Module
- BiFPN Feature Fusion

## 9. Training Details

- Epochs: 200
- Batch Size: 8
- Optimizer: AdamW
- Learning Rate: 0.0001
- Image Size: 640 × 640
- GPU: NVIDIA Tesla T4

## 10. Results

The detection model achieved:

- Precision: 98.61%
- Recall: 95.28%
- mAP@50: 98.0%
- mAP@50-95: 69.48%

The Conditional DCGAN was able to generate synthetic PCB defect
images that were used to increase dataset diversity.

## 11. Advantages

- Generates synthetic PCB defect images.
- Helps reduce dataset imbalance.
- Increases data diversity.
- Reduces dependence on manual data collection.
- Helps improve PCB defect detection.

## 12. Future Work

- Explore StyleGAN for better image generation.
- Explore Diffusion Models.
- Use Transformer-based detection models.
- Deploy the system on embedded hardware.
- Develop a real-time PCB inspection system.

## 13. Conclusion

This project uses Conditional DCGAN to generate synthetic PCB defect
images and augment the DeepPCB dataset. The augmented data is then
used for PCB defect detection using YOLOv12, CBAM and BiFPN.
The project shows how Gen AI can be used to generate additional
training data for PCB inspection.
