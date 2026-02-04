# SciLiPS: Scientific Paper Limitations Dataset

> **Note:** The dataset is currently being reorganized/arranged and will be **ready within the next couple of days**.  
> The final folder/file arrangement will be completed within the next couple of days.

SciLiPS (Scientific Papers Limitations Dataset) is a supervised resource for **evidence-grounded limitation extraction** from scientific papers.

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

SciLiPS currently includes **150 research papers** from two domains:

- **Natural Language Processing (NLP)**  
  - **100 papers from ACL 2024 and 2025 proceedings**
- **Computer Vision**  
  - **50 papers from IEEE/CVF venues (e.g., CVPR 2024)**

For every paper, SciLiPS provides:

- The **full paper PDFs** in `papers_pdf/`
- The same papers **parsed into structured JSON** in `papers_json/`
- A CSV file containing **author-written limitation sentences** and their **evidence sentences** from outside the Limitations section:  
  - **`scilips_limitations_evidence.csv`**

---

## Limitation Categories

Each limitation is assigned one normalized category from:

- `data_quality`
- `method/dataset_mismatch`
- `limited_scope`
- `evaluation/metrics`
- `compute/scale`
- `other`

---

## Repository Structure

```text
.
├── papers_pdf/                       # 150 original PDFs (100 ACL, 50 CVF)
│   ├── <paper_id_1>.pdf
│   ├── <paper_id_2>.pdf
│   └── ...
├── papers_json/                      # 150 parsed JSON files (one per paper)
│   ├── <paper_id_1>.json
│   ├── <paper_id_2>.json
│   └── ...
└── scilips_limitations_evidence.csv  # author limitations + evidence sentences
