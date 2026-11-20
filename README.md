# Nexvia Technologies Internship Projects

A portfolio index for two separate data science projects completed for Nexvia Technologies. Each project remains an independent repository, with its own codebase, dependencies, documentation, tests, and execution workflow. This repository links them as Git submodules; it does not combine their applications or duplicate their project files.

## Projects

### DS-01 — Customer Churn Intelligence

**Business objective:** identify customers at risk of churn and support evidence-informed retention planning through predictive, customer-value, survival, and treatment-uplift analyses.

**Project:** [`DS-01-Customer-Churn-Intelligence/`](DS-01-Customer-Churn-Intelligence/) · [Public repository](https://github.com/ayobamiiiii/customer-churn-intelligence) · [Project README](DS-01-Customer-Churn-Intelligence/README.md)

**Technology and capabilities:** Python, Streamlit, LightGBM, scikit-learn, SHAP, lifelines (Kaplan–Meier and Cox models), CausalML uplift analysis, PostgreSQL, pandas, and automated tests. The project includes a churn prediction interface, model insights, value segmentation, a scenario-based retention ROI simulator, survival analysis, and an optional Hillstrom email-experiment uplift analysis. PostgreSQL integration is optional.

The project README documents its evaluated tuned model: ROC-AUC 86.52% on 1,409 held-out customers at the documented threshold, plus the complete confusion matrix and other classification measures. The modeled ROI simulator is assumption-based; it is not a causal estimate of telecom campaign results.

### DS-02 — Nationwide Demand Forecasting and Inventory Optimization

**Business objective:** forecast daily product demand and evaluate replenishment decisions using time-series validation, hierarchical summaries, prediction intervals, and constrained inventory optimization.

**Project:** [`DS-02-Retail-Demand-Forecasting/`](DS-02-Retail-Demand-Forecasting/) · [Public repository](https://github.com/ayobamiiiii/DS-02-Retail-Demand-Forecasting-Inventory-Optimization) · [Project README](DS-02-Retail-Demand-Forecasting/README.md)

**Technology and capabilities:** Python, pandas, NumPy, LightGBM, Prophet, Darts Regression, Plotly Dash, OR-Tools CP-SAT, and automated tests. The project provides a six-tab dashboard, held-out forecasting comparisons, hierarchy rollups, empirical prediction intervals, and inventory recommendations with documented proxy costs.

The verified Favorita evaluation covers 39 items, 116 item-store series, and three stores—not the entire nationwide store network. On its primary holdout, LightGBM WAPE was 29.53% versus 40.94% for the weekly naive baseline. The OR-Tools run returned 110 optimal recommendations; its 47.83% objective-cost reduction is modeled under assumed costs and stock inputs, not realized business savings. Temporal Fusion Transformer (TFT) remains pending GPU training and has no claimed metrics or predictions.

## Repository layout

```text
Nexvia-Internship-Projects/
├── README.md
├── .gitmodules
├── DS-01-Customer-Churn-Intelligence/   # Git submodule
└── DS-02-Retail-Demand-Forecasting/     # Git submodule
```

The detailed architecture, data dictionary/API notes, model methodology, tests, and execution commands are maintained inside each project's README and documentation.

## Clone and update

Clone this portfolio index together with both projects:

```bash
git clone --recurse-submodules https://github.com/ayobamiiiii/Nexvia-Internship-Projects.git
cd Nexvia-Internship-Projects
```

If you cloned without submodules, initialize them with:

```bash
git submodule update --init --recursive
```

Each project has its own dependency requirements and should be installed and run separately. Follow the setup and execution instructions in the corresponding project README; do not install both requirements files into one shared environment.

## Data and privacy

Datasets, customer-level prediction rows, virtual environments, credentials, private reflection material, and submission recordings are not stored in this mother repository. Follow each project README for authorized local data setup. The submodules point to the existing public project repositories and preserve their independent commit histories.
