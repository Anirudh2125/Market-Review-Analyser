# Market Review Semantic Clustering and Theme Analysis

## Objective
Cluster **approximately 10,000 market reviews per month** into **semantic themes** to identify dominant and recurring patterns in large-scale review data.

---

## Pipeline Overview
The project follows a fully unsupervised semantic analysis pipeline:

1. Text embedding generation  
2. Embedding model comparison and selection  
3. Density-based clustering  
4. Cluster labeling and interpretation  
5. Quantitative and qualitative evaluation  
6. Visualization of cluster structure  

---

## Embedding Generation and Model Comparison

### Approach
- Generated **contextual sentence embeddings** using the **SentenceTransformer framework**.
- Benchmarked multiple pretrained models, including:
  - `all-MiniLM-L6-v2`
  - `all-mpnet-base-v2`
- Compared models based on:
  - Semantic coherence of clusters  
  - Separation in embedding space  
  - Computational efficiency  

### Model Selection
- Selected **MiniLM-L6-v2** due to its strong balance between **embedding quality**, **clustering coherence**, and **runtime efficiency**.

---

## Semantic Clustering

### Approach
- Applied **HDBSCAN density-based clustering** to identify semantically coherent review groups.
- Enabled automatic discovery of clusters without predefining the number of themes.
- Supported variable cluster densities to reflect real-world review distributions.

---

## Cluster Labeling

### Approach
- Assigned **interpretable cluster labels** using **TF-IDF–based keyword extraction**.
- Extracted high-weight terms per cluster to summarize dominant semantic themes.
- Avoided manual annotation while maintaining interpretability.

---

## Evaluation Methodology

### Quantitative Evaluation
Clustering quality was evaluated using:
- **Silhouette Score** – to measure intra-cluster semantic coherence  
- **Davies–Bouldin Index** – to assess inter-cluster separation  
- **Cluster Stability Analysis** – to verify robustness across perturbations  

### Qualitative Evaluation
- Used **UMAP-based 2D projections** to visually inspect:
  - Cluster separation  
  - Density structure  
  - Overall embedding organization  

---

## Results
- Produced semantically coherent clusters that grouped reviews by **contextual meaning** rather than lexical similarity.
- Identified dominant and recurring themes across monthly datasets.
- Assigned clear, interpretable labels to clusters using TF-IDF.
- Validated clustering robustness through both quantitative metrics and UMAP visualizations.

---

## Key Takeaways
- Demonstrated effective use of **semantic embeddings for large-scale unsupervised text analysis**.
- Showed informed **model selection reasoning** through embedding benchmarking.
- Combined **quantitative evaluation** with **visual validation** for reliable clustering analysis.
