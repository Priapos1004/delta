# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the course repository for **DELTA (Deep Learning for Text Analytics)**, an MSc module at Humboldt-University of Berlin (Summer Semester 2026). It contains lecture slides, tutorial Jupyter notebooks, and graded task assignments covering deep learning and NLP.

## Repository Structure

- `lecture_slides/` — PDF lecture slides (topics 1–9: intro, DL foundations, NLP, word embeddings, RNNs, transformers, transfer learning)
- `tutorial_notebooks/` — Jupyter notebooks for hands-on tutorials (Tut1–Tut10), plus supporting data files (CSVs, pickles, pretrained models)
- `task1/` — Graded assignment: build and tune a neural network for regression on tabular data (train/test CSVs + task notebook)
- `requirements.txt` — Python dependencies

## Environment Setup

- **Python version:** 3.11.15
- Install dependencies: `pip install -r requirements.txt`
- Key frameworks: TensorFlow/Keras 3.x, PyTorch, Hugging Face Transformers, scikit-learn, XGBoost, Optuna, Keras Tuner, Gensim, NLTK

## Working with Notebooks

Run notebooks from their containing directory so relative CSV/data paths resolve correctly. For example:
```bash
cd tutorial_notebooks && jupyter notebook
cd task1 && jupyter notebook
```

**One cell at a time:** When building or editing notebooks together, only write/modify one cell at a time, then wait for the user to run it and confirm the output before moving to the next cell. This prevents errors from cascading downstream.

## Graded Tasks

Before working on a graded task (e.g. `task1/`), read the relevant tutorial notebooks in `tutorial_notebooks/` to understand the approaches, patterns, and techniques used in the course. Match the style and methods from the tutorials.

**Notebook style:** the grader is a domain expert. Write for that audience.

- **Keep documentation lean.** Don't explain ML fundamentals (why scaling matters, what KFold is). Document the *decisions* (which library, which CV scheme, which HP ranges) and skip the textbook background.
- **Tell a consistent story.** Each section should flow from the previous one. If a markdown cell asserts a fact (e.g. "features have very different scales"), an earlier cell must have produced the evidence.
- **Prefer many small cells.** One concept or one decision per cell.
- **Match the plan.** If you said you'd include an EDA / NaN check / descriptive-stats step, deliver it — don't silently skip "obvious" steps.
- **One short line for docstrings.** Satisfies the "documented code" rubric without padding.

## Data Loading Convention

CSV files are loaded with: `pd.read_csv(file_name, sep=',', header=0, index_col=0)` — note the `index_col=0` parameter.

## Task 1 Context

Regression task with 19 features, 1875 train / 625 test samples. Required components: preprocessing, 3 benchmarks (linear, tree-based, untuned NN), hyperparameter-tuned NN with regularization, train/val loss plot, results table. Evaluated on RMSE.
