---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
title: Projects
permalink: /projects/
---

## Analyzing the Effectiveness of K-FAC on Training MLP-Mixers for Image Classification
University of Toronto, CSC2541 Neural Network Training Dynamics (Winter 2022)

K-FAC is an approximate second order optimization method that has been shown to speed up training convergence while achieving competitive performance when training logistic autoencoders, convolutional networks, and RNNs. Here, we apply K-FAC to the MLP-Mixer architecture, and demonstrate that (without pretraining) K-FAC outperforms SGD and Adam when performing CIFAR-100 image classification and when handling large input sizes on CIFAR-10. Additionally, we perform learning rate grafting to confirm that the implicit learning rate schedule is the primary factor dictating classification performance.


[\[Project Report\]](data/CSC2541_Project_Analyzing_KFAC_on_MLP_Mixer.pdf) [\[Code\]](https://github.com/Salarios77/kfac-mlp-mixer)
<br>
<br>
<br>

--- 
## ResCapsNet: Detection of COVID-19 from Chest X-Ray Images Using ResNet and Capsule Network
University of Toronto, CSC413 Neural Networks and Deep Learning (Winter 2021)
<center><img src="/images/ResCapNet.png" align="center" width="100%" ></center>

The coronavirus disease (COVID-19) is spreading rapidly and has drastically af-
fecting the health of people over 200 countries. COVID-19 is spreading fast;
therefore; a critical step in controlling the epidemic curve is its early detection.
While current diagnosis tests in clinics and hospitals require specific requirements,
it has been shown that COVID-19 affects the lungs of patients and displays the
symptoms of pneumonia, where can be diagnosed from Computed Tomography
(CT) scans and X-ray images. It, therefore, necessities the need for detection
of COVID from other lung diseases. Deep learning-based algorithms especially
Convolutional Neural Networks (CNNs) are among the most interested methods in
this regards. However, CNNs-based frameworks suffer from being unable to find
the spatial relations between image instances and the need for a large number of
data requirement, which is unavailable due to sudden emergence of COVID-19. To
tackle the mentioned problems of CNNs, this paper proposes a Capsule Network-
based framework, referred to as ResCapsNet, which uses capsule networks as
the main body and ResNet50 for feature extraction. The proposed ResCapsNet
framework has been performed on a dataset of X-ray images and an accuracy
of 98%, sensitivity of 98.07%, specificity of 99.15%, and area under the curve
of 99% were resulted. The achieved results demonstrate the advantage of the
proposed method in comparison to CNN-based framework proposed in [2] and
capsule network-based COVID-CAPS framework proposed in [ 3]. In order to
further improve the performance of ResCapsNet, we applied the proposed ResCap-
sNet framework on the augmented data and accuracy of 98.9% and sensitivity
of 98.99% , and specificity of 98.30% were achieved.


[\[Project Report\]](data/CSC413_final_report.pdf) [\[code\]](https://github.com/sherrychen127/CSC413_project.git)



<br>
<br>
<br>

---

## Real-Time Face Mask Detector using a Faster-RCNN Architecture
University of Toronto, APS360 Applied Fundamentals of Machine Learning (Fall 2020)


<center><img src="/images/FaceMaskDetector.png" align="center" width="50%" ></center>
<br>
<br>

Fast (~14 fps) face mask detector which accurately identifies bounding boxes of faces and labels whether a mask is worn (correctly) or not worn using a Faster-RCNN (with FPN backbone) architecture. Achieves 85% mAP@0.5 on a kaggle face mask detection dataset.

[\[Project Report\]](data/final_report_aps360.pdf) [\[Code\]](https://github.com/Salarios77/face_mask_detector)
<br>
<br>
<br>

---

## AuPackto: Autonomous Hardware Packing Machine
University of Toronto, AER201H  Engineering Design  (Winter 2018)

<center><img src="/images/AuPackto.png" align="center" width="50%" ></center>

Aupackto is designed to autonomously package four types of fasteners in AER201 design course. Our team consists of three people, where each member is responsible for one of the following three subsyetems: Circuits, Electro-mechanics, and Microcontroller. As a Microcontroller member, I was responsible for programming on the PIC and Arduino to interface with various sensors and carry out the overall software logic.


[\[Project Report\]](data/AER201_FinalReport.pdf) [\[Code\]](https://github.com/sherrychen127/AER201_HardwarePackagingMachine)


<br>
<br>
<br>