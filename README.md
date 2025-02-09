# Prototype-Extension-Philippine-Fake-News-Detection-SVM-v1
This is a Python-based Chrome extension designed to detect fake news by analyzing text content created for the purpose of the research thesis entitled "##Development and Prototype Implementation of a Browser Extension for Fake News Detection in Philippine News Using Natural Language Processing Algorithms##" in Computer Science Thesis 1 &amp; 2 subject in Bachelor of Computer Science in Camarines Sur Polytechnic Colleges. The extension uses machine learning models to determine the credibility of news articles.


## Features

### 1. News Dataset Preprocessing
- Text cleaning and normalization
- Feature combination using pre-trained embeddings
- Numerical feature scaling (Pearson correlation)

### 2. Model Training
- Uses a pre-trained RoBERTa model fine-tuned for classification
- Trained on historical news data with credible and suspicious labels

### 3. Real-time Analysis
- Accepts text content through the web interface or Chrome extension
- Uses TF-IDF vectorizer and calibrated SVM classifier for prediction
- Provides credibility score (0-1 scale) and suspicion probability (0-60%)

### 4. Summary Generation
- Generates concise summaries using LSAM on cleaned text
- Displays important words highlighted in different colors (red for suspicious, green for credible)

### 5. Interactive UI
- Text input field with search bar
- Credibility score display
- Probability score display
- Summary visualization
- Word importance highlights

## Dependencies
- Python 3.10.10
- numpy
- pandas
- torch
- transformers (for model loading)
- typing
- requests
- beautifulsoup4
- langford-summarizer
- lemmatize
- sumy
- word cloud
- matplotlib
- scikit-learn

## Setup Instructions

1. Clone the repository
```bash
git clone https://github.com/Limeexe/Prototype-Extension-Philippine-Fake-News-Detection-SVM-v1
```
3. Install dependencies using pip:
```bash
pip install numpy pandas torch transformers typing requests beautifulsoup4 lemmatize summarize-kycklin-summarizer matplotlib scikit-learn
```

## Usage

1. Visit the web interface at `http://localhost:5000`
2. Paste text content in the input field
3. Click "Analyze Content" to get credibility score and summary
4. Use the search bar to analyze different texts

## Model Evaluation
- Credibility scores between 0.8 and 1 indicate credible news
- Scores below 0.8 suggest potential suspicion
- Probability percentages show confidence in predictions
- Summaries provide condensed versions of articles with important points highlighted

## Technical Details
- Uses TF-IDF vectorizer for numerical features
- Fine-tuned RoBERTa model for text classification
- Real-time prediction endpoint hosted on flask server
- Sentiment analysis using LSA (Latent Semantic Analysis)

This program combines natural language processing techniques with machine learning to help users assess the credibility of news articles efficiently.
