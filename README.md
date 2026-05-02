# Predicting E-commerce Customer Device Usage

> **Should an e-commerce company invest in its mobile app or its website? A linear regression on 500 customers gives a clear answer.**

![Hero](https://images.unsplash.com/photo-1556742049-0cfed4f6a45d?w=1200&h=400&fit=crop)

![Python](https://img.shields.io/badge/python-3.x-blue) ![Notebook](https://img.shields.io/badge/jupyter-notebook-orange) ![Model](https://img.shields.io/badge/model-linear--regression-green)

---

## About

**Who:** Gyanesh Samanta — built as a hands-on regression case study.
**What:** A supervised learning project predicting `Yearly Amount Spent` per customer from session and engagement metrics.
**When:** Originally explored in 2021; revisited and re-shared in 2026.
**Where:** Jupyter notebook, runnable locally on any Python 3 install.
**Why:** Translate raw e-commerce telemetry into a concrete strategic recommendation: app vs. website.

## The Story

The dataset has **500 customers** and **8 columns** — average session length, time on the app, time on the website, length of membership, and yearly spend.

A naive guess would say: more time on website = more spend. The regression says otherwise.

Key findings:

- **Length of Membership** is by far the strongest driver of yearly spend (coefficient ~61).
- **Time on App** is the second strongest (coefficient ~38).
- **Time on Website** is nearly flat (coefficient ~0.19) — practically no relationship to spend.

The strategic takeaway: either **double down on the app** (where engagement converts to revenue) or **fix the website** (where it currently doesn't). Loyalty (membership length) dwarfs both — retention beats acquisition.

The model achieves a strong fit on the holdout set with residuals approximately normally distributed, confirming linear regression is an appropriate model class for this data.

## Gallery

The notebook contains:

- Pair plots (Seaborn) of every numeric feature vs. yearly spend
- Joint plots highlighting the app-vs-website divergence
- Residual distribution plot validating the linear-model assumption
- Coefficient table with business interpretation

---

## Tech Stack

- **Python 3** — language
- **Jupyter Notebook** — interactive analysis
- **pandas** — data wrangling
- **NumPy** — numerics
- **scikit-learn** — `LinearRegression`, `train_test_split`, metrics
- **Seaborn / Matplotlib** — visualization

## Repo Structure

```
Predicting-ecommerce-customers-device-usage/
├── data.csv                  # 500-row customer dataset
├── regression model.ipynb    # Full analysis notebook
└── README.md
```

## Getting Started

```bash
git clone https://github.com/GyaneshSamanta/Predicting-ecommerce-customers-device-usage.git
cd Predicting-ecommerce-customers-device-usage
pip install pandas numpy scikit-learn seaborn matplotlib jupyter
jupyter notebook "regression model.ipynb"
```

Run all cells top-to-bottom. The dataset loads from `data.csv` in the repo root.

## Contributing

PRs welcome — especially alternative models (Ridge, Lasso, gradient boosting) for comparison, or feature-engineering experiments.

## License

MIT — free to use, modify, and learn from.

## Credits

Built by **Gyanesh Samanta** ([@GyaneshSamanta](https://github.com/GyaneshSamanta)). Dataset is a popular public e-commerce teaching dataset.
