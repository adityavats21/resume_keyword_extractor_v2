# Resume–JD Keyword Matcher 📄

An NLP-powered tool that extracts keywords from uploaded resumes using TF-IDF scoring and generates match analysis visualizations — built as a full-stack Flask + React application.

---

## What It Does

Upload a resume PDF → the system:
1. Extracts and cleans text using NLP preprocessing (tokenization, stopword removal)
2. Scores keywords using **TF-IDF** (Term Frequency–Inverse Document Frequency)
3. Generates three visualizations: **Word Cloud**, **Bar Chart** (ranked scores), **Radar Chart** (keyword strength distribution)
4. Serves results through a React dashboard with real-time rendering

---

## Tech Stack

| Layer | Tools |
|---|---|
| NLP / ML | scikit-learn (TF-IDF), NLTK, PyPDF2 |
| Visualization | Matplotlib, WordCloud |
| Backend | Python, Flask, Flask-CORS |
| Frontend | React.js, TailwindCSS, React Router |
| Deployment | Render (backend), Vercel (frontend) |

---

## How TF-IDF Works Here

**TF (Term Frequency)** — how often a word appears in the resume.
**IDF (Inverse Document Frequency)** — penalizes common words, rewards unique ones.

A high TF-IDF score = the word is both frequent *and* distinctive to this resume — which are your strongest keywords for a given JD.

```
TF-IDF(word) = TF(word) × log(N / df(word))
```

---

## Project Structure

```
resume_keyword_extractor_v2/
├── main.py                 # Flask entry point
├── requirements.txt
├── src/
│   ├── pdf_reader.py       # PDF text extraction
│   ├── text_cleaner.py     # NLP preprocessing
│   ├── tfidf_extractor.py  # TF-IDF scoring
│   └── visualizer.py       # Chart generation
└── frontend/               # React + Tailwind UI
    └── src/
        └── pages/          # Home, Results, About, Contact
```

---

## Local Setup

### Backend

```bash
python3 -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
python main.py
```

Runs at `http://127.0.0.1:5000`

### Frontend

```bash
cd frontend
npm install
npm start
```

Runs at `http://localhost:3000`

> Before deploying, update the backend URL in your React fetch calls to point to your Render deployment URL.

---

## Author

**Aditya Vats**
[GitHub](https://github.com/adityavats21) · [LinkedIn](https://linkedin.com/in/adityavats21)
