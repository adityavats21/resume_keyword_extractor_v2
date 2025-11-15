#  Resume Keyword Extractor (AI Powered)

A full-stack AI application that extracts meaningful **keywords**, **TF-IDF scores**, and generates **Wordcloud**, **Bar Chart**, and **Radar Chart** visualizations from any uploaded resume.

This project uses **NLP + TF-IDF**, **Python (Flask)**, **React.js**, and **TailwindCSS**, and is fully deployable.

---

##  Features

###  AI/NLP Features
- Extracts clean text from PDF resumes  
- Cleans text using **NLP preprocessing**  
- Computes **TF-IDF scores** for keyword ranking  
- Generates:
  - Word Cloud  
  - Bar Chart (modern stylized)  
  - Radar Chart for keyword strength  

###  Full-Stack Features
- React.js modern UI with TailwindCSS + animations  
- Multi-page app with:
  - Home Page
  - Results Dashboard
  - About
  - Contact  
- Flask backend with CORS  
- Image generation using Matplotlib & WordCloud  
- Fully deployable

---

##  Tech Stack Used

### **Frontend**
- React.js (Create React App)
- React Router
- TailwindCSS
- Modern UI/UX with gradients, glassmorphism, and animations

### **Backend**
- Python
- Flask
- Flask-CORS
- scikit-learn (TF-IDF)
- NLTK
- PyPDF2
- Matplotlib
- WordCloud library

### **AI Working**
The intelligence comes from:
1. **TF-IDF (Term Frequency – Inverse Document Frequency)**  
   - Measures how important a word is in the resume  
   - Higher TF-IDF → more unique, meaningful keyword  
2. **NLP Cleaning**
   - Removes stopwords  
   - Normalizes text  
   - Tokenizes and processes words  
3. **Visualization Layer**
   - WordCloud shows prominence  
   - Bar Chart shows ranked score  
   - Radar Chart shows keyword strength distribution  

---

##  Project Structure
resume_keyword_extractor/
│── frontend/ # React UI
│── src/
│ ├── pdf_reader.py
│ ├── text_cleaner.py
│ ├── tfidf_extractor.py
│ ├── visualizer.py
│── main.py # Flask backend
│── uploaded.pdf
│── wordcloud.png
│── bar_chart.png
│── radar_chart.png
│── README.md


---

## Local Setup Instructions

###  1. Backend Setup (Flask)

```sh
cd resume_keyword_extractor
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python main.py
```
Backend runs at:

http://127.0.0.1:5000

 2. Frontend Setup (React)
cd frontend
npm install
npm start


Frontend runs at:

http://localhost:3000
 Deployment Guide
 Deploy Backend (Flask) — Render

Go to https://render.com

Click New Web Service

Connect your GitHub repository

Select your repo

Configure:

Build Command: pip install -r requirements.txt
Start Command: python main.py


Set Runtime to Python 3

Deploy

After deployment, Render gives you a backend URL like:

https://resume-ai-backend.onrender.com


 Replace your frontend fetch URL:

fetch("https://your-backend-url/extract")

 Deploy Frontend (React) — Vercel

Go to https://vercel.com

Import your GitHub repository

Select frontend folder (monorepo support)

Set:

Build Command: npm run build
Output Folder: build


Click Deploy

Frontend will deploy to:

https://resume-ai.vercel.app

 Environment Notes

Update backend URL in React before deploying:

const backendURL = "https://your-render-backend-url/extract";

 Author

Aditya Vats
Modern AI + Full-Stack Developer 🚀


