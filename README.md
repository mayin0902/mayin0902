# Hi, I'm Mayin 👋

I am currently pursuing my M.S. degree at **Nanjing University**, with research and project experience in **computer vision, multimodal AIGC, LLM fine-tuning, and AI for Science**.

My recent work focuses on building practical AI systems, including e-commerce image generation, community rule violation detection, UAV image regression, medical image classification, and molecular machine learning.

---

## About Me

- 🎓 M.S. student at **Nanjing University**, AI for Science direction
- 🏅 **Kaggle Expert** with 2 Silver Medals and 1 Bronze Medal
- 🔬 Research experience in equivariant graph neural networks and machine-learning potentials
- 🤖 Project experience in LLM fine-tuning, computer vision, AIGC image generation, and multimodal systems
- 🛠️ Interested in building reliable AI systems that combine algorithms, engineering, and real-world applications

---

## Selected Highlights

- **Kaggle Expert**: 2 Silver Medals, 1 Bronze Medal, global ranking Top 1.18%
- **Google Jigsaw Rules Classification**: Kaggle Silver Medal, ranking 42 / 2445
- **CSIRO Image2Biomass Prediction**: Kaggle Silver Medal, ranking 83 / 3803
- **Jittor Medical Image Classification**: Finalist in the Jittor Algorithm Challenge
- **E-commerce AIGC Try-on System**: built an end-to-end virtual try-on and product image generation pipeline
- **FiLM-Δ-PaiNN**: first-author research on equivariant graph neural networks for molecular potential prediction

---

## Selected Projects

### E-commerce AIGC Try-on System

Built an end-to-end virtual try-on and product image generation prototype for e-commerce scenarios.

**Tech Stack:** FLUX.1 Fill, Gemini Image Generation, SigLIP, LoRA, ComfyUI, FastAPI, LangGraph

**Main Contributions:**

- Designed a dual-route generation pipeline combining local controllable diffusion models and high-level image generation models
- Used SigLIP-based visual condition injection to preserve garment texture and visual details
- Applied LoRA-based identity customization to improve face consistency in generated product images
- Built an automated workflow with FastAPI, ComfyUI, and LangGraph for generation routing, quality checking, and retry control
- Explored an algorithmic solution to reduce product image production time from traditional shooting workflows to rapid AI-assisted generation

---

### Google Jigsaw Rules Classification

Kaggle Silver Medal, ranking **42 / 2445**.

This project focused on community rule violation detection, where the model needed to judge whether a post violated a specific community rule.

**Tech Stack:** Qwen3-4B, QLoRA, DeepSpeed ZeRO-2, vLLM, GTE, Triplet Loss, DeBERTa-v3, FGM, EMA, Rank Blending

**Main Contributions:**

- Reformulated the task as rule-conditioned violation detection instead of simple rule ID classification
- Fine-tuned Qwen3-4B with QLoRA under limited GPU resources
- Used DeepSpeed ZeRO-2 and bf16 mixed precision to improve training efficiency
- Built a GTE-based metric learning branch to improve generalization to unseen rules
- Built a DeBERTa-v3 discriminative classifier with FGM adversarial training and EMA
- Combined LLM, metric-learning, and discriminative branches through rank-based blending
- Improved final AUC to **0.929**

---

### CSIRO Image2Biomass Prediction

Kaggle Silver Medal, ranking **83 / 3803**.

This project focused on multi-target biomass prediction from UAV top-view grassland images under a small-sample setting.

**Tech Stack:** PyTorch, timm, DINOv3 ViT-Huge, SigLIP, LightGBM, CatBoost, PCA, GMM, AMP

**Main Contributions:**

- Designed a DINOv3-based dual-view image feature extraction pipeline for 2000×1000 UAV images
- Split each image into left and right views and encoded them with shared-weight visual backbones
- Developed a Gated Local Token Mixer to improve cross-view token interaction and local texture modeling
- Used structured multi-head outputs to explicitly predict Green, Dead, and Clover biomass, then reconstruct GDM and Total biomass
- Added a SigLIP + LightGBM / CatBoost semantic compensation branch
- Improved weighted R² from baseline **0.54** to **0.63**

---

### Medical Image Fine-grained Classification

Finalist in the **Jittor Algorithm Challenge**, B leaderboard ranking **7th**.

This project focused on fine-grained BI-RADS classification from breast ultrasound images.

**Tech Stack:** Jittor, EfficientNetV2-S, Multi-Dropout, BN-Neck, 5-Fold CV, TTA, AMP, Albumentations, OpenCV

**Main Contributions:**

- Designed an EfficientNetV2-based fine-grained medical image classification model
- Combined multi-scale features from intermediate and final backbone layers
- Used BN-Neck normalization to stabilize feature representation
- Built a Multi-Dropout classification head with multiple dropout rates and averaged logits
- Used 5-fold cross validation, test-time augmentation, checkpoint ensemble, and mixed-precision training
- Improved robustness under severe class imbalance, especially for high-risk categories with very limited samples

---

### FiLM-Δ-PaiNN: Equivariant GNN for Molecular Potential Prediction

First-author research project on molecular machine learning and AI for Science.

**Tech Stack:** PaiNN, FiLM, Δ-learning, PyTorch, ASE, DeepMD, equivariant GNNs

**Main Contributions:**

- Designed an equivariant graph neural network for high-accuracy molecular potential prediction
- Combined PaiNN-style equivariant message passing with FiLM-based physical information modulation
- Used Δ-learning to reduce the learning difficulty between low-fidelity and high-fidelity energy labels
- Evaluated the model on molecular and periodic benchmark datasets
- Achieved significant error reduction compared with direct-learning baselines and several mainstream equivariant models

---

### Hydrogen Behavior at Mineral Interfaces

Research project on quantum-accuracy simulation of hydrogen behavior at mineral interfaces.

**Tech Stack:** VASP, DeepMD, DPA, LAMMPS, ASE, Python

**Main Contributions:**

- Built a closed-loop workflow from DFT calculations to machine-learning potential training and molecular dynamics simulation
- Generated and curated more than 40k atomic structures for model training
- Trained machine-learning potentials for hydrogen-water-mineral interface systems
- Used LAMMPS and DeepMD to study interfacial adsorption, diffusion, and structural stability
- Improved simulation efficiency while maintaining near-DFT-level energy and force accuracy

---

## Technical Skills

### Programming and Engineering

- Python, C/C++
- PyTorch, Jittor, scikit-learn, timm
- FastAPI, LangGraph, ComfyUI
- OpenCV, Albumentations
- Linux, Git, VS Code Remote SSH

### Computer Vision and Multimodal Learning

- DINOv3
- SigLIP
- EfficientNetV2
- Vision Transformer
- Image classification
- Visual regression
- Multi-scale feature fusion
- Test-time augmentation and model ensemble

### Large Language Models

- Transformer, BERT, GPT
- Qwen
- QLoRA
- DeepSpeed
- vLLM
- DeBERTa
- GTE embedding models
- Rank blending and ensemble learning

### AIGC and Image Generation

- Diffusion models
- FLUX.1 Fill
- Gemini image generation
- LoRA fine-tuning
- Virtual try-on
- Image editing workflow design
- Generation quality control and automatic retry

### AI for Science

- Molecular machine learning
- Equivariant graph neural networks
- PaiNN
- DeepMD
- DPA
- Δ-learning
- Molecular dynamics simulation
- DFT-to-ML potential workflows

---

## Current Interests

I am currently interested in:

- Multimodal AIGC systems for e-commerce and content generation
- LLM fine-tuning and efficient inference
- Computer vision models for small-sample and fine-grained recognition
- Reliable AI workflows with automatic evaluation and retry mechanisms
- Equivariant graph neural networks and machine-learning potentials for molecular simulation

---

## Contact

- Email: 1196973334@qq.com
- GitHub: https://github.com/mayin0902
