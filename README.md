# SciLiPS: Scientific Paper Limitations Dataset

SciLiPS (Scientific Papers Limitations Dataset) is a supervision resource for **evidence-grounded limitation extraction** from scientific papers.

For each paper, SciLiPS links:

- **Explicit limitation sentences** written by the paper’s authors  
  → typically from a *Limitations* (or equivalent) subsection  
- to **related evidence sentences** that appear **outside** the Limitations section  
  → with their **section provenance** and a **normalized limitation category**

This enables models to **detect limitations** and **justify them** with verifiable in-paper evidence and section context.

---

## Dataset Overview

> **Note:** The dataset is currently being reorganized/arranged.  
> The final folder/file arrangement will be completed within the next couple of days.

SciLiPS currently includes **100 research papers** from two domains:

- **Natural Language Processing (NLP)**  
  - 70 papers from ACL 2024 and 2025 proceedings
- **Computer Vision**  
  - 30 papers from IEEE/CVF 2024 CVPR

For every paper, SciLiPS provides:

- The **full paper** (original PDF)
- The same paper **parsed into sections and sentences**
- A set of **explicit limitation sentences** extracted from the Limitations (or equivalent) subsection
- A **category** for each limitation, chosen from:
  - `data_quality`
  - `method/dataset_mismatch`
  - `limited_scope`
  - `evaluation/metrics`
  - `compute/scale`
  - `other`
- One or more **related evidence sentences** for each limitation,  
  sampled **only from non-Limitations sections**, each with:
  - Sentence text  
  - Section name / provenance  

---

## Repository Structure

The repository is organized as follows:

```text
.
├── papers/              # 100 original PDFs (70 ACL, 30 CVPR)
│   ├── <paper_id_1>.pdf
│   ├── <paper_id_2>.pdf
│   └── ...
└── json/                # 100 JSON files, one per paper
    ├── <paper_id_1>.json
    ├── <paper_id_2>.json
    └── ...
