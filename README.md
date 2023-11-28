1. Data Loading and Exploration


The project begins by importing necessary libraries and loading the financial tweets datasets (Financial_train_data.csv and Financial_valid_data.csv).
The label_mapping dictionary is defined to map numerical labels to their corresponding categories.
A function basic_info is created to provide basic information about the datasets, such as info, head, and descriptive statistics.
The distribution of labels in the training and validation datasets is visualized using seaborn countplots.




2. Text Preprocessing


NLTK is used for text preprocessing, including tokenization, lemmatization, and removal of stopwords.
The preprocess_text function is defined to apply these preprocessing steps to the 'text' column of the datasets.
The processed text is added to new columns ('processed_text') in both training and validation datasets.




3. TF-IDF Vectorization


A TF-IDF vectorizer is employed to convert the processed text into numerical features.
The script initially creates a TF-IDF vectorizer without setting max_features to explore the most frequent terms.
It then adjusts the vectorizer's parameters, including max_df, min_df, and max_features, and applies it to both training and validation datasets.




4. Word Cloud Visualization


Word clouds are generated for each label in the training dataset, providing a visual representation of the most frequent words associated with each category.




5. Model Training and Evaluation


The dataset is split into training and validation sets using train_test_split.
A Random Forest Classifier is trained on the training set and evaluated on the validation set.
Classification report and accuracy score are printed to assess the model's performance.
