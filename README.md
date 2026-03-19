# 💊 AI-Driven Drug Interaction Detection

![Python](https://img.shields.io/badge/Language-Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Tool-Jupyter%20Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Domain](https://img.shields.io/badge/Domain-Healthcare%20AI-FF4B4B?style=for-the-badge)
![Algorithm](https://img.shields.io/badge/Algorithm-Apriori%20%7C%20Association%20Rule%20Mining-6DB33F?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)

> An AI-driven drug-drug interaction (DDI) detection system that applies association rule mining (Apriori algorithm) on real-world pharmaceutical datasets to identify frequent drug combinations and classify their interaction severity — supporting patient safety and clinical decision-making.

---

## 📖 Table of Contents

- [About the Project](#about-the-project)
- [Problem Statement](#problem-statement)
- [Datasets](#datasets)
- [Methodology](#methodology)
- [Key Results](#key-results)
- [Tech Stack](#tech-stack)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Project Structure](#project-structure)
- [Future Improvements](#future-improvements)
- [Author](#author)

---

## About the Project

Adverse drug-drug interactions (DDIs) are a leading cause of preventable hospital admissions, yet traditional interaction databases are often **incomplete, manually curated, and slow to update**. This project applies **AI-driven association rule mining** to automatically discover frequent drug co-occurrence patterns and flag potentially dangerous combinations from real clinical datasets.

Using the **Apriori algorithm** across multiple pharmaceutical data sources — DDInter and BioSNAP — this notebook demonstrates how data mining techniques can complement existing pharmacological knowledge to enhance drug safety monitoring at scale.

This project showcases applied skills in **healthcare AI**, **unsupervised pattern mining**, **data preprocessing**, and **clinical data analysis**.

---

## Problem Statement

> *Drug interactions can cause severe adverse health effects. Traditional curated databases are incomplete and cannot scale to the growing number of approved drug combinations. This project applies association rule mining to detect frequent drug interaction patterns automatically — reducing reliance on manual curation and improving patient safety.*

---

## Datasets

Three real-world drug interaction datasets were used:

| Dataset | Source | Description |
|---|---|---|
| `DDI_data.csv` | DDInter Database | General drug-drug interaction records |
| `ddinter_downloads_code_A.csv` | DDInter (Code A) | DDI records — severity category A |
| `ddinter_downloads_code_B.csv` | DDInter (Code B) | DDI records — severity category B |
| `ddinter_downloads_code_L.csv` | DDInter (Code L) | DDI records — severity category L |
| `biosnap.tsv` | BioSNAP (Stanford) | Large-scale biomedical drug interaction network |

> 📌 **DDInter** is a comprehensive drug-drug interaction database. **BioSNAP** is a biomedical network dataset from Stanford University used extensively in computational drug discovery research.

---

## Methodology
```
1. Data Loading & Preprocessing
   └── Load DDInter (A, B, L) + BioSNAP datasets
   └── Clean, normalize, and encode drug pair records
   └── Handle missing values and duplicates

2. Exploratory Data Analysis
   └── Distribution of interaction types
   └── Frequency analysis of drug co-occurrences
   └── Severity category breakdown

3. Association Rule Mining (Apriori Algorithm)
   └── Encode drug combinations as transactional data
   └── Apply Apriori with minimum support threshold
   └── Generate frequent itemsets
   └── Extract association rules with confidence & lift metrics

4. Rule Evaluation & Filtering
   └── Filter rules by support, confidence, and lift
   └── Categorize interactions by severity
   └── Identify high-risk drug combinations

5. Visualization & Insights
   └── Plot frequent itemsets
   └── Visualize top association rules
   └── Summarize key findings
```

**Key Metrics Used:**
| Metric | Definition |
|---|---|
| **Support** | How frequently a drug combination appears in the dataset |
| **Confidence** | Probability that drug B is flagged given drug A is present |
| **Lift** | Strength of the association beyond random chance (lift > 1 = meaningful) |

---

## Key Results

- Successfully identified **frequent drug combination patterns** across DDInter severity categories A, B, and L
- Applied Apriori mining on **BioSNAP** biomedical network data for cross-dataset validation
- Generated association rules with **support, confidence, and lift** metrics to rank interaction risk
- Demonstrated that **data mining can surface interaction patterns** not easily captured by manual curation alone

> 📝 Update this section with your specific support/confidence thresholds and top rules discovered after running the notebook.

---

## Tech Stack

| Tool | Purpose |
|---|---|
| Python 3.x | Core programming language |
| Pandas | Data loading, cleaning, and manipulation |
| NumPy | Numerical operations |
| MLxtend | Apriori algorithm and association rule mining |
| Matplotlib / Seaborn | Visualizations |
| Jupyter Notebook | Interactive analysis environment |

---

## Getting Started

### Prerequisites
```bash
pip install pandas numpy matplotlib seaborn mlxtend jupyter
```

### Installation

1. **Clone the repository**
```bash
   git clone https://github.com/nandita0401/ai_drug_interaction.git
   cd ai_drug_interaction
```

2. **Launch Jupyter Notebook**
```bash
   jupyter notebook
```

3. **Open and run the notebook**
```
   Open AI_Driven_Drug_Interaction.ipynb
   Kernel → Restart & Run All
```

> ⚠️ All dataset files (`DDI_data.csv`, `biosnap.tsv`, `ddinter_downloads_code_*.csv`) must be present in the root directory before running the notebook.

---

## Project Structure
```
ai_drug_interaction/
├── AI_Driven_Drug_Interaction.ipynb   # Main analysis notebook
├── DDI_data.csv                       # General DDI dataset
├── ddinter_downloads_code_A.csv       # DDInter severity A
├── ddinter_downloads_code_B.csv       # DDInter severity B
├── ddinter_downloads_code_L.csv       # DDInter severity L
├── biosnap.tsv                        # BioSNAP drug interaction network
└── README.md
```

---

## Future Improvements

- [ ] Extend analysis to **all DDInter severity categories** for a complete interaction profile
- [ ] Apply **graph-based methods** (GNN) on BioSNAP network for deeper DDI prediction
- [ ] Build a **drug interaction lookup tool** — input two drugs, get interaction risk score
- [ ] Integrate with **PubChem or DrugBank API** for real-time drug data enrichment
- [ ] Deploy as a **clinical decision support web app** using Streamlit or FastAPI
- [ ] Add **NLP pipeline** to extract DDI patterns from medical literature

---

## Author

**Nandita Bharambe**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-nanditabharambe-0A66C2?style=flat&logo=linkedin)](https://www.linkedin.com/in/nanditabharambe/)
[![GitHub](https://img.shields.io/badge/GitHub-nandita0401-181717?style=flat&logo=github)](https://github.com/nandita0401)

---

> 💡 *This project sits at the intersection of AI and healthcare — two fields where getting it right genuinely matters. Applying data mining to drug safety shows how machine learning can move from pattern recognition to potentially life-saving clinical insight.*
