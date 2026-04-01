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
  <img src="/assets/images/dbnet_baseline.png" style="width:45%; height:45%; object-fit:cover;" />
  <img src="/assets/images/rt_dbnet.png" style="width:45%; height:45%; object-fit:cover;" />
</div>


## Pneumothorax Classification with LLaVA-Med and PEFT

Adapted a multimodal large language model (LLaVA-Med) for pneumothorax and multiclass detection in chest X-rays using parameter-efficient finetuning (PEFT) techniques, enabling effective learning under limited medical data and compute constraints

- **Key results:** Improved binary classification accuracy from ~48% (zero-shot) to ~78% using LoRA+BitFit, with significant gains in F1-score, AUC, and MCC. Additionally improved multiclass classification accuracy from ~14.25% (zero-shot) to ~38.07%.
- **Efficiency:** Achieved strong performance while training only a small fraction of model parameters (≈0.05% for BitFit), enabling scalable adaptation of large MLLMs.
- **Focus:** PEFT for medical vision-language models for targeted classification
- [Project Repo](https://github.com/midoppal/PEFT-LLaVa-Med)
- [Paper](./assets/papers/Peft_LlaVaMed_Pneumothorax.pdf)
  
## Graph Neural Networks for Hyperparameter Inference in Ising Solvers

Co-developed a graph neural network system to infer high performing hyperparameters for a chaotic amplitude control Ising solver, replacing manual tuning with learned instance specific parameter prediction. The pipeline was designed around supervised learning on optimized graph hyperparameter pairs and incorporated a scaling based post processing module to improve generalization from small training graphs to much larger unseen instances.

- **Key results:** Achieved strong transfer from graphs with 100–300 nodes during training to benchmark graphs up to 2000 nodes, with the learned hyperparameters frequently outperforming hand tuned settings on time to solution.
- **Focus:** Learned solver configuration for combinatorial optimization using graph neural networks.
- [Publication](./papers)
- [Paper](./assets/papers/Graph_Neural_Networks_for_Ising.pdf)

## Modeling Realistic SCADA Traffic with Diffusion
Developed a diffusion-based pipeline to generate realistic Modbus/TCP SCADA network traffic from raw PCAP data, enabling privacy-preserving dataset augmentation for industrial control system (ICS) research. Designed feature extraction, model training, and validation pipelines to ensure both protocol correctness and statistical realism.

- **Key results:** Generated synthetic traffic that preserved core statistical properties of real Modbus communication, with ~48% of synthetic packets indistinguishable from real traffic under SVM classification
- **Contribution:** Built an end-to-end pipeline from PCAP parsing → structured feature extraction → diffusion model training → protocol-compliant packet reconstruction
- **Validation:** Designed a multistage evaluation framework combining protocol-level verification (request–response consistency) and statistical similarity testing (PCA + SVM)
- **Focus:** Network security, generative modeling, and realistic traffic synthesis for ICS environments
- [Paper](./assets/papers/Modeling_Realistic_SCADA_Traffic_w_Diffusion.pdf)

## Efficient Multi-Agent LLM Orchestration for Optimization (Chain-of-Experts)
Developed and evaluated alternative orchestration policies for a multi-agent LLM system (Chain-of-Experts) that converts natural language optimization problems into executable integer programming code. Replaced a costly conductor LLM with rule-based and reinforcement learning policies to reduce computational overhead while maintaining performance.

- **Key results:** Achieved comparable accuracy (~44.9% vs. 46.9% baseline) while reducing token usage by ~60% using a rule-based conductor policy
- **Contribution:** Designed a keyword-weighted expert selection strategy and a reinforcement learning (DQN) policy for dynamic expert routing.
- **Evauation:** Benchmarked across accuracy, compile/runtime error rates, and token cost on the LPWP dataset for optimization problem solving.
- **Focus:** Multi-agent LLM systems, cost-efficient inference, and automated optimization modeling
- [Paper](./assets/papers/Efficient_Multi_Agent_LLM_Orchestration_for_Optimization.pdf)

