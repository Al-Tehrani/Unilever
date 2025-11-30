# Unilever Sales Prediction Case

Predict weekly **sales** for ~970 Material–Customer keys for the horizon **2022-46 → 2023-02**, using historical data up to **2022-45**. The primary metric is **WMAPE** (higher accuracy is better), and we also report **Bias**. :contentReference[oaicite:0]{index=0}

---

## 📦 Repository Structure


---

## 🧮 Problem Overview

- **Goal:** For each `Key` (Material–Customer), forecast weekly `Sales` for weeks 2022-46 to 2023-02.  
- **Data columns (high level):** Encoded product/customer info, time/holiday features, promo features (incl. `DiscountedPrice`), and target `Sales`.  
- **Assessment:**  
  - **Accuracy (WMAPE):** `Accuracy = 1 - SUM(|Sales - Prediction|) / SUM(Sales)`  
  - **Bias:** `Bias = SUM(Sales)/SUM(Prediction) - 1`  
  - Objective: **maximize** accuracy with **low** bias. :contentReference[oaicite:1]{index=1}

---

## 🔧 Environment & Setup

### Option A — Conda
```bash
conda create -n py312 python=3.12 -y
conda activate py312
pip install -U pip wheel
pip install -U numpy pandas scikit-learn xgboost lightgbm matplotlib seaborn ipykernel
python -m ipykernel install --user --name py312 --display-name "Python (py312)"
