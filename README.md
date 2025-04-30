# Introspective LLM Evaluation Toolkit

## Overview

This repository contains the data, code, and evaluation framework developed as part of the MSc research project titled:

**"Quantifying AI Self-Reflection: A Computational Approach to Measuring Introspective Behavior in Large Language Models (LLMs)"**

It includes introspective output data from four large language models (GPT-4, Claude v3.7, DeepSeek-R1, and LLaMa-3.2), alongside a Python-based evaluation notebook that measures self-reflective behavior using five key metrics:

- **Semantic Coherence**  
- **Sentiment Polarity**  
- **Intent Fulfilment**  
- **Calibration**  
- **Hallucinated Introspection**  

---

## Repository Structure

```
.
├── introspection_data_all_models.csv         # Raw introspective outputs from all four models
├── scored_introspection_dataset.csv          # Final dataset with all metric scores applied
├── introspection_evaluator.ipynb             # Main Jupyter Notebook to evaluate model introspection
├── flowchart_diagram.png                     # Diagram illustrating the introspection scoring workflow
└── README.md                                 # (This file)
```

---

## System Requirements

To successfully run the project, ensure you have the following:

### Hardware Requirements
- RAM: 4 GB minimum (8 GB recommended for smooth processing)
- Disk Space: ~500 MB available

### Software Requirements
- **Python version:** `3.9` or `3.10` (tested)
- **Environment Management:** [Anaconda](https://www.anaconda.com/) (recommended)
- **Notebook Interface:** [Jupyter Notebook or JupyterLab](https://jupyter.org/)

---

## Setup Instructions

### Step 1: Clone the Repository or Download the Files

```bash
git clone https://github.com/your_username/introspective-llm-evaluation.git
cd introspective-llm-evaluation
```

### Step 2: Create and Activate a Virtual Environment (Anaconda Recommended)

```bash
conda create -n llm_eval_env python=3.10
conda activate llm_eval_env
```

### Step 3: Install Required Dependencies

```bash
pip install -r requirements.txt
```

Or manually install:

```bash
pip install pandas numpy sentence_transformers vaderSentiment matplotlib seaborn scikit-learn
```

---

## Files Description

| File | Description |
|------|-------------|
| `introspection_data_all_models.csv` | Contains the 240 raw introspective responses (20 prompts × 4 models × 3 trials). |
| `scored_introspection_dataset.csv` | Fully scored dataset with all evaluation metric values applied. |
| `introspection_evaluator.ipynb` | Main Jupyter Notebook for data loading, metric computation, and model comparison. |
| `flowchart_diagram.png` | A diagram showing the introspection evaluation pipeline. |

---

## How to Use

1. Launch **Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   Or use:
   ```bash
   jupyter lab
   ```

2. Open `introspection_evaluator.ipynb`.

3. Run cells sequentially to:
   - Load and preprocess data
   - Compute semantic coherence using Sentence-BERT
   - Analyze sentiment using VADER
   - Score intent fulfilment and calibration
   - Detect hallucinated introspection
   - Visualize comparison summaries per model

---

## Research Aim

The goal is to construct a behavioral, multi-metric framework to evaluate introspective tendencies in LLMs and assess how model alignment strategies influence the production of reflective outputs.

---

## Ethical Considerations

This work addresses several AI ethics concerns including:

- **Hallucinated self-disclosures**  
- **Epistemic manipulation through emotional language**  
- **Risks of anthropomorphic misinterpretation**

These are documented with supporting analysis in the full dissertation and supported by outputs generated using this toolkit.
