# starsCDS_IISc
Data Engineering Challenge (PS 2)

In this project, we structured the BBC article data by creating a CSV file named bbc_articles.csv with the columns article_id, text, and category. We accomplished this by looping through the files in the BBC_articles folder, extracting the relevant information from the filenames and file contents, and creating a DataFrame from the collected data.
For the data preprocessing and vectorization step, we followed these steps:

Tokenized the text data using NLTK's word_tokenize function.
Performed preprocessing steps such as:-
=> lowercasing removing stopwords, and punctuation, by defining a custom function preprocess_text.

Additionally we also defined 4 preprocessing functions to:-      ------- Novelty ---------
1)remove_accents: Removes accents from strings using the unicodedata module.
2)remove_html_tags: Removes HTML tags from strings using regular expressions.
3)expand_contractions: Expands contractions to their full forms using the contractions library.
4)remove_urls: Removes URLs from strings using regular expressions.

Vectorized the preprocessed text data using the TF-IDF technique from scikit-learn's TfidfVectorizer.
Created a new DataFrame vectorized_df by stacking the sparse matrix of features (X) horizontally with the target labels (y).
Saved the vectorized dataset to a CSV file named vectorized_dataset.csv.

For vectorization, we chose the TF-IDF technique as it is widely used and effective for text classification tasks. TF-IDF assigns higher weights to words that are more relevant and informative for a particular document, while downplaying the importance of common words that appear frequently across documents.
The vectorized dataset vectorized_dataset.csv contains numerical features derived from the TF-IDF vectorization, along with the corresponding category labels. This dataset can be directly used for training machine learning models for text classification tasks, such as classifying the BBC articles into their respective categories.
Please note that the code provided assumes the presence of the necessary libraries and packages, such as pandas, nltk, scikit-learn, and numpy. Make sure to install these dependencies before running the code.
