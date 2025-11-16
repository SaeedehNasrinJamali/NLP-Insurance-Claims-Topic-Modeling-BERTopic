# NLP-Insurance-Claims-Topic-Modeling-BERTopic
Insurance Claims Topic Modeling with BERTopic
# Project Overview
This project uses advanced Natural Language Processing (NLP) techniques to automatically identify and categorize underlying topics within a dataset of insurance claim descriptions. 
By applying the state-of-the-art BERTopic framework, this project demonstrates an end-to-end unsupervised topic modeling pipeline, from text preprocessing to model interpretation and visualization.
The core objective is to move beyond manual, time-consuming methods of sorting claims, enabling faster processing, improved efficiency, and deeper insights into recurring claim types and trends.

# Key Insights
- Successfully identified 16 meaningful topics, providing a clear and structured overview of the most common types of insurance claims—without requiring any pre-labeled data.
- Clear claim themes emerged, such as Rear-End Collisions, Slip & Fall, Water Damage, Windshield Damage, and Food Poisoning.
  The noise cluster (Topic -1) captured ambiguous or mixed claims that did not strongly align with any specific topic.
- The use of transformer-based SentenceTransformer embeddings significantly improved topic coherence and semantic similarity, resulting in cleaner and more interpretable clusters.
- BERTopic’s combination of UMAP + HDBSCAN + c-TF-IDF enabled strong clustering performance and transparent topic descriptions, making the generated categories intuitive and easy to interpret.
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
- Topic Frequency Bar Chart
   Shows which claim types occur most often.
- Average Topic Probability Chart
   Shows the model’s confidence in each discovered topic.
-  CSV Outputs
-  claims_with_topics.csv — each claim with assigned topic
-  topic_summary.csv — aggregated topic stats

