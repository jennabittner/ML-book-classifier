# Goodreads Genre Classification

This project explores using machine learning to classify Goodreads book reviews into genres to enhance recommendation systems.  
It includes comprehensive data preprocessing, feature extraction with TF-IDF, sentiment analysis, and classification using a Random Forest model trained on balanced data via SMOTE.

## Project Overview

- Data loading and filtering of Goodreads reviews and book genres.  
- Text preprocessing: tokenization, stopword removal, lemmatization.  
- Feature engineering: TF-IDF vectorization and sentiment scoring.  
- Model training: Random Forest classifier to predict primary genres.  
- Evaluation: Accuracy, classification report, confusion matrix, ROC curve visualization.

## Dataset

The dataset used is publicly available from [Goodreads Data from Mengting Wan]([https://www.kaggle.com/datasets/jealousleopard/goodreadsbooks](https://cseweb.ucsd.edu/~jmcauley/datasets/goodreads.html)).  

**Specifically, this project uses these two files:**  
- `goodreads_reviews_dedup.json.gz`  
- `goodreads_book_genres_initial.json.gz`  

These files are used for review texts and genre labels, respectively.

## Explore Results

You can view a **static HTML version of the notebook** here (note: this is not executable):  
📄 [Notebook (HTML)](file:///C:/Users/jenna/Downloads/BigData_Final_Code%20(1).html) 

---

## Summary of Results

- The confusion matrix shows the model performs well overall, with highest values along the diagonal indicating correct classifications. However, notable misclassifications occur where genres overlap or share similar themes.

- The model’s ROC curve demonstrates strong discriminatory power with an AUC of 0.93, significantly outperforming random chance. This indicates a high true positive rate while maintaining a low false positive rate.

- Precision-recall analysis reveals the model balances precision and recall consistently across most genres. Genres like comics, graphic novels, romance, and non-fiction show strong performance with both high precision and recall, while smaller or more ambiguous genres such as poetry exhibit more variability and challenges.

- Overall accuracy is moderate at 51%, reflecting the complexity and overlap in genre classification. The model struggles most with smaller or overlapping genres like poetry and young adult.

- Initially, a CNN was tested but the Random Forest classifier outperformed it, likely due to the text-based nature of the data and the effectiveness of Random Forest in handling complex feature relationships.

- Future improvements could include more advanced models like BERT for semantic understanding, multilabel classification to handle books spanning multiple genres, and more extensive parameter optimization and data balancing techniques.


