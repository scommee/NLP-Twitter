# Twitter Sentiment Analysis and Visualization

## Objectives

The primary objective of this project is to analyze Twitter data and categorize reviews based on sentiment analysis. This involves several key steps:

1. **Data Ingestion**: Read Twitter data from a CSV file.
2. **Preprocessing**: Clean and preprocess the text data.
3. **Word Embedding**: Convert words into vector spaces using a pre-trained Word2Vec model.
4. **Document Embedding**: Calculate the average vector for each review to represent the entire review in the vector space.
5. **Sentiment Classification**: Categorize each review as positive or negative based on its vector representation.
6. **Visualization**: Plot the reviews in a 2D space using dimensionality reduction techniques to visually demonstrate the categorization.

## Steps to Achieve Objectives

### 1. Data Ingestion
- Read Twitter data from a CSV file into a DataFrame.

### 2. Preprocessing
- Tokenize the text data.
- Remove stop words, punctuation, and other noise.
- Perform stemming or lemmatization if necessary.

### 3. Word Embedding
- Load a pre-trained Word2Vec model.
- Convert each word in the tweets to its corresponding vector using the model.

### 4. Document Embedding
- Calculate the average vector for each tweet by averaging the vectors of the words in the tweet.
- Handle cases where tweets contain no valid tokens by assigning a zero vector.

### 5. Sentiment Classification
- Train a classifier (e.g., Logistic Regression, SVM) using the document vectors and their corresponding sentiment labels.
- Predict the sentiment of new tweets based on their document vectors.

### 6. Visualization
- Use PCA to reduce the dimensionality of the document vectors to 2D.
- Plot the reduced vectors in a 2D space.
- Color-code the points based on their sentiment (positive/negative).

## Implementation

### Prerequisites

- Python 3.x
- Pandas
- Numpy
- Gensim
- Scikit-learn
- Matplotlib

### Instructions

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/your-username/twitter-sentiment-analysis.git
    cd twitter-sentiment-analysis
    ```

2. **Install Dependencies**:
    ```bash
    pip install pandas numpy gensim scikit-learn matplotlib
    ```

3. **Run the Script**:
    - Ensure your Twitter data CSV file is in the correct format and placed in the project directory.
    - Modify the script to point to your CSV file.
    - Run the script to perform sentiment analysis and generate the plot.
