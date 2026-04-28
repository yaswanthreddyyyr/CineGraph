# CineGraph: Understanding User Taste Through Genre Patterns

CineGraph analyzes movie-rating behavior to understand how user taste clusters emerge from genre preferences and how those clusters relate to recommendation quality under extreme sparsity. The project combines exploratory data mining, user segmentation, and collaborative filtering to produce practical guidance for building better recommendation systems.

## Start Here

- Main deliverable notebook: [main_notebook.ipynb](main_notebook.ipynb)
- Project video: [https://youtu.be/cnrTiw0UEc4?si=mjIDUDf3VAhQOOvY](https://youtu.be/cnrTiw0UEc4?si=mjIDUDf3VAhQOOvY)

## Research Questions

1. Do genre preference patterns form interpretable user taste personas?
2. Under extreme sparsity, does Truncated SVD outperform Item-KNN, and where does each method fail?
3. How does model performance vary across user segments discovered through clustering?

## Results Summary

The analysis finds that meaningful genre-based user personas can be identified and used to explain recommendation behavior. In a matrix with more than 99.7% sparsity, both SVD and Item-KNN improve over a baseline, but SVD delivers stronger practical performance because it maintains near-complete coverage while preserving competitive error metrics.

## Data

- Dataset: MovieLens 25M
- Source: [GroupLens MovieLens 25M](https://grouplens.org/datasets/movielens/25m/)
- The raw dataset is not committed to GitHub.
- For automatic download and extraction, run [checkpoints/checkpoint_1.ipynb](checkpoints/checkpoint_1.ipynb) first.
- Checkpoint 1 downloads MovieLens 25M into `data/` when files are missing.
- Basic preprocessing done in notebooks:
  - timestamp parsing
  - user/movie filtering for modeling subsets
  - genre feature engineering and normalization for clustering

## Reproducibility

This project was developed in notebook-first workflow (Colab-compatible) and can be reproduced locally with Jupyter.

Colab environment export used for this deliverable:

```python
!pip freeze > requirements.txt
from google.colab import files
files.download('requirements.txt')
!python --version
```

This is the required method to capture all package versions from the Colab runtime and place `requirements.txt` at the repo root.

1. Create and activate a Python environment.
2. Install dependencies from [requirements.txt](requirements.txt).
3. Run [checkpoints/checkpoint_1.ipynb](checkpoints/checkpoint_1.ipynb) to download/extract data into `data/` if needed.
4. Review progression notebooks in order:
	- [checkpoints/checkpoint_1.ipynb](checkpoints/checkpoint_1.ipynb)
	- [checkpoints/checkpoint_2.ipynb](checkpoints/checkpoint_2.ipynb)
5. Run the final curated notebook:
	- [main_notebook.ipynb](main_notebook.ipynb)

Example setup:

```bash
git clone https://github.com/yaswanthreddyyyr/CineGraph.git
cd CineGraph
python -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook
```

Python version used (local dev): 3.12.6
Python version for submission should be captured from Colab with `!python --version`.

## Key Dependencies

- python 3.12.6
- pandas >= 1.5.0
- numpy >= 1.21.0
- scipy >= 1.9.0
- scikit-learn >= 1.2.0
- scikit-surprise >= 1.1.3
- matplotlib >= 3.5.0
- seaborn >= 0.12.0
- networkx >= 3.0

For the complete dependency list, see [requirements.txt](requirements.txt).

## Repository Structure

```text
.
├── .gitignore
├── README.md
├── main_notebook.ipynb
├── requirements.txt
├── checkpoints/
│   ├── checkpoint_1.ipynb
│   └── checkpoint_2.ipynb
└── data/
	 └── ml-25m/   # download locally; not committed to GitHub
```

## Author

Yaswanth Reddy
