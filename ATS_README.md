
# ATS Resume Analyzer & Competition Portal

An AI-powered **ATS (Applicant Tracking System) Resume Analyzer** built using **Python, Streamlit, NLP, and Supabase**.  
The system evaluates resumes against job descriptions and provides an **ATS compatibility score**, helping candidates optimize their resumes.

This project was developed for the **Perfect CV Match 2025 competition hosted by Microsoft Learn Student Chapter (MLSC) at Thapar Institute of Engineering & Technology**.

---

## Features

• Upload resume in **PDF format**  
• Extract resume text using **PyMuPDF**  
• Analyze resume using **NLP (SpaCy)**  
• Calculate **ATS match score** against job description  
• Detect **skills from resume automatically**  
• Estimate **years of experience**  
• **Plagiarism detection** using TF-IDF similarity  
• **Keyword similarity scoring** between resume & JD  
• **Resume quality scoring system**  
• **Leaderboard system for competition participants**  
• **Participant registration with upload limits**  
• **Interactive analytics dashboard**

---

## Tech Stack

**Frontend**
- Streamlit
- Plotly

**Backend**
- Python
- NLP (SpaCy)
- Scikit-learn

**Database**
- Supabase (PostgreSQL)

**Data Processing**
- Pandas
- NumPy
- TF-IDF Vectorization

---

## Project Structure

ATS-Resume-Analyzer
│
├── app.py                # Streamlit frontend UI
├── backend.py            # ATS scoring engine and database functions
├── requirements.txt      # Python dependencies
├── supabase_schema.txt   # Database schema for participants & applications
├── mlsc.png              # Project logo
├── LICENSE
└── README.md

---

## ATS Scoring Algorithm

The ATS score is computed using multiple evaluation factors:

### 1. Skill Matching (40 points)
Detected resume skills are matched against the job description.

### 2. Experience Matching (20 points)
Extracted experience years are compared with JD requirements.

### 3. Project Verification (10 points)
Checks whether claimed skills appear in the projects section.

### 4. Education Validation
Education fields and CGPA consistency are validated.

### 5. Keyword Similarity
TF-IDF similarity between resume text and job description.

### 6. Resume Quality Score
Evaluates structure based on:
- Resume length
- Presence of sections
- Skill diversity
- Experience mentions

### 7. Plagiarism Detection
Compares resumes with previously uploaded resumes.

---

## Installation

### Clone Repository

git clone https://github.com/yourusername/ats-resume-analyzer.git
cd ats-resume-analyzer

### Install Dependencies

pip install -r requirements.txt

### Install NLP Model

python -m spacy download en_core_web_sm

### Configure Supabase

Create `.streamlit/secrets.toml` and add:

SUPABASE_URL=your_supabase_url
SUPABASE_KEY=your_supabase_key

### Run Application

streamlit run app.py

---

## Example ATS Score Output

ATS Score: 78%

Matched Skills:
Python, SQL, Machine Learning, Git

Experience:
2 Years

Keyword Similarity:
65%

Resume Quality Score:
8 / 10

---

## Future Improvements

- Transformer-based resume analysis
- Resume improvement suggestions
- GPT-based job description matching
- Resume formatting feedback
- Recruiter dashboard

---

## Author

Tanmay Bansal  
B.Tech Computer Science  
Thapar Institute of Engineering & Technology

---

## License

This project is licensed under the MIT License.
