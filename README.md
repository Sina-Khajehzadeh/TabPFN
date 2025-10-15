# ⚡ TabPFN • XGBoost • Logistic — Tabular Benchmark

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![License: MIT](https://img.shields.io/badge/License-MIT-green)
![TabPFN](https://img.shields.io/badge/Model-TabPFN-black)
![XGBoost](https://img.shields.io/badge/Model-XGBoost-orange)
![LogReg](https://img.shields.io/badge/Model-Logistic%20Regression-lightgrey)

> 🔎 **What is this?**  
> Rusable pipeline to compare **TabPFN**, **XGBoost**, and **Logistic Regression** on **tabular** data.  
> It includes group-aware splits, repeated simulations (e.g., 10×), and polished metrics/plots.

---

## ✨ Highlights
- <mark>Drop-in</mark> prep for any CSV: drop meta/labels → numeric-only → `fillna(0.0)`  
- **GroupShuffleSplit** by subject/ID to prevent train–test leakage  
- Repeated simulations (**10×**) with **AUROC / Balanced Accuracy / MSE** + runtime per iteration  
- Plots: single ROC on a fixed test, **10 faint ROC overlays**, AUROC/MSE/runtime **boxplots**  
- **CPU/GPU-friendly TabPFN** adapter (caps rows/cols on CPU to avoid OOM)

---

## 🚀 Quickstart
```bash
pip install -r requirements.txt



## 📎 Appendix A — Demo dataset used in this repo

**AMR-UTI: Antimicrobial Resistance in Urinary Tract Infections**  
<https://www.physionet.org/content/antimicrobial-resistance-uti/1.0.0/>

- De-identified EHR for **>80k** UTI specimens (2007–2016).
- **Labels:** resistance (1) vs susceptible (0) for **NIT**, **SXT**, **CIP**, **LVX** → modeled as **four separate binary tasks**.
- **Cohort:** recommended to use `uncomplicated == 1`.
- **Time split:** `is_train == 1` (2007–2013) for training, `is_train == 0` (2014–2016) for testing.
- **Why classification?** Each drug is a **yes/no** “resistant?” decision; predicted probabilities help guide empiric therapy.

> Please follow PhysioNet’s terms and cite the dataset & original paper as requested on the project page.




## ▶️ Run the notebook in Google Colab

Launch the end-to-end benchmark notebook directly in your colab

**Direct links**
- GitHub (view the .ipynb): https://github.com/Sina-Khajehzadeh/TabPFN/blob/main/notebooks/tabular_benchmark.ipynb

> 🔧 **Adjust if needed:** replace `Sina-Khajehzadeh/TabPFN` or `main` with your actual GitHub username/repo/branch,  
> and update the path if your notebook filename or folder is different.

### Notes
- On first run in Colab, install deps in the first cell, e.g.:
- For private repos, Colab may prompt you to **sign in to GitHub** or grant access.
- Large models (TabPFN) run faster with **GPU**: Runtime → Change runtime type → **GPU**.



