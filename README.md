# Hi, I'm Mayin 👋

I'm an **M.S. student at Nanjing University** (expected 2027), working across **AI agents, multimodal generation, LLM post-training, computer vision, and AI for Science**.

I build AI systems that connect models with tools, measurable evaluation, and practical applications—from virtual try-on and content-aware image adaptation to agent security and molecular simulation.

## Highlights

- 🏅 **Kaggle Expert · 3 Silver Medals + 1 Bronze Medal**
- 🤖 **AI algorithm internship experience at Huawei and Alibaba**, with projects in image adaptation and virtual try-on
- 🥇 **1st place in the individual training track** and **team Silver Award** at the China Merchants Bank Digital Finance Bootcamp
- 🔬 **First-author research** on multi-fidelity equivariant neural potentials and hydrogen transport at mineral interfaces

| Competition | Result | Focus |
| --- | --- | --- |
| **OpenAI × Google × IEEE — AI Agent Security** | **🥈 58 / 4,186 · Top 1.39%** | Tool-using agent security, automated evaluation, replayable tests |
| **Google Jigsaw — Agile Community Rules** | **🥈 42 / 2,445 · Top 1.72%** | Rule-conditioned LLM judging and model ensembles |
| **CSIRO — Image2Biomass Prediction** | **🥈 83 / 3,803 · Top 2.18%** | Visual foundation models and structured regression |
| **NeurIPS 2025 — Open Polymer Prediction** | **🥉 217 / 2,240 · Top 9.69%** | Molecular representations and material property prediction |
| **Jittor Algorithm Challenge — Ultrasound Classification** | **B leaderboard: 7th · National finalist** | Fine-grained medical image recognition |

## Experience & Applied Projects

### Huawei · Retarget-Agent

**AI Application Algorithm Intern · Image Processing Project Lead · Jul 2026–Present**  
**Recognition:** Outstanding Intern

Developed content-aware image adaptation for different aspect ratios, preserving people, products, text, and logos.

- Evaluated **8 processing routes on 600+ business images** and established a quality rubric covering content fidelity, visual completeness, and composition.
- Combined detection, OCR, segmentation, and geometric processing with multimodal judging to generate, score, and select candidates.
- Added controlled generative repair with original subject/text restoration, followed by re-evaluation and fallback.
- On a **fixed evaluation set**, improved the A-grade rate from **77.33%** for the best single method to **93.00%** with Retarget-Agent and **96.33%** with generative repair.
- Delivered FastAPI interfaces and replay-based evaluation with versioned results and failure analysis.

**Tools:** Python · OpenCV · YOLO · OCR · SAM · ComfyUI · FLUX · Multimodal Judge · FastAPI

### Alibaba / Taobao · Virtual Try-on, and OutfitFlow (衣序)

**AIGC Algorithm Project Intern · Nov 2025–Feb 2026**  
**Independent extension:** OutfitFlow, a clothing recommendation and virtual try-on agent system

- Built **FLUX.1 Fill + Redux** and **Gemini image-editing** workflows, with mask control and Face-Fidelity LoRA customization for garment detail and identity consistency.
- Processed **500+ product/model images** in the merchant workflow; reduced production time for selected assets from approximately **7 days to 30 minutes**.
- Independently extended the workflow into OutfitFlow: clothing retrieval, constraint-based outfit planning, virtual try-on, independent quality review, and user confirmation.
- Connected **AgentScope and LangGraph** with multimodal retrieval, BM25 + RRF, persistent preferences, and recoverable execution state.
- Added budget controls, duplicate-call detection, bounded repair, and an independent judge that can re-evaluate existing candidates without generating new images.

**Tools:** FLUX · Gemini · LoRA · SigLIP · ComfyUI · AgentScope · LangGraph · FastAPI · SQLite

## Agent Security & LLM Post-training

### OpenAI × Google × IEEE · AI Agent Security

**Kaggle Silver Medal · Team rank: 58 / 4,186 (Top 1.39%) · Jun–Sep 2026**  
[Official competition: AI Agent Security — Multi-Step Tool Attacks](https://www.kaggle.com/competitions/ai-agent-security-multi-step-tool-attacks/overview)

Contributed to automated security evaluation of tool-using agents in the competition's offline sandbox, focusing on tool misuse and reproducibility under different guardrails.

- Contributed to **40 model-specific test configurations** across GPT-OSS and Gemma, adapting instruction formats and tool parameters to each model.
- Evaluated behavior through **tool execution traces**, checking whether actions actually occurred.
- Helped build a test-generation → sandbox-execution → trace-collection → strategy-selection workflow, configured for **30 probes per strategy**.
- Ranked strategies using a **heuristic estimate of tool-action reward per unit time**, calculated from the final 20 probes.
- Supported up to **2,000 test candidates per model**, with deterministic parameter variation and a single-file `aicomp_sdk` submission for independent replay.
- Analyzed differences between public and hidden guardrail behavior, and moved away from dependence on a fixed test marker.

**Tools:** Python · GPT-OSS · Gemma · Tool Tracing · Automated Red Teaming · aicomp_sdk

### China Merchants Bank · Financial Text-to-SQL

**Training Track Lead · Individual 1st Place · Team Silver Award · Jun 2026**

Built a training and verification workflow for multi-turn financial queries.

- Curated **5,635 interaction turns across 4 database schemas**, covering field selection, joins, aggregation, time boundaries, and conversational context.
- Corrected **345 timezone-related false errors** and increased the proportion of **execution-verified SQL labels from 36.6% to 97.32% (5,484 / 5,635)**.
- Applied **SFT, DPO, and GRPO** to Qwen3.5-2B with LoRA, using query execution feedback for supervision and preference construction.
- Built a **PostgreSQL execution verifier** to distinguish executable SQL from queries that return the correct result.

*97.32% measures validated data labels, not model test accuracy.*

**Tools:** Qwen3.5-2B · LoRA · SFT · DPO · GRPO / RLVR · PostgreSQL · Twinkle

## Selected Competition Solutions

### Google Jigsaw · Rule-conditioned LLM Judge

**Silver Medal · 42 / 2,445 · Final AUC: 0.92909**  
[Code & methodology](https://github.com/mayin0902/google-jigsaw-agile-community-rules-silver)

- Modeled moderation as **rule + comment → violation**, including generalization to unseen rules.
- Fine-tuned Qwen3-4B with **4-bit QLoRA**, completion-only supervision, and single-token scoring.
- Combined a generative LLM branch, **GTE + Triplet Loss** metric learning, and a **DeBERTa-v3** classifier through rank blending.
- Used **DeepSpeed ZeRO-2** and **vLLM** for training and batch inference.

### CSIRO · Image2Biomass Prediction

**Silver Medal · 83 / 3,803 · Weighted R²: 0.54 → 0.63**  
[Code & methodology](https://github.com/mayin0902/csiro-image2biomass-silver)

Predicted five pasture biomass targets from a small dataset of **357 high-resolution images**.

- Built a shared **DINOv3 ViT-Huge** backbone over two image views, with a **Gated Local Token Mixer** for local texture and spatial information.
- Predicted Green, Dead, and Clover biomass, then reconstructed GDM and Total to preserve target relationships.
- Added **SigLIP + LightGBM / CatBoost** branches and used four-fold validation and late blending.

### NeurIPS 2025 · Open Polymer Prediction

**Bronze Medal · 217 / 2,240**  
[Code & methodology](https://github.com/mayin0902/neurips-open-polymer-prediction-bronze)

- Built a polymer property prediction workflow from molecular structures, combining **RDKit / Mordred descriptors, molecular fingerprints, and graph representations**.
- Combined graph models and gradient-boosted trees to capture complementary structure–property relationships.
- Addressed missing labels, different target scales, feature selection, and multi-target validation.

### Jittor · Fine-grained Ultrasound Classification

**B leaderboard: 7th · National finalist**  
[Code & methodology](https://github.com/mayin0902/7th-jittor-cainiao-ultrasound-images)

- Built an **EfficientNetV2** model with multi-scale feature fusion, **BN-Neck**, and **Multi-Dropout** for breast ultrasound BI-RADS grading.
- Explored ordinal label modeling with cumulative multi-label targets and **BCEWithLogitsLoss**.
- Used **five-fold validation, TTA, checkpoint ensembles, and Jittor AMP** to improve robustness with limited and imbalanced data.

## Research · AI for Science

### PRISM · Multi-fidelity Equivariant Neural Potentials

**First-author research**

- Developed a shared equivariant graph representation to learn medium- and high-fidelity energy/force corrections to a low-cost physical baseline.
- Combined **multi-fidelity residual learning** with joint energy–force training, data alignment, and controlled ablations.
- With **200 MP2 configurations** on PBC-Water, achieved **0.48 meV/atom energy MAE** and **42.31 meV/Å force MAE**.
- Reduced energy error by **67.3% vs. Δ-EGNN** and force error by **26.4% vs. Δ-PaiNN** in the reported benchmark comparisons.

**Tools:** PyTorch · SchNetPack · Equivariant GNNs · Multi-fidelity Learning · Linux / HPC

### Hydrogen Transport at Mineral Interfaces

**First-author research · Jiangsu Provincial Frontier Technology R&D Project**

- Built a workflow spanning structure sampling, **DFT labeling, data quality checks, machine-learning potential training, and molecular dynamics**.
- Processed **40k+ atomic configurations** using VASP, DeepMD / DPA / MACE, ASE, and LAMMPS.
- Analyzed hydrogen aggregation and transport in nanoconfined brine and mineral interfaces through density, clustering, diffusion, orientation, and residence-time statistics.

## Technical Skills

| Area | Tools & Methods |
| --- | --- |
| **Programming & Engineering** | Python, C/C++, Linux, Git, FastAPI, SQLite, PostgreSQL, SSE / WebSocket |
| **Agents & Evaluation** | LangGraph, AgentScope, tool integration, multimodal RAG, BM25 / RRF, persistent state, execution verification, replay evaluation |
| **LLMs & Post-training** | Qwen, LoRA / QLoRA, SFT, DPO, GRPO, DeepSpeed, vLLM, GTE, DeBERTa |
| **Vision & Generation** | PyTorch, Jittor, OpenCV, DINOv3, SigLIP, EfficientNetV2, FLUX, Gemini, ComfyUI |
| **Machine Learning** | scikit-learn, LightGBM, CatBoost, XGBoost, cross-validation, ensemble learning |
| **AI for Science** | Equivariant GNNs, SchNetPack, RDKit, ASE, VASP, DeepMD, DPA, MACE, LAMMPS |

## Education

- **Nanjing University** — M.S. in Physical Chemistry, Kuang Yaming Honors School · **2024–2027 (expected)**  
  Research focus: AI for Science, molecular machine learning, and scientific computing.
- **Nanjing Tech University** — B.Eng. in Chemical Engineering and Technology · **2020–2024**  
  Rank: **3 / 257** · GPA: **3.83 / 4.0**.

## Current Interests

Reliable tool-using agents · Multimodal generation and evaluation · LLM post-training with verifiable feedback · Small-sample visual learning · Equivariant models for molecular simulation

## Contact

[Email](mailto:1196973334@qq.com) · [GitHub](https://github.com/mayin0902)
