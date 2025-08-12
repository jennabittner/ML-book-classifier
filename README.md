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

The dataset consists of Goodreads book reviews and associated genre labels, including genres such as fantasy, romance, mystery, and more.

## Explore Results

View the complete analysis and interactive visualizations on Kaggle:  
📄 **Notebook:** [View on Kaggle](https://www.kaggle.com/YOUR_NOTEBOOK_LINK)  
📂 **Dataset:** [Download dataset](https://drive.google.com/YOUR_DATASET_LINK)  

---

## Summary of Results

- The confusion matrix shows the model performs well overall, with highest values along the diagonal indicating correct classifications. However, notable misclassifications occur where genres overlap or share similar themes.

- The model’s ROC curve demonstrates strong discriminatory power with an AUC of 0.93, significantly outperforming random chance. This indicates a high true positive rate while maintaining a low false positive rate.

- Precision-recall analysis reveals the model balances precision and recall consistently across most genres. Genres like comics, graphic novels, romance, and non-fiction show strong performance with both high precision and recall, while smaller or more ambiguous genres such as poetry exhibit more variability and challenges.

- Overall accuracy is moderate at 51%, reflecting the complexity and overlap in genre classification. The model struggles most with smaller or overlapping genres like poetry and young adult.

- Initially, a CNN was tested but the Random Forest classifier outperformed it, likely due to the text-based nature of the data and the effectiveness of Random Forest in handling complex feature relationships.

- Future improvements could include more advanced models like BERT for semantic understanding, multilabel classification to handle books spanning multiple genres, and more extensive parameter optimization and data balancing techniques.


