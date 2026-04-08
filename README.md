# SAR Rental Fleet Clustering

This project implements a complete end-to-end K-Means clustering pipeline for analyzing car rental usage behavior. It was developed to optimize fleet management strategies, including maintenance scheduling, dynamic pricing, and targeted fleet expansion.

## Overview

The dataset comes from the **SAR Rental Car Service** in San Francisco. It contains trip-level records detailing travel types, package information, booking methods, geo-coordinates, and timestamps. 

By applying unsupervised machine learning (K-Means), we segment the rental trips into distinct behavioral clusters, turning raw trip data into actionable business intelligence.

## Delivered Artifacts

- **`SAR_Rental_Clustering.ipynb`**: The primary Jupyter Notebook containing all code, analysis, and visualizations across 9 detailed phases.
- **`use_case_diagram.png`**: UML Use Case diagram mapping out the system interactions between various actors and system features.
- **`class_diagram.png`**: UML Class diagram detailing the system architecture, preprocessing pipeline, and model flow.
- **`SAR Rental.csv`**: The source dataset (approx. 10,000 trips).

## Methodology Structure

The analysis pipeline is divided into the following phases:

1. **Data Loading & Exploration**: Profiling the raw dataset.
2. **Feature Engineering**: Creating 8 new domain-specific features (e.g., Haversine distance, booking lead time, rental frequency).
3. **Data Preprocessing**: Handling complementary nulls strategically and removing outliers to prepare for distance-based clustering.
4. **Optimal K Selection**: Using Elbow Method and Silhouette Scores to determine the ideal number of clusters.
5. **K-Means Clustering**: Fitting the model to the scaled feature set.
6. **Cluster Validation**: Verifying separation using Davies-Bouldin index, Calinski-Harabasz score, and hierarchical dendrograms.
7. **Cluster Profiling & Visualization**: Detailed analysis and plotting of the generated segments.
8. **Business Recommendations**: Tailored operational strategies assigned to each cluster.
9. **System Design (UML)**: Modeling the analytical system using PlantUML.

## Key Insights

During preprocessing, it was discovered that **Hourly Rental Packages** and **Point-to-Point GPS tracking** are mutually exclusive features. Handling this through strategic zero-filling preserved the natural distinction between travel types, yielding robust, well-separated clusters.

## How to Run

1. Clone this repository.
2. Ensure you have Python installed along with `pandas`, `numpy`, `scikit-learn`, `matplotlib`, and `seaborn`.
3. Open `SAR_Rental_Clustering.ipynb` via Jupyter Notebook or JupyterLab.
4. Select **Kernel -> Restart & Run All** to execute the pipeline from start to finish.
