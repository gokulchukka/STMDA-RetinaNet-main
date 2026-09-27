Multi-Camera Unsupervised Domain Adaptation for Object Detection
About

This project focuses on improving object detection when the training data and real-world testing data come from different environments.

The model is trained using labeled synthetic images and adapted to real images collected from different cameras. The project uses RetinaNet, domain adaptation, pseudo-labeling, and self-training to improve detection performance across different camera domains.

Project Workflow
Synthetic Labeled Images
          +
Real Unlabeled Images
          ↓
    Initial Training
          ↓
    Pseudo-Label Generation
          ↓
      Self-Training
          ↓
 Improved Target-Domain Detection
Step 1: Initial Training

The model is trained using synthetic labeled images along with unlabeled images from the HoloLens and GoPro domains.

After the initial training, the model generates pseudo-labels for the real target-domain images.

Step 2: Self-Training

The generated pseudo-labels are combined with the synthetic labeled data and used for further training.

This process is repeated to improve the quality of the pseudo-labels and the detection performance on the target domains.

Technologies
Python
PyTorch
Detectron2
RetinaNet
Computer Vision
Deep Learning
Object Detection
Unsupervised Domain Adaptation
Adversarial Learning
Self-Training
Pseudo-Labeling
COCO Dataset Format
Dataset

The project uses three domains:

Synthetic — Source domain
HoloLens — Target domain
GoPro — Target domain

The dataset follows the COCO annotation format.

Model

The main object detection architecture used is RetinaNet.

The project modifies Detectron2 components to support the proposed domain-adaptation and self-training pipeline.

The training process includes:

Object detection
Feature alignment
Pseudo-label generation
Iterative self-training
Target-domain evaluation
Results

The reported STMDA-RetinaNet results are:

Target Domain	Detection Result
HoloLens	54.36%
GoPro	59.51%

With CycleGAN-based image translation:

Target Domain	Detection Result
HoloLens	66.64%
GoPro	72.22%
What I Learned
Computer vision and object detection
RetinaNet
Detectron2
Deep learning
Multi-camera domain adaptation
Synthetic-to-real transfer
Pseudo-labeling
Self-training
Model evaluation
Working with different image domains
Future Improvements
Test on additional camera domains
Improve pseudo-label quality
Experiment with different object detection models
Compare different domain-adaptation techniques
Improve inference speed
Evaluate on larger datasets
Reference

This project is based on the research work:

A Multi Camera Unsupervised Domain Adaptation Pipeline for Object Detection in Cultural Sites through Adversarial Learning and Self-Training