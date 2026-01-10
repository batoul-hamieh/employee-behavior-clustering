# Clustering Work Arrangements by Productivity, Well-Being, and Work–Life Balance

## Rationale
Given the absence of predefined labels, this study employs clustering to reveal latent employee profiles shaped by productivity, mental and physical well-being, and work–life balance. The analysis examines how these profiles align with onsite, remote, and hybrid work arrangements in the post-pandemic era, providing insights for organizational decision-making and workforce management.

## Dataset
- **Title:** post_pandemic_remote_work_health_impact_2025 
- **Source:** [Kaggle]( https://www.kaggle.com/datasets/pratyushpuri/remote-work-health-impact-survey-2025)  
- **Collection Period:** 2025  
- **Unit of Analysis:** Individual employees  

The dataset includes survey responses on work modality, productivity, physical and mental well-being, social engagement, and work–life balance. 
Both categorical and numerical features are present.

## Exploratory Data Analysis 
- Inspection of missing values and data types (categorical, ordinal, numerical).  
- Visualization of distributions for features.  
- Identification of necessary cleaning and transformation steps.  

## Data Preprocessing
- One-hot encoding and label encoding for categorical variables.  
- Standardization of numerical variables to ensure comparable scales.   

## Feature Engineering
- Aggregation of multiple related survey columns to produce **three core features** representing:  
  1. Work modality intensity  
  2. Psychophysiological health strain    
  3. Perceived WellBeing Social Index 
- Dropped original single columns to focus the clustering analysis on these derived features.  

## Clustering
- Determination of the optimal number of clusters using the **Elbow Method** and **Silhouette Score**.  
- Application of K-Means clustering on the engineered feature set.  
- Visualization of clusters in **3D feature space**.  
- Analysis of feature distributions by cluster.  
- Assignment of interpretable cluster labels for meaningful insights.  

### Cluster Profiles
**Cluster 0: Thriving**  
- **Rationale:**  Individuals in this cluster maintain the highest work modality intensity and social well-being while exhibiting low psychophysiological health strain.  

**Cluster 1: Detached**  
- **Rationale:** These employees exhibit the lowest work modality intensity and social well-being. Due to minimal pressure, they maintain the lowest and most stable health strain scores.  

**Cluster 2: Vulnerable**  
- **Rationale:** Despite moderate work intensity, these individuals suffer from the highest health strain scores. Combined with low social well-being, this indicates they lack the resources to cope with even average work demands, making them highly susceptible to burnout.  

## Visualizations
- Distribution plots of core features by cluster.  
- 3D scatter plots of cluster assignments.  
- Violin and boxplots to compare feature trends across clusters.  

## Usage
1. Clone the repository:
   ```bash
    git clone https://github.com/your-username/work-arrangement-clustering.git
2. Install dependencies:
   ```bash
    pip install -r requirements.txt
3. Run the Jupyter Notebook:
   ```bash
    jupyter notebook Work_Arrangement_Clustering.ipynb

