## SECTION 1 : PROJECT TITLE

# **DualSight: Multispectral Object Detection with ICAFusion and Knowledge Distillation**

An RGB–Infrared Pedestrian Detection System with Lightweight Architecture and Performance Optimization.

---

## SECTION 2 : EXECUTIVE SUMMARY / PAPER ABSTRACT

Traditional object detectors struggle under varying lighting conditions:

- RGB images lose effectiveness at night.
- Infrared (IR) images lack fine details during the day.

To solve this, we build **DualSight**, a multispectral object detection system that fuses RGB and thermal information. We adopt the **ICAFusion** dual-stream architecture, which extracts features from both modalities and performs **mid-level fusion with cross-attention**, achieving state-of-the-art accuracy on the KAIST dataset.

However, the original ICAFusion model contains **120M+ parameters**, making it too heavy for real-time deployment. To address this, we propose a **modality-level knowledge distillation (KD)** strategy that transfers cross-modal knowledge from the large teacher model to a **lightweight student model (6M parameters)**.

**Key Innovations:**

- Adapted ICAFusion dual-stream architecture into a practical training pipeline.
- Progressive fusion at multiple semantic levels (F3–F5).
- **Modality-level distillation (teacher RGB/IR → student fusion features).**
- **Two-stage training with warm-up for stable convergence.**

**Results:**

- Fusion model significantly outperforms RGB-only and IR-only.
- KD improves student model accuracy by **+0.036 mAP@0.5**.
- Student model retains **real-time performance** while approaching teacher accuracy.

**DualSight** successfully balances **accuracy and efficiency**, making multispectral detection practical for real-world scenarios.

---

## SECTION 3 : CREDITS / PROJECT CONTRIBUTION

| Official Full Name | Student ID | Work Items (Who Did What)                                                                                                                                                                                                                                                            | Email              |
| -------------------- | :----------: | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------- |
| **Zhu Kaixu**      | A0328919M | Dataset preprocessing (alignment, normalization), ICAFusion architecture adaptation, dual-stream fusion implementation, knowledge distillation design & coding, experiment design/execution (modality comparison, KD ablation), GUI development, Section 3 & 4 of report, demo video | e1553246@u.nus.edu |
| **Chen Xinyu**     | A0317887J | Business problem analysis, requirement analysis, use case design, Section 1, 2 & 5 of report, documentation support                                                                                                                                                                  | e1519747@u.nus.edu |

---

## SECTION 4 : VIDEO OF SYSTEM MODELLING & USE CASE DEMO

**Refer to demo video in `/video` folder.**

The demo video includes:

- System workflow (RGB + IR fusion)
- GUI interaction and usage
- Detection result visualization

---

## SECTION 5 : USER GUIDE

### 5.1 System Requirements

- OS: Windows / Ubuntu / macOS
- Python 3.8+
- NVIDIA GPU ≥ 8GB VRAM (recommended)
- CUDA & cuDNN (for acceleration)

---

### 5.2 Installation

```bash
# Clone project
git clone <repository-url>
cd DualSight

# Create environment
conda create -n dualsight python=3.8
conda activate dualsight

# Install dependencies
pip install -r requirements.txt
```

### 5.3 Run the GUI Application

```bash
5.4 Usage Steps

Click Browse RGB Video → select RGB input.

Click Browse IR Video → select corresponding IR input.

Click Start Detection.

System will:

Load pretrained fusion model

Extr5.4 Usage Steps

Click Browse RGB Video → select RGB input.

Click Browse IR Video → select corresponding IR input.

Click Start Detection.

System will:

Load pretrained fusion model

Extract cross-modal features

Perform detection

Display results with bounding boxes

Save or view output detection video.

The system assumes RGB and IR are frame-aligned. Minor misalignments are compensated by fusion blocks.act cross-modal features

Perform detection

Display results with bounding boxes

Save or view output detection video.

The system assumes RGB and IR are frame-aligned. Minor misalignments are compensated by fusion blocks.python gui.py
```

### 5.4 Usage Steps

1. Click **Browse RGB Video** → select RGB input.
2. Click **Browse IR Video** → select corresponding IR input.
3. Click **Start Detection**.
4. System will:

    - Load pretrained fusion model
    - Extract cross-modal features
    - Perform detection
    - Display results with bounding boxes
5. Save output detection video.

The system assumes RGB and IR are frame-aligned. Minor misalignments are compensated by fusion blocks.

---

## SECTION 6 : PROJECT REPORT / PAPER

Refer to full project report in Github Folder: `ProjectReport`.

---

## SECTION 7 : MISCELLANEOUS

Refer to `Miscellaneous` folder for additional resources.

Possible contents:

- Survey / Dataset
- UI Mockups / Prototype images
- PPT slides or presentation assets

---

**This project is part of the Artificial Intelligent Systems Programme at NUS-ISS.**