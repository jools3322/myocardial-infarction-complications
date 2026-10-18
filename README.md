# Predicting Complications After Myocardial Infarction

**Scientific Programming (MSB1015) — Maastricht University**  
**Author:** Jools Parren

## Project overview

This project investigates whether clinical information collected during hospitalization can help predict complications after myocardial infarction (MI).

Using the UCI Myocardial Infarction Complications dataset, I compare machine-learning methods, investigate whether additional information collected during the first 72 hours improves prediction, and explore differences between patient groups using a branching clinical representation.

The analysis is carried out in Python using a Jupyter Notebook.

## Dataset

The project uses the [UCI Myocardial Infarction Complications dataset](https://archive.ics.uci.edu/dataset/579/myocardial+infarction+complications).

The dataset contains 1,700 patient records, including clinical characteristics, treatment information, and outcomes recorded during hospitalization. This analysis focuses on 11 binary post-MI complications.

**To obtain the data:**

1. Open the UCI dataset link above.
2. Download and extract the dataset.
3. Place the file `MI.data` in the same folder as the Jupyter Notebook.

The notebook reads the original data file directly.

## Repository contents

- `MSB1015_Project_MI_Jools_Parren.ipynb` — Main Jupyter Notebook containing the complete analysis, code, figures, and results.
- `README.md` — Project description and instructions for reproducing the analysis.

The dataset (`MI.data`) can be downloaded from the UCI Machine Learning Repository using the link provided above. 

## Software and required libraries

The analysis uses **Python 3** and **Jupyter Notebook**.

The following Python packages are required:

- `numpy`
- `pandas`
- `matplotlib`
- `scikit-learn`
- `xgboost`
- `scipy`
- `statsmodels`
- `networkx`
- `elpigraph`

Most packages can be installed with:

```bash
python -m pip install numpy pandas matplotlib scikit-learn xgboost scipy statsmodels networkx jupyter
```

For the elastic principal tree analysis, install the ElPiGraph Python package:

```bash
python -m pip install elpigraph-python
```

## How to run the analysis

1. Download the Jupyter Notebook from this repository.
2. Download `MI.data` from the UCI dataset page and place it in the same folder.
3. Install Python, Jupyter, and the required libraries listed above.
4. Open the notebook in Jupyter Notebook, JupyterLab, or VS Code.
5. Select a Python environment containing the required packages.
6. Run the notebook from top to bottom using **Run All**.
 
## Analysis workflow

The notebook is organized into seven parts:

1. **Data preparation:** Load the dataset, examine missing values, identify complication outcomes, and construct time-specific predictor sets.
2. **Preprocessing and study design:** Define preprocessing pipelines and create training and independent test cohorts.
3. **Model development and selection:** Compare classification algorithms and select a suitable model using cross-validation.
4. **Individual complication prediction:** Train and evaluate separate models for the 11 post-MI complications.
5. **Temporal analysis:** Compare predictive performance at admission and after 24, 48, and 72 hours.
6. **Model interpretation:** Investigate which clinical variables and groups of predictors contribute most to prediction.
7. **Clinical pathway analysis:** Construct an elastic principal tree and examine complication frequencies across the identified patient groups.

## Data source

Golovenkin, S. E., et al. (2020). *Myocardial Infarction Complications*. UCI Machine Learning Repository.

https://archive.ics.uci.edu/dataset/579/myocardial+infarction+complications
