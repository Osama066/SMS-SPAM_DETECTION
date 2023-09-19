
# Spam Detection using Streamlit

This is a simple Spam Detection application built with Streamlit, which allows you to classify text messages or emails as either spam or not spam. The application uses a pre-trained machine learning model to make predictions.

## Setup

To run this application, you'll need to have Python installed on your machine. You can install the required libraries using `pip`:


pip install streamlit nltk scikit-learn


You'll also need to download the NLTK data for tokenization and stopwords. If you haven't already, execute the following commands:

```python
import nltk
nltk.download('punkt')
nltk.download('stopwords')
```

## How to Use

1. Clone this repository to your local machine.

2. Make sure you have the trained model and vectorizer files (`model.pkl` and `vectorizer.pkl`) in the same directory as this script. These files should contain a pre-trained machine learning model and a TF-IDF vectorizer.

3. Run the application by executing the following command in your terminal:


streamlit run spam_detection.py


4. Once the application is running, you will see a web interface.

5. Enter the text message or email you want to classify in the provided text area.

6. Click the "Predict" button to get the classification result.

## How It Works

1. **Text Preprocessing**: The input text is preprocessed to prepare it for classification. The preprocessing includes:
   - Converting the text to lowercase.
   - Tokenizing the text into words.
   - Removing non-alphanumeric characters.
   - Removing stopwords (common words like "the," "and," etc.).
   - Applying stemming using the Porter Stemmer.

2. **Vectorization**: The preprocessed text is transformed into a TF-IDF vector using the vectorizer loaded from `vectorizer.pkl`.

3. **Prediction**: The TF-IDF vector is fed into the pre-trained machine learning model loaded from `model.pkl`, and a prediction is made.

4. **Display**: The application displays whether the input text is classified as "Spam" or "Not Spam" based on the prediction.
