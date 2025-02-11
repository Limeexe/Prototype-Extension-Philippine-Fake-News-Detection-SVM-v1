# Prototype-Extension-Philippine-Fake-News-Detection-SVM-v1
This is a Python-based Chrome extension designed to detect fake news by analyzing text content created for the purpose of the research thesis entitled "**Development and Prototype Implementation of a Browser Extension for Fake News Detection in Philippine News Using Natural Language Processing Algorithms**" in Computer Science Thesis 1 &amp; 2 subject in Bachelor of Computer Science in Camarines Sur Polytechnic Colleges. The extension uses machine learning models to determine the credibility of news articles.


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
- nltk
- joblib
- flask

## Setup Instructions

1. Clone the repository
```bash
git clone https://github.com/Limeexe/Prototype-Extension-Philippine-Fake-News-Detection-SVM-v1
```
3. Install dependencies
- using pip:
```bash
pip install -r requirements.txt
```

## Usage

1. The extension's backend is hosted on `[localhost:5000](http://localhost:5000)`. It includes:
- Flask server with CORS enabled
- Pre-trained SVM model for fake news detection
- Joblib model loading mechanism  
2. Paste text content in the input field
3. Click "Analyze Content" or just let it be to get credibility score and summary

## Technical Details
- Text preprocessing using TF-IDF vectorizer
- Machine learning model (SVM) for fake news detection
- Cross-browser compatibility

## Known Issues
- Initial model training and deployment may require additional optimization for performance.
- Limited testing has been conducted on edge cases; further validation is recommended.

## Contributors
The project was developed by Team LiveANet.
