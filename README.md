# 🎬 Movie Recommender System (ML Project)

A machine learning-based movie recommendation system that suggests similar movies using **TF-IDF similarity** and **genre-based filtering**, powered by the **TMDB API** for real-time movie data.

---

## 🚀 Features

* 🔍 Search movies by keyword
* 🎯 Smart suggestions using TMDB search
* 🤖 Content-based recommendations (TF-IDF)
* 🎭 Genre-based recommendations
* 📄 Movie details (poster, overview, release date, genres)
* 🏠 Browse trending and popular movies

---

## 🧠 Machine Learning Approach

This project uses a **Content-Based Filtering** technique:

* **TF-IDF Vectorization** on movie metadata
* **Cosine Similarity** to find similar movies
* Precomputed similarity using:

  * `tfidf_matrix.pkl`
  * `indices.pkl`

---

## 🛠️ Tech Stack

* **Python**
* **Pandas / NumPy**
* **Scikit-learn (TF-IDF)**
* **FastAPI** (serves ML model)
* **Streamlit** (UI for interaction)
* **TMDB API** (movie data & posters)

---

## 📁 Project Structure

```id="projtree01"
movie-recommender/
│
├── app.py                # Streamlit UI
├── main.py               # FastAPI (ML + API layer)
├── requirements.txt
├── .env                  # API key (not included)
├── .gitignore
│
├── df.pkl
├── tfidf_matrix.pkl
├── indices.pkl
```

---

## ⚙️ Setup Instructions

### 1️⃣ Clone the repository

```bash id="clone01"
git clone https://github.com/your-username/movie-recommender.git
cd movie-recommender
```

---

### 2️⃣ Create virtual environment

```bash id="venv01"
python -m venv venv
source venv/bin/activate   # Mac/Linux
venv\Scripts\activate      # Windows
```

---

### 3️⃣ Install dependencies

```bash id="install01"
pip install -r requirements.txt
```

---

### 4️⃣ Setup environment variables

Create a `.env` file:

```id="env01"
TMDB_API_KEY=your_tmdb_api_key_here
```

---

### 5️⃣ Run the backend (ML API)

```bash id="runbackend01"
uvicorn main:app --reload
```

---

### 6️⃣ Run the frontend (UI)

```bash id="runfrontend01"
streamlit run app.py
```

---

## 📊 Dataset

* The dataset is not included due to size constraints.
* Required processed files:

  * `df.pkl`
  * `tfidf_matrix.pkl`
  * `indices.pkl`

👉 These are generated during preprocessing.

---

## 🔍 How It Works

1. User searches for a movie
2. TMDB API fetches matching movies
3. Selected movie → passed to ML model
4. TF-IDF similarity finds closest matches
5. Results displayed with posters + details

---

## ⚠️ Important Notes

* Do NOT upload:

  * `.env`
  * `.pkl`
  * large dataset files
* Keep your API key secure

---


