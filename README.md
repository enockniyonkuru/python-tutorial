# Python for Dry-Lab Biology: A Beginner Tutorial

A three-part, hands-on introduction to Python, data science and machine learning for wet-lab scientists starting computational work. No coding experience needed.

**Author:** Enock Niyonkuru · **Questions?** [enock.niyonkuru@ucsf.edu](mailto:enock.niyonkuru@ucsf.edu)

The series prepares you for our lab project: **fine-tuning a single-cell foundation model** (such as Geneformer or scGPT) on our own data.

## The notebooks

Work through them in order. Each one builds on the one before.

| # | Notebook | What you learn |
|---|---|---|
| 1 | [`01_Python_Basics.ipynb`](01_Python_Basics.ipynb) | Setting up Python, variables and functions, `if` / loops, lists / sets / dictionaries, classes and objects |
| 2 | [`02_Intro_to_Data_Science.ipynb`](02_Intro_to_Data_Science.ipynb) | pandas tables, loading CSV / Excel / Parquet, filtering and grouping, exploratory analysis, plots |
| 3 | [`03_Intro_to_Machine_Learning.ipynb`](03_Intro_to_Machine_Learning.ipynb) | AI vs ML vs foundation models, GitHub and Hugging Face, supervised, unsupervised and semi-supervised learning, fine-tuning |

Every section follows the same pattern:
1. **Intro:** the idea in plain English, plus a lab analogy.
2. **Let's run it:** short code cells to run.
3. **Try it yourself:** a small exercise with step-by-step hints.

## Getting started

### Option A: Google Colab (easiest, nothing to install)
1. Go to <https://colab.research.google.com> and sign in with a Google account.
2. **File → Upload notebook** and pick a notebook from this folder.
3. For Part 2, also upload `dummy_cells.csv` (folder icon in the left sidebar → upload).

### Option B: VS Code on your laptop
1. Install [Python](https://www.python.org/downloads/) and [VS Code](https://code.visualstudio.com), plus the **Python** and **Jupyter** extensions.
2. In a terminal, inside this folder:
   ```bash
   python3 -m venv myenv
   source myenv/bin/activate          # Windows: myenv\Scripts\activate
   pip install pandas numpy matplotlib seaborn scikit-learn openpyxl pyarrow ipykernel
   ```
3. Open a notebook, click **Select Kernel** (top right) and choose `myenv`.

**Optional (Part 3 only):** one cell downloads a small model from Hugging Face. It needs `pip install transformers torch` and an internet connection, and it skips politely without them.

## Tips
- Run cells **from top to bottom** with **Shift + Enter**.
- A red error? Read the **last line**. It usually names the problem (a typo, a skipped cell, wrong indentation).
- You can't break anything. Change numbers, re-run, and see what happens.
- Everything runs in seconds to a minute on an ordinary laptop or the free Colab CPU.

## Files

| Path | What it is |
|---|---|
| `01_…`, `02_…`, `03_…` | The tutorial notebooks |
| `dummy_cells.csv` | Simulated single-cell metadata (600 cells) used in Part 2. Not real data. |

## Datasets
- **`dummy_cells.csv`** (Part 2): simulated cell-level QC data: cell type, condition, genes detected, counts, % mitochondrial reads, and one marker gene (CD3E). Some values are deliberately missing so you can practise cleaning.
- **Breast cancer** and **handwritten digits** (Part 3): small datasets built into scikit-learn, so there is nothing to download. They stand in for single-cell data so every cell runs quickly.

## After the series
1. Learn [scanpy and AnnData](https://scanpy.readthedocs.io), the standard single-cell tools in Python (start with the PBMC 3k tutorial).
2. Read the model cards for Geneformer and scGPT on Hugging Face.
3. Work through the [Hugging Face course](https://huggingface.co/learn) to learn real fine-tuning.

## Author and contact
Created by **Enock Niyonkuru**.

Questions, stuck on an exercise, or found a mistake? Email **[enock.niyonkuru@ucsf.edu](mailto:enock.niyonkuru@ucsf.edu)**. No question is too basic.
