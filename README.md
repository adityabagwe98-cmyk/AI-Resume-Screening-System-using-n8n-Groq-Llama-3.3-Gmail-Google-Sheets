# AI-Resume-Screening-System-using-n8n-Groq-Llama-3.3-Gmail-Google-Sheets
Built an AI-powered resume screening workflow using n8n. Automatically retrieves resumes from Gmail, extracts PDF content, analyzes candidates with Groq Llama 3.3, scores resumes based on hiring criteria, stores results in Google Sheets, and sends automated interview or rejection emails.
 #  AI Resume Screening System

An end-to-end AI-powered resume screening workflow built with **n8n**, **Groq Llama 3.3**, **Gmail**, and **Google Sheets**. The system automatically retrieves resumes from Gmail, extracts text from PDF files, evaluates candidates using AI, stores structured results in Google Sheets, and sends interview or rejection emails based on predefined hiring criteria.

---

##  Features

*  Automatically monitors Gmail for new resume emails
*  Downloads PDF resume attachments
*  Extracts text from PDF resumes
*  Analyzes resumes using Groq Llama 3.3 LLM
*  Scores candidates out of 100
*  Determines interview eligibility (YES/NO)
*  Extracts:

  * Name
  * Email
  * Phone
  * Education
  * Experience
  * Skills
  * Strengths
  * Weaknesses
*  Saves structured candidate data to Google Sheets
*  Sends automated interview or rejection emails

---

##  Tech Stack

* n8n
* Groq Llama 3.3 (70B Versatile)
* Gmail API
* Google Sheets API
* JavaScript
* PDF Text Extraction
* JSON Processing

---

##  Workflow

```text
Gmail Trigger
      │
      ▼
Get Message
      │
      ▼
Download PDF Attachment
      │
      ▼
Extract PDF Text
      │
      ▼
AI Resume Analysis (Groq)
      │
      ▼
Parse JSON (JavaScript)
      │
      ▼
Google Sheets
      │
      ▼
IF (Score ≥ 75)
   ┌──────┴──────┐
   ▼             ▼
Interview     Rejection
Email         Email
```

---

##  AI Evaluation Criteria

| Category          | Weight  |
| ----------------- | ------- |
| Education         | 20      |
| Experience        | 30      |
| Skills            | 30      |
| Communication     | 10      |
| Resume Formatting | 10      |
| **Total**         | **100** |

Decision Rule:

* Score ≥ 75 → Interview = YES
* Score < 75 → Interview = NO

---

##  Google Sheets Output

Each resume is stored with the following information:

* Name
* Email
* Phone
* Education
* Experience
* Skills
* Resume Score
* Interview Decision
* Strengths
* Weaknesses
* Reason
* Date Processed

---

##  Example AI Output

```json
{
  "name": "John Doe",
  "email": "john@example.com",
  "phone": "+1 555-123-4567",
  "education": "B.Tech Computer Science",
  "experience_years": 5,
  "skills": [
    "Python",
    "SQL",
    "JavaScript",
    "AWS"
  ],
  "strengths": "Strong technical background with relevant industry experience.",
  "weaknesses": "Resume formatting can be improved.",
  "resume_score": 85,
  "interview": "YES",
  "reason": "Strong technical skills and relevant experience."
}
```

---

##  Skills Demonstrated

* Workflow Automation
* AI Integration
* Resume Parsing
* Prompt Engineering
* API Integration
* Gmail Automation
* Google Sheets Automation
* PDF Processing
* JSON Parsing
* JavaScript
* Conditional Logic

---

##  Future Improvements

* Match resumes against job descriptions
* Rank candidates automatically
* HR dashboard with analytics
* Candidate shortlist generation
* Calendar integration for interview scheduling
* Multi-language resume support
* ATS keyword matching
* Duplicate candidate detection

---

## 👨‍💻 Author

**Aditya Bagwe**

If you found this project useful, feel free to ⭐ this repository.
