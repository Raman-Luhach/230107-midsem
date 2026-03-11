# MidSem Part B: Advice Refinement in Knowledge-Based SVMs

This repository contains the full reproduction code and report for the NIPS 2011 paper **"Advice Refinement in Knowledge-Based SVMs"** by Kunapuli, Maclin, and Shavlik.

## Directory Structure

- `task_1_1.ipynb` - `task_1_3.ipynb`: Markdown notebooks breaking down the paper's core contributions, key assumptions, and claims relative to baseline methods.
- `task_2_1.ipynb` - `task_2_3.ipynb`: Code notebooks that load the Wisconsin Breast Cancer dataset, define polyhedral expert advice, and implement the **arkSVM-sla** alternating linear programming solver using `scipy.linprog` to show performance gains at low data regimes.
- `task_3_1.ipynb`: Ablation study proving the necessity of both the rotational refinement ($F_i$) matrix and the advice penalty ($\mu$).
- `task_3_2.ipynb`: Failure Mode analysis demonstrating the structural limitation of the method on non-linear (circular) datasets.
- `data/`: Contains the processed datasets as `.npz` files for immediate reproducibility.
- `results/`: Contains the generated matplotlib plots used in the final report.
- `report.pdf`: The final 4-page IEEE-format synthesis report.
- `llm_task_X_Y.json`: 10 JSON files disclosing LLM usage for the project as required by the MidSem rubric.

## Reproducing the Results

This code relies entirely on standard CPU-based Python libraries. No GPU is required.

### 1. Setup the Environment

It is highly recommended to use a virtual environment.

```bash
cd partB
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### 2. Run the Notebooks

You can execute the notebooks in your IDE (Jupyter/VSCode) or run them sequentially from the command line to reproduce the dataset generation and model training:

```bash
jupyter nbconvert --to notebook --execute --inplace task_2_1.ipynb
jupyter nbconvert --to notebook --execute --inplace task_2_2.ipynb
jupyter nbconvert --to notebook --execute --inplace task_2_3.ipynb
jupyter nbconvert --to notebook --execute --inplace task_3_1.ipynb
jupyter nbconvert --to notebook --execute --inplace task_3_2.ipynb
```

All plots will be automatically saved to the `results/` folder and data splits to the `data/` folder.
