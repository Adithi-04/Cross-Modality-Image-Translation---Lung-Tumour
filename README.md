# 🩺 PET–CT Image Translation using Hybrid CycleGAN + Diffusion

This project implements a **Hybrid CycleGAN + Diffusion Model** for **cross-modality image translation** between **Positron Emission Tomography (PET)** and **Computed Tomography (CT)** scans of the lung.  
It generates synthetic CT images from PET scans to improve visualization and support diagnostic analysis.

The proposed approach employs a Hybrid CycleGAN and Diffusion framework to enable bidirectional translation between PET and CT imaging domains. The CycleGAN component learns mapping functions between unpaired PET and CT datasets using adversarial, cycle-consistency, and identity losses to ensure structural and intensity fidelity. This enables the model to generate anatomically consistent CT images from PET scans and vice versa. To further enhance the realism and texture quality of the synthesized outputs, a Diffusion Refinement Module is incorporated post-translation. The diffusion process iteratively denoises the generated images, improving fine-grained details and reducing artifacts. Together, this hybrid setup ensures high-quality, modality-consistent image synthesis while maintaining anatomical integrity essential for medical analysis.

---

## 📂 Dataset
**Source:** [Anti–PD-1 Lung Dataset (TCIA)](https://wiki.cancerimagingarchive.net/pages/viewpage.action?pageId=52758026)  
**Type:** Paired PET/CT scans of lung cancer patients (46 subjects)  
**License:** CC-BY 3.0  

A copy of the dataset access link and instructions is included in the attached ZIP file:  
📎 https://drive.google.com/file/d/1J3DZhIlq5J8SKb1V8mRIY7ebo9H3nvjp/view?usp=sharing
---

## ⚙️ Methodology
**Model:** Hybrid CycleGAN + Diffusion Refinement  
- **CycleGAN:** Learns PET ↔ CT translation from unpaired data  
- **Diffusion Module:** Enhances realism and anatomical accuracy  

**Training Configuration:**
| Parameter | Value |
|------------|--------|
| Image Size | 256×256 |
| Epochs | 200 |
| Learning Rate | 0.0002 |
| Optimizer | Adam |
| Batch Size | 2–4 |

---

## 📊 Evaluation
**Metrics Used:**
- MAE / MSE – Pixel accuracy  
- PSNR – Reconstruction quality  
- SSIM – Structural similarity  
- LPIPS – Perceptual realism  

---



