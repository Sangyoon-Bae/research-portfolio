# Research Portfolio

Collection of my research projects and publications.

## 🔥 Highlight Projects

### 1. POYO-SSL: Predictability-aware Self-Supervised Learning
**Status**: Under Review  
**Description**: Self-supervised framework achieving SOTA in visual decoding from calcium imaging
- 📈 13% performance improvement (SSIM 0.593)
- 🎯 Stable model scaling for foundation-level architectures
- 🔗 Paper: Available upon acceptance | Code: Available upon acceptance

**Key Contributions**:
- Biologically-grounded SSL framework using statistical regularity (skewness/kurtosis) to separate predictable vs. unpredictable neurons
- 12-13% performance gains over baselines with smooth model scaling (unlike prior methods that plateau)
- State-of-the-art visual reconstruction (SSIM: 0.593) from calcium imaging, 1.98× data efficiency

**Why This Matters**:
- Neural data mixes stable regulatory neurons with sparse stimulus-encoding ones—treating them equally creates ill-conditioned optimization
- Turns heterogeneity into an asset: pretrain on predictable neurons, fine-tune on unpredictable ones
- Demonstrates principled data selection enables scalable neural foundation models

**Technical Approach** (General):
- Pretrain on predictable neurons (low skewness/kurtosis) via masked reconstruction + weak auxiliary loss
- Fine-tune on unpredictable neurons with task-specific decoders (UNet for reconstruction)
- Evaluation: movie decoding (SSIM), drifting gratings classification on Allen Brain Observatory

### 2. CausalMamba: Scalable Conditional SSMs
**Status**: Under Review  
**Description**: State-space framework for causal inference from fMRI
- 📈 38% accuracy improvement over baselines
- ✅ Validated on 1,000+ subjects
- 🔗 Paper: Available upon acceptance | Code: Available upon acceptance

**Key Contributions**:
- Two-stage framework: BOLD deconvolution → causal graph inference (37% better than DCM)
- 88% pathway recovery on real fMRI vs. <1% for baselines
- Reveals task-specific network reconfiguration (e.g., L-Insula hub for faces, preSMA for body)

**Why This Matters**:
- fMRI causal inference is ill-posed (hemodynamic distortion hides true causality)
- DCM: computationally intractable. Granger Causality: ignores hemodynamics
- Existing methods fail to recover canonical pathways in 99%+ of subjects

**Technical Approach**:
- Stage 1: Deconvolve BOLD with learnable region-specific HRFs
- Stage 2: Conditional Mamba (ROI-adaptive SSM) predicts directed causal graphs
- Scales linearly O(N) vs. quadratic O(N²) for DCM

### 3. MBBN: Multi-Band Brain Network
**Status**: Under Review  
**Description**: Transformer-based framework for frequency-decomposed brain dynamics modeling
- 📈 Up to 41.3% higher AUROC for ASD classification
- 🎵 Interpretable frequency-band biomarkers for psychiatric applications
- 🧠 Disentangles multi-scale temporal dynamics in brain activity
- 🔗 [Paper](https://arxiv.org/abs/2503.23394) | Code: Available upon acceptance

**Clinical Impact**:
- Discovered frequency-specific biomarkers for autism spectrum disorder
- Interpretable features align with neuroscience findings
- Potential for psychiatric disorder classification and monitoring

**Why This Matters**:
- Most fMRI models treat all frequencies equally → miss important temporal structure
- Brain operates at multiple timescales simultaneously
- Frequency decomposition = built-in interpretability


### 4. SwiFT: Swin 4D fMRI Transformer
**Status**: Published @ NeurIPS 2023 🏆  
**Role**: Co-author (Collaborative research)  
**Description**: Hierarchical transformer architecture for 4D brain imaging
- 🏗️ First to adapt Swin Transformer to 4D spatiotemporal fMRI data
- ⚡ Efficient attention mechanism for high-dimensional brain data
- 📊 Strong performance on multiple downstream tasks
- 🔗 [Paper](https://arxiv.org/abs/2307.05916) | [NeurIPS](https://proceedings.neurips.cc/paper_files/paper/2023/hash/8313b1920ee9c78d846c5798c1ce48be-Abstract-Conference.html)

**Key Contribution**:
Hierarchical window-based attention for 4D fMRI:
- **Spatial windows**: Local 3D brain regions  
- **Temporal windows**: Sequential time frames
- **Shifted windows**: Cross-region communication
- **Hierarchical structure**: Multi-scale representation learning

**Why SwiFT Matters**:
- **Scalability**: Handles high-res 4D data efficiently (O(N) vs O(N²) for standard transformers)
- **Inductive bias**: Window structure respects brain's spatial locality
- **Generalizability**: Strong transfer learning across tasks and datasets

**Technical Innovation**:
- Extended 2D Swin Transformer to 4D (3D space + time)
- Solved computational challenges of full 4D attention
- Maintains hierarchical feature learning from images to brain volumes

**Applications**:
- Brain age prediction
- Disease classification (e.g., Alzheimer's, schizophrenia)
- Pretraining for downstream neuroscience tasks


## 📊 Research Statistics
- 🎓 8 publications (4 first-author)
- 🏆 Best Paper Award @ QCE 2025
- 👥 Mentored 8 students → peer-reviewed publications
- 💾 Experience with 40K+ subject datasets

## 🔧 Code Release Policy
Research code is released upon paper acceptance, following standard academic practices and journal requirements.

For collaboration inquiries: stella.sangyoon.bae@gmail.com
