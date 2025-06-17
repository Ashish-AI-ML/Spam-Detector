# 📧 SMS Spam Detector using NLP

This repository contains a Python-based **SMS Spam Detection** system. It uses classic **Natural Language Processing (NLP)** techniques and a **Naive Bayes classifier** to classify SMS messages as either **ham (not spam)** or **spam**.

---

## 📄 Project Description

This project demonstrates how to build a spam classifier using a traditional NLP pipeline. It processes and analyzes short SMS messages to determine whether they are spam or not. The dataset used comes from the [SMS Spam Collection Dataset](https://www.dt.fee.unicamp.br/~tiago/smsspamcollection/), which is widely used in text classification benchmarks.

Using text preprocessing, tokenization, lemmatization, stopword removal, and feature extraction, the model learns to identify common patterns in spam messages using the Naive Bayes algorithm.

---

## ⚙️ How It Works

1. **Load the Dataset**  
   The SMS data is read from a tab-separated text file (`SMSSpamCollection.txt`) into a pandas DataFrame.

2. **Preprocess the Text**  
   Each message is:
   - Lowercased
   - Tokenized into words
   - Cleansed of stopwords
   - Lemmatized (or stemmed)
   This ensures consistent word forms for better classification.

3. **Convert Messages to Features**  
   A list of the most common words is generated from the dataset. Each message is then transformed into a dictionary of features, showing which of these common words are present.

4. **Split the Dataset**  
   The dataset is split into training and test sets (e.g., 4000 training samples, rest for testing).

5. **Train the Naive Bayes Classifier**  
   A Naive Bayes classifier from the NLTK library is trained using the feature sets.

6. **Evaluate the Model**  
   The model's accuracy is evaluated on the test set. It also shows the most informative words for identifying spam.

---

## 🧠 Tech Stack

- Python
- Pandas
- NLTK (Natural Language Toolkit)

---

## 📊 Results

- The model performs well in distinguishing between spam and ham.
- Spam messages are often identified by specific keywords such as **free**, **win**, **call**, etc.

---

## 📁 Dataset

The dataset used is the **SMS Spam Collection**, a public dataset consisting of SMS messages labeled as either spam or ham.

- File: `SMSSpamCollection.txt`
- Format: Tab-separated (`\t`)
- Columns:
  - `label`: "spam" or "ham"
  - `message`: actual text message

---

## 🧪 Example

**Input:**  
`"Congratulations! You've won a $1000 Walmart gift card. Go to http://bit.ly/123456 to claim now."`  
**Prediction:** `Spam`

**Input:**  
`"Are we still meeting at 6 today?"`  
**Prediction:** `Ham`

---

## 📦 Installation

1. Clone the repository:

```bash
