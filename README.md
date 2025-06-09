

# 🔐 Adversarial Exploits and Security Evaluation in Transfer-Learned Image Classification

This project investigates the **security vulnerabilities of deep learning models** to adversarial attacks using a ResNeXt101-based image classifier. We implement and analyze the **Fast Gradient Sign Method (FGSM)** to demonstrate how carefully crafted perturbations can significantly degrade model performance, even on high-accuracy systems.

## 📌 Objectives

- Build a high-accuracy image classification system using **transfer learning with ResNeXt101_32x8d**.
- Evaluate the system’s robustness against **adversarial examples** generated via FGSM.
- Visualize and quantify the **impact of attack strength** (ε) on classification accuracy.

## 📊 Dataset

- **Intel Image Classification Dataset**  
  - 6 classes: `buildings`, `forest`, `glacier`, `mountain`, `sea`, `street`  
  - Real-world, multi-class natural scene dataset  
  - Download: [Intel Image Classification on Kaggle](https://www.kaggle.com/puneet6060/intel-image-classification)

## 🧠 Model Architecture

- **Base Model**: `ResNeXt101_32x8d` pretrained on ImageNet
- **Framework**: PyTorch  
- **Techniques Used**:
  - Transfer Learning with frozen early layers
  - Image normalization and data augmentation
  - Custom fully-connected head for 6-way classification

## 🧪 Adversarial Attack Implementation

- Attack Type: **FGSM (Fast Gradient Sign Method)**
- Attack Strength (ε): Explored in range `[0.0, 0.3]`
- Target: Model prediction on clean test data
- Method:
  - Perturb the input image in the direction of the gradient sign
  - Evaluate model accuracy on perturbed images

## 📉 Visualization of Results

![image](https://github.com/user-attachments/assets/03eac39d-7bfe-4b7d-ac8b-510d42210122)


- Accuracy **drops significantly** as ε increases
- Visualization confirms **subtle perturbations can cause misclassification**


## 🔐 Security Implications

- Even robust, high-performing models are **vulnerable to adversarial attacks**
- Demonstrates need for:
  - Adversarial training
  - Robust optimization
  - Secure deployment strategies in vision applications

