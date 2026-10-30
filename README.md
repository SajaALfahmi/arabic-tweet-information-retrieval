# Arabic Tweet Information Retrieval System

An Arabic Information Retrieval (IR) system developed to explore and compare traditional lexical retrieval methods with neural re-ranking techniques for retrieving relevant Arabic tweets.

## Overview

This project implements an end-to-end Arabic text retrieval pipeline, combining lexical retrieval models, query expansion, and AraBERT-based neural re-ranking.

The system processes Arabic tweets, builds an inverted index, retrieves candidate documents, and ranks results using different information retrieval approaches.

## Features

- **Arabic Text Preprocessing:** Text normalization, tokenization, and noise removal.
- **Boolean Retrieval:** Document retrieval using Boolean AND operations and an inverted index.
- **TF-IDF Retrieval:** Ranking documents using TF-IDF vectorization and cosine similarity.
- **BM25 Retrieval:** Ranking documents using the BM25 probabilistic retrieval model.
- **Query Expansion:** Exploring Word2Vec embeddings to expand search queries.
- **Neural Re-ranking:** Using AraBERT embeddings and cosine similarity to re-rank retrieved documents.
- **Evaluation:** Implementing Precision@K, Mean Average Precision (MAP), and Normalized Discounted Cumulative Gain (nDCG).

## Technologies & Libraries

- Python
- Pandas and NumPy
- Scikit-learn
- Gensim (Word2Vec)
- PyTorch
- Hugging Face Transformers
- AraBERT (`aubmindlab/bert-base-arabertv02`)
- rank-bm25
- Matplotlib

## Project Workflow

1. Load and preprocess the Arabic tweet dataset.
2. Normalize Arabic text and prepare tokens.
3. Build an inverted index for document retrieval.
4. Implement Boolean retrieval.
5. Apply TF-IDF and BM25 for ranked retrieval.
6. Explore query expansion using Word2Vec.
7. Apply AraBERT-based neural re-ranking.
8. Evaluate retrieval approaches using information retrieval metrics.

## Dataset

The project uses the ArSarcasm training dataset (`ArSarcasm_train.csv`), provided as part of the course materials.

The dataset is not included in this repository. Users must obtain it separately and place the required CSV file in the notebook's working directory before running the notebook.

## Installation

Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

1. Clone this repository.
2. Install the dependencies.
3. Obtain the dataset and place `ArSarcasm_train.csv` in the appropriate working directory.
4. Open the Jupyter Notebook.
5. Run the notebook cells sequentially.

**Note:** Loading the AraBERT model requires an internet connection on the first run. GPU acceleration is optional; the notebook can use CPU when CUDA is unavailable.

## Evaluation

The notebook implements the following evaluation metrics:

- Precision@K
- Mean Average Precision (MAP)
- Normalized Discounted Cumulative Gain (nDCG)

The evaluation section includes relevance judgments for a limited set of queries. The evaluation dataset should be expanded before drawing general conclusions about comparative model performance.

## Future Improvements

- Expand relevance judgments across all evaluation queries.
- Explore more advanced Arabic language models.
- Improve query expansion and neural re-ranking.
- Develop a search interface for interactive Arabic tweet retrieval.

## Project Type

Academic / Technical Project — Information Retrieval and Natural Language Processing (NLP).

## Contributors

- Saja Alfahmi
- Shahad Madkhali
- Arwa Alroqi
