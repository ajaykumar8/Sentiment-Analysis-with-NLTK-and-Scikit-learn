# **Sentiment Analysis with NLTK and Scikit-learn**

This project performs sentiment analysis on text data using Python, NLTK, and Scikit-learn. The goal is to build a machine learning model that can classify a piece of text as having a positive or negative sentiment.

The entire process, from data cleaning to model training and evaluation, is contained in the Sentiment Analysis.ipynb Jupyter Notebook.

## **Project Files**

* **Sentiment Analysis.ipynb**: The main Jupyter Notebook containing all the Python code. This includes:  
  * Data loading and exploration.  
  * Text preprocessing (cleaning, tokenization, stopword removal).  
  * Feature extraction using TF-IDF.  
  * Model training (using Logistic Regression).  
  * Model evaluation.  
* **train.csv**: The dataset used to train the sentiment analysis model.  
* **test.csv**: A separate dataset used for testing the model's performance on unseen data.

## **Methodology**

1. **Data Loading**: The train.csv and test.csv files are loaded into Pandas DataFrames.  
2. **Text Preprocessing**: The text data is cleaned to make it suitable for a machine learning model. This process involves:  
   * Removing punctuation and special characters.  
   * Converting text to lowercase.  
   * Removing common "stopwords" (e.g., "the", "is", "a") using the **NLTK** library.  
   * (Optional) Applying stemming or lemmatization to reduce words to their root form.  
3. **Feature Extraction**: Machine learning models cannot understand raw text. We convert the cleaned text into numerical features using a **TF-IDF Vectorizer** (TfidfVectorizer from Scikit-learn).  
4. **Model Training**: A **Logistic Regression** model is trained on the TF-IDF features and the corresponding sentiment labels from the train.csv file.  
5. **Model Evaluation**: The trained model is evaluated using the test.csv data to see how accurately it can predict sentiment on new, unseen text.

## **Libraries Used**

This project relies on the following core Python libraries:

* **Pandas**: For data manipulation and loading CSVs.  
* **NLTK (Natural Language Toolkit)**: For text preprocessing tasks like stopword removal.  
* **Scikit-learn (sklearn)**: For:  
  * TfidfVectorizer (feature extraction)  
  * train\_test\_split (splitting data)  
  * LogisticRegression (the ML model)  
  * accuracy\_score (evaluation)  
* **Jupyter Notebook**: For interactive development and visualization.

## **How to Run**

1. **Clone the repository:**  
   git clone \[https://github.com/ajaykumar8/Sentiment-Analysis.git\](https://github.com/ajaykumar8/Sentiment-Analysis.git)  
   cd Sentiment-Analysis

2. **Install the required libraries:**  
   pip install pandas nltk scikit-learn jupyter

3. Download NLTK data (if first time):  
   Run Python in your terminal and execute the following commands:  
   import nltk  
   nltk.download('stopwords')  
   nltk.download('punkt')

4. **Launch Jupyter Notebook:**  
   jupyter notebook

5. Run the notebook:  
   Open Sentiment Analysis.ipynb in your browser and run the cells sequentially.