# CS133 Final Project – Predicting High-Priced Video Games

This repository contains my CS133 final project, which explores video game pricing data and builds machine learning models to predict whether a game is **“high-priced”** relative to others on the same platform.

The core of the project lives in a single Jupyter notebook:

- **`CS133_Final_Project.ipynb`**

---

## 📌 Project Overview

The goal of this project is to answer:

> Given information about a game (platform, genre, release year, etc.), can we predict whether it is in the **top quartile of prices** on its platform?

The project includes:

1. **Data cleaning & preprocessing**
2. **Exploratory data analysis (EDA)** with visualizations
3. **Feature engineering** for categorical and numeric data
4. **Binary classification models** (e.g., Logistic Regression, Random Forest, SVM)
5. **Model evaluation** and discussion of limitations

---

## 🧮 Target Definition

The machine learning task is **binary classification**.

For each platform, I compute the **75th percentile** of game prices. A game is labeled:

- `1` (**high price**) if its price is **≥ platform’s 75th percentile**
- `0` (**not high price**) otherwise

This produces a platform-relative measure of “high price” rather than using a fixed dollar threshold.

---

## 📂 Repository Contents

- `CS133_Final_Project.ipynb`  
  Main notebook with:
  - Data loading & cleaning  
  - EDA and plots  
  - Feature engineering  
  - Model training & evaluation  

- `README.md`  
  Project description (this file).

> If you add any extra files (e.g., `data/`, `figures/`, `src/`), update this section accordingly.

---

## 🗃️ Dataset

- The notebook uses a dataset of **video games and their prices** (e.g., Steam/console titles).
- Columns used include:
  - `platform`
  - `genre` / `genres`
  - `release_date` / `release_year`
  - `prices`
- Additional columns may be used in EDA (e.g., ratings, owners, etc., if available).

> **Note:** You may need to adjust the dataset path in the first data-loading cell of the notebook to match your local setup.

---

## 🛠️ Requirements

This project uses Python and common data science libraries. A typical environment will include:

- Python 3.8+
- Jupyter Notebook or JupyterLab

Key packages (install via `pip` or `conda`):

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `scikit-learn`
- `plotly` (for interactive plots)
- `kaleido` (optional, for saving Plotly figures as images)

Example installation:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn plotly kaleido
