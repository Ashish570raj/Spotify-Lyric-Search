
# 🎵 Spotify Lyric Search

A **lyric-based song identification system** that predicts the **Song Title** and **Artist** from a small snippet of lyrics using **Natural Language Processing (NLP)** and **text similarity techniques**.

---

## 📌 Project Overview

Given a short piece of song lyrics as input, the system:

* Processes and cleans the text
* Converts lyrics into numerical representations
* Computes similarity between the input lyrics and a large song database
* Returns the **most relevant song matches**

The model is designed as a **retrieval-based system**, not a classification model.

---

## 📂 Project Structure

```
Spotify-Lyric-Search/
│
├── data/
│   └── spotify_lyrics.csv   (not included in repo)
│
├── lyric_search.ipynb       # Main notebook (model + evaluation)
├── requirements.txt
└── README.md
```

---

## 📊 Dataset

* **Dataset:** Spotify Songs Lyrics Dataset
* **Size:** ~57,000 songs
* **Columns Used:**

  * `artist` – Artist name
  * `song` – Song title
  * `text` – Lyrics

---

## 🧠 Approach & Methodology

### 🔹 1. Text Preprocessing

The lyrics are cleaned using:

* Lowercasing
* Removal of punctuation and numbers
* Stopword removal

This reduces noise and improves similarity matching.

---

### 🔹 2. Feature Extraction

* **TF-IDF (Term Frequency–Inverse Document Frequency)** is used to convert lyrics into numerical vectors.
* Unigrams and bigrams are considered to capture important word phrases.

---

### 🔹 3. Similarity Measurement

* **Cosine Similarity** is applied to measure closeness between lyric vectors.
* Songs are ranked based on similarity scores.

---

### 🔹 4. Prediction

Given an input lyric snippet, the system retrieves the **Top-K most similar songs**, along with their artists and similarity scores.

---

## 🧪 Model Evaluation

Since this is a **retrieval-based system**, evaluation is done using **Top-K Accuracy**.

### 📈 Results

| Metric         | Accuracy |
| -------------- | -------- |
| Top-1 Accuracy | **73%**  |
| Top-3 Accuracy | **79%**  |
| Top-5 Accuracy | **82%**  |

These results indicate strong performance for lyric-based song retrieval using a TF-IDF similarity model.

---

## 📦 Installation & Setup

### 1️⃣ Clone the repository

```bash
git clone https://github.com/Ashish570raj/Spotify-Lyric-Search.git
cd Spotify-Lyric-Search
```

### 2️⃣ Install dependencies

```bash
pip install -r requirements.txt
```

### 3️⃣ Add dataset

Place the downloaded dataset file inside:

```
data/
```

### 4️⃣ Run the notebook

Open and run:

```bash
lyric_search.ipynb
```

---

## 🛠 Technologies Used

* Python
* Pandas, NumPy
* Scikit-learn
* NLTK
* Matplotlib & WordCloud (optional visualization)

---

## 🚀 Future Improvements

* Use semantic embeddings (e.g., Sentence-BERT) for better meaning capture
* Add multilingual lyric support
* Build a Streamlit web interface
* Optimize search using vector databases (FAISS)

---

## 👤 Author

**Ashish Raj**
B.Tech CSE (Data Science)

