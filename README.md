# AI Red Teaming: Deepfake Adversarial Robustness Suite

## Overview
This repository contains a specialized AI Security Research framework designed to evaluate the vulnerability of visual Convolutional Neural Networks (CNNs) against adversarial perturbation attacks. Developed specifically for Deepfake image and video frame detection architectures, this suite mathematically measures a model's operational breaking point when subjected to targeted gradient manipulation.

## Core Research Capabilities

* **Fast Gradient Sign Method (FGSM) Implementation:** A PyTorch-based execution engine that calculates the gradient of the loss function with respect to the input image, generating invisible pixel perturbations ($L_\infty$ norm bound) that force catastrophic misclassification.
* **White-Box Architecture Analysis:** Extracts gradient maps directly from locked model weights (`.eval()` state) to identify the specific visual features the CNN over-relies on for classification.
* **Confidence Decay Benchmarking:** Quantifies the mathematical degradation of the model's Softmax output before and after the injection of adversarial noise, providing concrete metrics for defensive model retraining (Adversarial Training).

## Research & Industry Context
As synthetic media (Deepfakes) become increasingly utilized in advanced social engineering and identity fraud, organizations are deploying CNNs as a primary defense. However, threat actors are actively utilizing Adversarial Machine Learning (AML) to inject invisible pixel noise into GAN-generated images, blinding the detection algorithms. 

This repository proves the necessity of Adversarial Robustness testing. A model cannot be considered secure for enterprise deployment simply because it achieves high baseline accuracy; it must maintain that accuracy under deliberate, mathematical sabotage.
