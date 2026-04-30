# Fake News Detection System using NLP & Machine Learning

## Project Overview

This project implements a **Fake News Detection System** that classifies news articles as **Fake or Real** using Natural Language Processing (NLP) and Machine Learning techniques.

The system leverages the **FakeNewsNet dataset**, which combines news content and social context, making it suitable for real-world misinformation detection scenarios.

---

## Objectives

* Detect fake news based on textual content
* Apply NLP techniques for feature extraction
* Train and evaluate machine learning models
* Understand how misinformation spreads through data

---

## Dataset Description

The project uses a subset of the **FakeNewsNet dataset**, which includes:

* **Politifact** (political news)
* **GossipCop** (entertainment news)

Each dataset contains:

* News ID
* Title
* URL
* Label (Fake / Real)
* Associated tweet IDs (optional for social analysis)
 Note: Full dataset is not included due to privacy and copyright restrictions.

---

## Methodology

### 1. Data Collection

* News articles and metadata are collected from dataset files
* Optional: Twitter data can be collected using API keys

### 2. Data Preprocessing

* Lowercasing text
* Removing punctuation and stopwords
* Tokenization

### 3. Feature Engineering

* TF-IDF vectorization is used to convert text into numerical form

### 4. Model Training

* Machine learning models such as:

  * Logistic Regression
  * Naive Bayes

### 5. Evaluation

* Accuracy
* Precision
* Recall
* F1-score

---

## Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* NLTK
* Matplotlib (for visualization)

---

## Project Structure

```id="n6o2zy"
Fake-news-Detection-System/
│── README.md
│── requirements.txt
│── config.json
│
├── code/
│   ├── main.py
│   ├── news_content_collection.py
│   ├── tweet_collection.py
│   ├── retweet_collection.py
│   ├── user_profile_collection.py
│
├── dataset/
│   ├── politifact_fake.csv
│   ├── politifact_real.csv
│   ├── gossipcop_fake.csv
│   ├── gossipcop_real.csv
```

---

## Installation & Setup

### 1. Clone the repository

```bash id="nhs7g4"
git clone https://github.com/your-username/fake-news-detection-ml.git
cd fake-news-detection-ml
```

### 2. Install dependencies

```bash id="q2j5mv"
pip install -r requirements.txt
```

### 3. (Optional) Configure Twitter API

* Add API keys in `tweet_keys_file.json`
* Update settings in `config.json`

---

## Running the Project

### Step 1: Start key server (for Twitter API handling)

```bash id="nxk0eo"
cd code
python -m resource_server.app
```

### Step 2: Run data collection / model pipeline

```bash id="0hsx9v"
python main.py
```

---

## Results (Example)

| Model               | Accuracy | F1 Score |
| ------------------- | -------- | -------- |
| Logistic Regression | 91%      | 0.90     |
| Naive Bayes         | 88%      | 0.87     |

---

## Key Highlights

* End-to-end ML pipeline (data → preprocessing → model → prediction)
* Integration of **content + social context data**
* Scalable data collection using multiprocessing
* Modular code structure

---

## Future Enhancements

* Deploy using Flask / FastAPI
* Implement Deep Learning models (LSTM, BERT)
* Build a web-based UI for real-time detection
* Improve accuracy using ensemble models

---

## References

* FakeNewsNet Dataset
* Research papers on fake news detection
