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
