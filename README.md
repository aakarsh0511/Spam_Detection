# Spam Detection using Word2Vec and Random Forest

## 📌 Project Overview

This project implements a text classification pipeline to detect spam messages using Natural Language Processing (NLP).
The workflow includes text preprocessing, training Word2Vec embeddings from scratch, converting text into numerical features, and applying a machine learning classifier for prediction.

The goal of the project is to understand how raw text data can be transformed into vector representations and used in supervised learning models.

---

## ⚙️ Methodology

### 1️⃣ Data Loading

* Loaded SMS dataset using **Pandas**
* Dataset contains message text and corresponding labels (spam/ham)

### 2️⃣ Text Preprocessing

* Removed non-alphabet characters using Regex
* Converted text to lowercase
* Tokenized words
* Applied **lemmatization** using NLTK WordNetLemmatizer
* Reconstructed cleaned corpus

---

### 3️⃣ Tokenization

* Converted cleaned text into token lists using:

  * `gensim.simple_preprocess`

---

### 4️⃣ Word Embedding (Word2Vec)

* Trained a Word2Vec model **from scratch** using Gensim
* Each word mapped to dense vector representation
* For each message:

  * Calculated average of word vectors
  * Generated fixed-length numeric feature vector

This step converts text → machine learning compatible features.

---

### 5️⃣ Feature Construction

* Built feature matrix from averaged vectors
* Encoded labels into binary values
* Combined features into Pandas DataFrame
* Handled missing values and alignment issues

---

### 6️⃣ Model Training

* Split data into training and testing sets
* Trained **Random Forest Classifier**
* Converted column names and labels into appropriate formats
* Fit model on training data

---

### 7️⃣ Evaluation

* Generated predictions on test data
* Evaluated using:

  * Accuracy Score
  * Classification Report

---

## 🧰 Technologies Used

* Python
* Pandas
* NumPy
* NLTK
* Gensim
* Scikit-learn
* tqdm

---

## 🚀 Key Learnings

* NLP preprocessing pipeline construction
* Training custom Word2Vec embeddings
* Converting variable-length text into fixed numeric vectors
* Handling real-world data alignment issues
* Applying ensemble models for classification
* Model evaluation and debugging

---

## 📈 Future Improvements

* Hyperparameter tuning
* Using TF-IDF or BERT embeddings
* Cross-validation
* Model comparison (SVM, XGBoost, etc.)
* Deployment as API or Web App

---

## 🏁 Conclusion

This project demonstrates an end-to-end pipeline for spam detection using classical NLP and machine learning techniques, providing hands-on understanding of embedding-based feature engineering and model building.
# Spam_Detection
