# Data Mining Project: Recommender Systems and Graph Mining on MovieLens

## Project Overview

This project explores **Graph Mining**, **Clustering**, and **Recommender Systems** using the **MovieLens 32M / 25M** dataset. The goal is to analyze user-movie interactions, extract meaningful communities, and build personalized recommendation models using both course-taught techniques and advanced methods.

## Research Questions

1. **How does data sparsity affect the performance of collaborative filtering vs. graph-based methods?**
2. **Can community detection (clustering) on the user-movie graph identify distinct taste groups?**
3. **Do temporal dynamics (changing user preferences) significantly impact recommendation accuracy?**
4. **Can we mitigate popularity bias using hybrid recommendation approaches?**

## Dataset

**MovieLens 25M** (approximating the 32M version mentioned) - A stable benchmark dataset for recommender systems.

| Attribute | Value |
|-----------|-------|
| Source | [GroupLens Research](https://grouplens.org/datasets/movielens/25m/) |
| Size | 25 Million ratings |
| Users | ~162,000 |
| Movies | ~62,000 |
| Tags | ~1 Million genome tags |
| License | Research Use |

## Techniques

### Course Techniques
- **Frequent Itemset Mining** (Apriori/FP-Growth on viewing history)
- **Graph Mining** (User-Movie Bipartite Graph, Community Detection)
- **Clustering** (K-Means on User/Movie Embeddings)
- **Text Mining** (Tag/Genre Analysis with TF-IDF)
- **LSH** (Locality Sensitive Hashing for similar item retrieval)

### Beyond-Course Techniques
- **Matrix Factorization** (SVD, ALS)
- **Graph Neural Networks (GNNs)** (e.g., LightGCN)
- **Neural Collaborative Filtering**
- **Transformer-based Recommendation** (Sequential modeling)

## Repository Structure

```
├── Checkpoint1_Dataset_Selection_EDA.ipynb   # This checkpoint
├── README.md                                  # Project overview
├── requirements.txt                           # Python dependencies
├── data/                                      # Data directory
│   ├── ml-25m/                               # Raw data (downloaded by notebook)
│   └── movielens_cleaned.csv                 # Cleaned subset for analysis
└── figures/                                   # Generated visualizations
```

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook

### Installation

```bash
# Clone the repository
git clone https://github.com/YaswanthReddy/data-mining-project.git
cd data-mining-project

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter
jupyter notebook
```



## Author

Yaswanth Reddy

## Citations

```
F. Maxwell Harper and Joseph A. Konstan. 2015. The MovieLens Datasets: History and Context. 
ACM Transactions on Interactive Intelligent Systems (TiiS) 5, 4: 19:1–19:19. 
https://doi.org/10.1145/2827872
```
