# 🤖 AI Recruitment Platform using n8n

An intelligent recruitment automation platform built using **n8n**, **Large Language Models (LLMs)**, **LlamaParse**, **Google Workspace**, and **Google Gemini** to streamline candidate screening and evaluation.

This project automates the entire resume screening pipeline—from receiving candidate resumes to extracting structured information, evaluating candidates using AI, assigning scores, and updating the recruitment database—reducing manual effort and improving hiring efficiency.

---

# 📌 Project Overview

Recruiters often spend significant time manually reviewing resumes, extracting candidate information, and comparing applicants against job requirements.

This project automates that workflow using AI agents and workflow automation.

The platform:

- Reads candidate information from Google Sheets
- Downloads resumes from Google Drive
- Extracts resume text using LlamaParse
- Uses an LLM to analyze resumes
- Calculates candidate scores
- Generates hiring recommendations
- Updates Google Sheets automatically

---

# 🚀 Features

- 📄 Automatic Resume Parsing
- 🤖 AI-powered Candidate Evaluation
- 🎯 Candidate Scoring System
- ⭐ Skill Matching
- 📊 Experience Analysis
- 📚 Education Extraction
- 💼 Job Recommendation
- 📈 Automatic Ranking
- 🔄 End-to-End Workflow Automation
- ☁️ Google Workspace Integration
- 📝 Structured JSON Output
- ⚡ No Manual Resume Screening Required

---

# 🛠 Tech Stack

## Workflow Automation

- n8n

## AI

- Google Gemini
- LlamaParse

## Data Storage

- Google Sheets

## File Storage

- Google Drive

## Programming

- JavaScript (Code Node)

---

# 🏗 Workflow Architecture

```
Google Sheets Trigger
        │
        ▼
Download Resume from Google Drive
        │
        ▼
LlamaParse
(Parse PDF Resume)
        │
        ▼
Google Gemini
(Resume Analysis)
        │
        ▼
JavaScript Code Node
(Candidate Scoring)
        │
        ▼
Update Google Sheets
(Store Results)
```

# 🔄 Workflow Steps

## Step 1 — Google Sheets Trigger

The workflow continuously monitors a Google Sheet for new candidate entries.

Each row contains:

- Candidate Name
- Email
- Resume Link
- Job Role

---

## Step 2 — Download Resume

The resume is automatically downloaded from Google Drive using the provided file link.

Supported formats:

- PDF
- DOCX (if converted)

---

## Step 3 — Resume Parsing

The downloaded resume is sent to **LlamaParse**, which extracts clean, structured text while preserving formatting.

Extracted content includes:

- Personal Information
- Education
- Skills
- Work Experience
- Projects
- Certifications

---

## Step 4 — AI Resume Evaluation

The parsed resume is passed to **Google Gemini**, which evaluates the candidate based on:

- Technical Skills
- Relevant Experience
- Education
- Certifications
- Projects
- Communication Indicators
- Overall Fit for the Job Role

The model returns structured JSON containing all extracted information.

---

## Step 5 — Candidate Scoring

A JavaScript Code node processes the AI output and computes:

- Overall Score
- Skill Match Percentage
- Experience Score
- Education Score
- Hiring Recommendation

Example:

```
Overall Score: 89

Recommendation:
Highly Recommended

Skills:
Python
Machine Learning
React
SQL
Docker
```

---

## Step 6 — Update Google Sheets

The workflow writes the processed results back into Google Sheets.

Columns updated include:

- Skills
- Experience
- Education
- AI Score
- Recommendation
- Strengths
- Weaknesses

---

# 📊 AI Evaluation Criteria

Candidates are evaluated on:

- Technical Skills
- Relevant Projects
- Programming Languages
- Internship Experience
- Education
- Certifications
- Leadership
- Communication
- Overall Resume Quality

---

# 📸 Screenshots

## Workflow

_Add workflow screenshot here_

---

## Google Sheet

_Add Google Sheet screenshot here_

---

## Resume Parsing

_Add LlamaParse output screenshot here_

---

## Final Candidate Evaluation

_Add AI output screenshot here_

---

# 💡 Future Enhancements

- Multi-job role support
- ATS compatibility score
- Candidate shortlisting dashboard
- Email interview invitations
- Recruiter dashboard
- Candidate comparison
- AI interview question generation
- PDF evaluation report generation
- Integration with LinkedIn Jobs
- HR Analytics Dashboard

---

# 🎯 Use Cases

- HR Departments
- Recruitment Agencies
- University Placement Cells
- Startups
- Enterprises
- Campus Hiring
- Internship Recruitment

---

# 📈 Benefits

- Saves recruiter time
- Eliminates repetitive manual screening
- Standardizes candidate evaluation
- Improves hiring consistency
- Scales recruitment efficiently
- Reduces human bias in initial screening

---

# 🔒 Notes

- API credentials are managed securely through n8n Credentials.
- Sensitive candidate information should not be committed to public repositories.
- Sample resumes and anonymized data are recommended for demonstration.

---

# 👩‍💻 Author

**Nivedita Sharma**

Summer School '26 – OpenAI Agents SDK Capstone Project

Built using **n8n**, **Google Gemini**, **LlamaParse**, **Google Drive**, and **Google Sheets**.
