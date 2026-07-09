# Sentiment Analysis Pipeline

This project builds a sentiment analysis workflow for IMDb movie reviews, from data collection to model evaluation.

## 1. Data Collection
- The workflow starts with [scraper.ipynb](scraper.ipynb), which is used to gather IMDb review pages.
- Review pages are stored in [imdb_pages](imdb_pages) as HTML files.
- The scraper extracts review metadata such as title, content, and rating from each page.

## 2. Dataset Preparation
- Extracted reviews are consolidated into [dataset/movie_reviews.csv](dataset/movie_reviews.csv).
- The dataset is then prepared for training by cleaning the text and transforming it into model-ready features.
- Labels are derived from review ratings to represent positive or negative sentiment.

## 3. Feature Engineering
- Text data is converted into numerical representations for classification.
- Two common approaches are used in this project:
  - TF-IDF for traditional machine learning models
  - Word embeddings for deep learning models

## 4. Model Training
The project experiments with three modeling approaches:

1. Random Forest
   - Uses TF-IDF features
   - Trained with a 70/30 split
   - Output: classification report, confusion matrix, and learning curve

2. Support Vector Machine (SVM)
   - Uses TF-IDF features
   - Trained with an 80/20 split
   - Output: classification report, confusion matrix, and learning curve

3. Deep Learning (LSTM)
   - Uses Word2Vec-based representations
   - Trained with a 70/30 split
   - Output: confusion matrix, accuracy/loss curves, and best-epoch selection

## 5. Evaluation and Comparison
- Each model is evaluated on test data using classification metrics.
- Results are compared to determine which approach performs best for this dataset.
- The trained experiments are organized in the [models](models) directory.

## 6. Output
- Final outputs include the prepared dataset, trained models, and evaluation results.
- The repository structure supports repeatable experimentation and future model improvements.
