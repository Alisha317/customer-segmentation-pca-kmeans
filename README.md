**Customer Segmentation using PCA & K-Means Clustering**

**Overview**

This project applies unsupervised machine learning to segment customers into distinct behavioral groups using purchasing history, demographics, and campaign response data. Instead of relying on predefined labels, the model discovers natural groupings in the data using distance-based clustering.

**Objective**


Reduce a high-dimensional customer dataset (20+ features) into a compact set of principal components.
Identify the optimal number of customer segments mathematically (not by guesswork).
Translate abstract clusters into actionable, human-readable business personas.


**Dataset** 

Customer Personality Analysis (Kaggle)
🔗 https://www.kaggle.com/datasets/imakash3011/customer-personality-analysis

Contains ~2,240 customer records with demographic info, purchase history across product categories, campaign acceptance, and store/web engagement data.


**Note:** The raw dataset file is not included in this repo due to size/licensing — download it directly from the Kaggle link above and place it in the project folder as marketing_campaign.csv.



**Tech Stack**


**Python:** pandas, numpy
**Visualization:** matplotlib, seaborn
**Machine Learning:** scikit-learn (StandardScaler, PCA, KMeans, silhouette_score)


**Pipeline**

StageTechniquePurpose1. ScaleStandardScalerNormalize features to equal weight2. CompressPCAReduce 20+ features into principal components3. ClusterK-MeansGroup customers using distance metrics4. ValidateElbow Method + Silhouette ScoreMathematically confirm optimal K5. TranslateCluster ProfilingConvert clusters into business personas

**Key Results**


Identified [X] distinct customer segments based on income, spending, and engagement patterns.
Achieved a silhouette score of [insert your score], indicating well-separated clusters.
Translated clusters into personas such as High-Value Loyal Customers, Budget-Conscious Enthusiasts, and Low Engagement / At-Risk customers.


**Repository Structure**

├── project3_customer_segmentation.py   # Main analysis script
├── cluster_personas_labeled.csv        # Final persona summary
├── pca_variance.png                    # PCA explained variance chart
├── elbow_method.png                    # Optimal K - Elbow Method
├── silhouette_scores.png               # Optimal K - Silhouette Score
├── clusters_3d.png                     # 3D visualization of clusters
└── README.md

**How to Run**

bashpip install pandas numpy matplotlib seaborn scikit-learn
python project3_customer_segmentation.py

**Business Value**

Customer segmentation like this powers targeted marketing campaigns, personalized retention strategies, and more efficient allocation of marketing budgets — turning raw behavioral data into clear strategic action.
