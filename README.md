# Customer Review Clustering and Topic Modeling

## Overview
This project explores customer reviews using Natural Language Processing (NLP), semantic embeddings, unsupervised clustering, and topic modeling.

## Objectives
- Group similar customer reviews using K-Means.
- Generate semantic embeddings using Sentence Transformers.
- Discover topics using BERTopic.
- Extract representative keywords using TF-IDF and c-TF-IDF.
- Visualize clusters and interpret discovered topics.

## Techniques
- Sentence-BERT (SBERT)
- K-Means clustering
- UMAP dimensionality reduction
- HDBSCAN clustering
- TF-IDF and class-based TF-IDF (c-TF-IDF)
- PCA visualization

## Project Structure
- `customer_review_topic_modeling.ipynb`: Main analysis notebook
- `requirements.txt`: Python dependencies
- `data/`: Input dataset
- `outputs/`: Generated topic assignments and summaries

## How to Run
1. Clone or download this repository.
2. Install dependencies with `pip install -r requirements.txt`.
3. Place the permitted dataset at `data/reviews.csv`.
4. Open the notebook in Jupyter.
5. Run the cells in order.

## Results
The project compares a five-cluster K-Means baseline with BERTopic's data-driven topic discovery. See the notebook for topic distributions, representative keywords, visualizations, and model comparisons.

## Limitations
Topic quality depends on the dataset and model settings. Topic labels require human interpretation, and HDBSCAN may leave some reviews unassigned.
Synthetic reviews are cleaner and more grammatical than real user text. Models trained only on this data will see distribution shift on production feedback with heavy slang, typos, or code-switching.
Labels are single-class. Real reviews often span categories (a scam complaint that is also a service complaint); this dataset forces one label.
English only.

## Future Improvements
- Evaluate topic coherence.
- Tune UMAP and HDBSCAN parameters.
- Refine topic representations.
- Build an interactive dashboard.
- 
## Dataset
This project uses the Product Reviews Sentiment dataset by Ankit Aglawe, hosted on Hugging Face.

- Source: https://huggingface.co/datasets/AnkitAI/product-reviews-sentiment
- License: MIT
- Data type:Synthetic English customer reviews
- Usage: Semantic clustering and topic modeling with K-Means and BERTopic.

The dataset is synthetic and does not represent actual customer transactions or verified real-world customer experiences. Please refer to the original dataset page for its license, provenance, and limitations.

## License
This project is released under the MIT License. Dataset and third-party model licenses remain separate.