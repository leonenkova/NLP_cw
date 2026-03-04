# NLP_cw

> Binary classification of **Patronising and Condescending Language** (PCL) in news media using DeBERTa-v3-base.

---

## Quick Links

| | |
|---|---|
| **Main notebook** | [BestModel/Exercise4.ipynb](BestModel/Exercise4.ipynb) |
| **Results** | [BestModel/results.json](BestModel/results.json) |
| **Final Report** | [Exercise6_Report.pdf](Exercise6_Report.pdf) |
| **Dev predictions** | [BestModel/dev.txt](BestModel/dev.txt) |
| **Test predictions** | [BestModel/test.txt](BestModel/test.txt) |

---

## Results

| Model | Dev F1 | t\* | Test F1 |
|---|:---:|:---:|:---:|
| RoBERTa-base (given baseline) | 0.4800 | — | — |
| RoBERTa-base (Run 1) | 0.5981 | 0.35 | 0.5265 |
| **DeBERTa-v3-base (BestModel)** | **0.6045** | **0.50** | **0.5642** |

- ⬆️ **+0.1245** dev F1 over the given baseline
- ⏱️ Trained for **4 epochs** on T4 GPU (~18 min), early stopped at epoch 7
- 🎯 Optimal threshold **t\* = 0.50** — perfectly calibrated probabilities

---

## Repository Structure

```
NLP_cw/
│
├── BestModel/
│   ├── Exercise4.ipynb                     ← Main training notebook
│   ├── best_model.py                       ← Model weights
│   ├── dev.txt                             ← Dev set predictions (0/1 per line)
│   ├── test.txt                            ← Test set predictions (0/1 per line)
│   └── results.json                        ← Full training metrics & hyperparameters
│
├── Exercise6_Report.pdf                    ← Exercise 6 — Final Report
└── README.md
```
