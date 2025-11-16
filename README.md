# NLP-Insurance-Claims-Topic-Modeling-BERTopic
Insurance Claims Topic Modeling with BERTopic
# Project Overview
This project uses advanced Natural Language Processing (NLP) techniques to automatically identify and categorize underlying topics within a dataset of insurance claim descriptions. 
By applying the state-of-the-art BERTopic framework, this project demonstrates an end-to-end unsupervised topic modeling pipeline, from text preprocessing to model interpretation and visualization.
The core objective is to move beyond manual, time-consuming methods of sorting claims, enabling faster processing, improved efficiency, and deeper insights into recurring claim types and trends.

# Key Insights
- Successfully identified 16 meaningful topics, providing a clear overview of the most common types of insurance claims without any pre-labeled data.
- Topic prevalence analysis revealed the most dominant claim types, such as "Rear-End Collisions" and "Water Damage," allowing a business to prioritize or investigate these areas further.
- The use of BERTopic, powered by transformer-based embeddings, produced highly coherent and semantically relevant topics, ensuring that the generated categories are both accurate and easy to interpret.
- The project provides a foundation for more advanced analytics, such as tracking topic trends over time or combining topic data with other claim metadata for deeper insights.
# Methodology 
The project follows a standard unsupervised NLP workflow and leverages the advanced clustering capabilities of BERTopic to automatically discover themes in insurance claim descriptions.
1. Data Loading & Preprocessing
Raw claim descriptions were imported from an Excel file.
Records with missing descriptions were removed to maintain data integrity.
All text was converted to string format for consistency.

2. Embedding Generation
Each claim description was transformed into a numerical vector (embedding) using the SentenceTransformer model all-MiniLM-L6-v2.
This model was chosen for its strong semantic performance and lightweight architecture.

3. Topic Modeling with BERTopic
BERTopic automatically applies several steps internally to generate coherent topics:
a. Dimensionality Reduction (UMAP – internal)
UMAP reduces the high-dimensional sentence embeddings, improving clustering quality and enabling visualization.
b. Clustering (HDBSCAN – internal)
HDBSCAN groups similar claims and flags outliers as noise (Topic -1) without requiring a preset number of clusters.
c. Topic Representation (c-TF-IDF – internal)
BERTopic uses c-TF-IDF to extract the most informative words for each topic, which were then used to assign human-readable topic labels.
# Results and Visualizations
