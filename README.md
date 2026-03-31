# Listener Persona Clustering

Acoustic feature-based listener segmentation and persona discovery using 114,000 Spotify tracks.

## Overview

This project clusters Spotify tracks based on their acoustic features and assigns listener personas to each cluster using music psychology literature (Rentfrow & Gosling, 2003; Rentfrow et al., 2011). The pipeline supports persona prediction for new tracks and persona analysis based on listening history.

## Dataset

Source: https://www.kaggle.com/code/jessieangelica/spotify-tracks-dataset/input  
The dataset (`dataset.csv`) is included in the repository.

## Requirements

```bash
pip install pandas numpy scikit-learn matplotlib seaborn scipy
```

## Usage

Open and run `Listener_persona_clustering.ipynb` end-to-end. The notebook is organized as follows:

1. Data loading & EDA
2. Correlation analysis & feature selection
3. Standardization & PCA visualization
4. K-Means clustering (k=8)
5. Hierarchical clustering (stratified sample)
6. DBSCAN
7. Algorithm comparison
8. Persona assignment
9. Persona prediction for new tracks
10. Listening history analysis

## Results

| Model | Clusters | Silhouette | Davies-Bouldin |
|---|---|---|---|
| K-Means | 8 | 0.2113 | 1.3243 |
| Hierarchical | 8 | 0.1518 | 1.4787 |
| DBSCAN | 2 | 0.6200* | 0.4173* |

*DBSCAN evaluated on 4,560-record sample with only 2 clusters.

## Identified Personas

| Cluster | Persona |
|---|---|
| 0 | Cultural / Traditional Listener |
| 1 | Sophisticated / Reflective Listener |
| 2 | Intense / Rebellious Listener |
| 3 | Energetic / Social Dancer |
| 4 | Mood-Lift / Casual Listener |
| 5 | Flow / Electronic Immersion |
| 6 | Calm / Focus Listener |
| 7 | Rhythmic / Urban Dancer |

## References

- Rentfrow & Gosling (2003). *The do re mi's of everyday life.* J. Pers. Soc. Psychol.
- Rentfrow et al. (2011). *The structure of musical preferences: A five-factor model.* J. Pers. Soc. Psychol.

---
