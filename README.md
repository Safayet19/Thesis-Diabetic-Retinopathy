# Risk-Controlled Selective Prediction for Diabetic Retinopathy Screening

This repository contains the Jupyter notebooks associated with our research, **“Risk-Controlled Selective Prediction with Retinal Foundation Models for Referable Diabetic Retinopathy Screening Under Distribution Shift.”**

The study investigates automatic non-referral screening using frozen retinal foundation models, probability calibration, and Learn-Then-Test (LTT) risk certification. It evaluates source-domain screening performance on APTOS 2019 and examines the reliability of source-selected policies on two external datasets, IDRiD and Messidor-2.

The research also investigates lesion-morphology-based screening using Grade-Boundary Lesion Screening (GBLS) and Shift-Robust Grade-Boundary Lesion Screening (SR-GBLS).

## Repository Structure

The repository contains seven research notebooks.

| Notebook | Research component |
|---|---|
| `01_Thesis_DR_APTOS_RETOUND.ipynb` | RETFound-Green experiments on APTOS |
| `02_DR_APTOS_MedSigLIP.ipynb` | MedSigLIP-based experiments |
| `03_Thesis_External_Validation.ipynb` | External evaluation on IDRiD and Messidor-2 |
| `04_DR_APTOS_DINOv2_Large.ipynb` | DINOv2-Large experiments |
| `05_DR_GBLS_SR_GBLS.ipynb` | GBLS and SR-GBLS investigation |
| `06_External_Failure_Analysis.ipynb` | External screening failure analysis |
| `07_Thesis_Result_&_Analysis.ipynb` | Experimental results and comparative analysis |

## Datasets

The research uses three publicly available retinal fundus image datasets.

- **APTOS 2019:** Source-domain model development, calibration, and internal evaluation.
- **IDRiD:** Independent external evaluation.
- **Messidor-2:** Independent external evaluation.

Referable diabetic retinopathy is defined using severity grades 2–4, while grades 0–1 are treated as non-referable.

## Methodology

The study includes the following research components:

1. Feature extraction using frozen RETFound-Green, DINOv2-Large, and MedSigLIP encoders.
2. Binary referable-DR classification and temperature scaling.
3. Risk-controlled automatic non-referral using Learn-Then-Test certification.
4. External evaluation of source-selected screening policies.
5. Lesion-morphology-based screening using GBLS and SR-GBLS.
6. Risk–coverage comparisons and grade-specific failure analysis.

## Key Findings

At a predefined 5% conditional-risk target, the RETFound-Green screening policies achieved **51.06% mean automatic-clearance coverage** and **0.37% mean observed risk** on held-out APTOS test images.

When transferred unchanged to external datasets, mean observed risk increased to **14.73% on IDRiD** and **14.66% on Messidor-2**.

These findings highlight the importance of evaluating automatic non-referral risk under distribution shift rather than relying only on conventional classification performance.

## Reproducibility

The experiments were developed in Python using PyTorch and supporting machine-learning libraries.

The notebooks document different components of the research workflow. Reproducing the experiments requires access to the relevant datasets, pretrained model checkpoints, and compatible execution environments.

Dataset locations and file paths may need to be configured for the environment in which the notebooks are executed.

## Research Authors

- Safayet Ullah
- Md. Jubayer Islam
- Tanvirul Hoque Faysal

**Department of Computer Science and Engineering**  
Southeast University, Bangladesh

**Research Supervisor:** Prof. Dr. Abdul Kadar Muhammad Masum
