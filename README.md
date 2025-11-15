ResumeAI – AI Resume Keyword Extractor (TF-IDF + WordCloud + Charts)

 An AI-powered resume analysis tool that extracts keyword insights and generates visual analytics.

 Overview

ResumeAI is a full-stack AI project that analyzes a resume PDF using Natural Language Processing (NLP) and generates:

 Top TF-IDF keywords

 Modern Word Cloud

 Enhanced Bar Chart

 Radar Chart for Keyword Strength

 Modern React Frontend (TailwindCSS, Animations)

 Python Flask Backend with NLP + TF-IDF

This tool helps students & professionals understand how well their resume highlights important skills.

 How the AI Works (Simple Explanation)

The AI logic is implemented in Python (Flask) using NLP techniques:

1️ PDF Text Extraction

Using PyPDF2, the text is extracted from the uploaded PDF.

️ Text Cleaning

Converting to lowercase

Removing punctuation

Removing stopwords (the, is, and)

Tokenizing

Lemmatization (root forms)

 TF-IDF Calculation (Core AI Part)

We use TfidfVectorizer from scikit-learn:

TF = how frequently a word appears

IDF = how unique/important a word is

TF-IDF = TF × IDF → importance score

 The AI selects top 10 most important keywords from the resume.

 Modern Data Visualizations

Word Cloud generated using WordCloud

Bar chart generated using matplotlib

Radar Chart giving visual strength distribution

These visuals are automatically saved & returned to frontend.

 Tech Stack
 Frontend (React + TailwindCSS)

React.js

React Router

Tailwind CSS

Advanced UI with blur, glassmorphism, animations

 Backend (Flask + Python NLP)

Flask REST API

PDF text extraction (PyPDF2)

NLP cleaning (NLTK)

TF-IDF keyword ranking (scikit-learn)

WordCloud + Matplotlib visualizations

 AI / ML

NLP preprocessing

TF-IDF vectorizer

Keyword importance scoring

Visualization analytics

 Project Structure
resume_keyword_extractor/
│
├── frontend/                    # React app
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── context/
│   │   ├── App.jsx
│   │   └── index.js
│   └── package.json
│
├── src/                        # Backend source
│   ├── pdf_reader.py
│   ├── text_cleaner.py
│   ├── tfidf_extractor.py
│   └── visualizer.py
│
├── venv/                       # Python virtual environment
├── main.py                     # Flask backend
├── requirements.txt
└── README.md

 How to Run the Project
 Backend Setup
cd resume_keyword_extractor
source venv/bin/activate
pip install -r requirements.txt
python main.py


Backend runs on:

http://127.0.0.1:5000

 Frontend Setup
cd frontend
npm install
npm start


Frontend runs on:

http://localhost:3000

 Features Preview
 Keyword Extraction

Shows top keywords with TF-IDF score.

 Modern Word Cloud

Visual distribution of important skills and terms.

 Bar Chart

Enhanced gradient-style bar chart for keyword importance.

 Radar Chart

Unique modern visualization to compare keyword strength.

 Clean Dashboard UI

Glassmorphism, animations, and modern layout.

 Why This Project is Useful?

Helps improve resume keyword density

Shows skill representation clearly

Useful for ATS optimization

Great portfolio project for ML + Web Dev

Includes both AI + Full-Stack exposure

 Deployment Options

Backend → Render / Railway

Frontend → Vercel / Netlify

Assets → Served directly from Flask

 License

MIT License — Free to use, modify, and distribute.

 Author

Aditya Vats
B.Tech CSE | AI & Web Developer
GitHub: adityavats21
