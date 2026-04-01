---
layout: page
title: Projects
permalink: /projects/
---

## Real-Time Text Detection Under Motion Blur

Built and evaluated two real time live text detection models for blurred video frames with DBNet and DINOv2 as base architectures. Designed and trained on a gamma-aware motion blur augmentation pipeline, compared pixel-level and IoU-based performance, and measured deployment-oriented FPS.

- **Key results:** Achieved over 50% absolute improvement in F1 score over baseline for the highest blur level while maintaining stability across conditions. Maintained over 49 FPS for realtime deployment.
- **Focus:** Real-time robustness under motion blur
- [Project Repo](https://github.com/midoppal/DBNet-Blurred-Text-Detector)
- [Paper](./assets/papers/Realtime_Live_Text_Detection.pdf)

<div style="display:flex; justify-content:center; align-items:center; gap:10px; flex-wrap:nowrap;">
  <img src="./assets/images/dbnet_baseline.png" style="width:45%; height:45%; object-fit:cover;" />
  <img src="./assets/images/rt_dbnet.png" style="width:45%; height:45%; object-fit:cover;" />
</div>


## Pneumothorax Classification with LLaVA-Med and PEFT

Finetuned the multimodal LLaVA-Med model using parameter-efficient methods to detect pneumothorax and multiclass diseases from chest X-rays.

- **Key results:** Achieved over 25% improvement in F1 score over the zero shot baseline in binary classification and over 20% improvement in multiclass disease classification (Determined among 6 Diseases and No Finding)
- **Focus:** PEFT for medical vision-language models for targeted classification
- [Project Repo](https://github.com/midoppal/PEFT-LLaVa-Med)
- [Paper](./assets/papers/Peft_LlaVaMed_Pneumothorax.pdf)
  
## Graph Neural Networks for Hyperparameter Inference in Ising Solvers

Worked on graph-based learning methods for solver/hyperparameter selection, contributing to a workshop publication.

- [Publication](./papers)
