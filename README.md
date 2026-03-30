# 🤖 AI Recruitment Intelligence Agent System

An end-to-end AI-powered recruitment automation system that automatically screens CVs, evaluates candidates using LLM-based scoring, classifies applicants, and auto-schedules interviews — reducing manual HR workload and improving hiring efficiency.

---

## 🚀 Project Overview

The **AI Recruitment Intelligence Agent** is a production-ready hiring automation system built using:

- **n8n** (Workflow Automation Engine)
- **Groq LLaMA 3 (70B)** – Large Language Model
- **Gmail API** – Email monitoring & automation
- **Google Sheets** – Lightweight structured database

The system automatically:

- 📥 Monitors incoming CV emails  
- 📄 Extracts and parses PDF resumes  
- 🧠 Evaluates candidates using AI scoring  
- 📊 Classifies applicants (Shortlisted / Rejected / Closed)  
- 📅 Auto-schedules interviews  
- 📧 Sends automated email responses  
- 🗂 Maintains structured candidate database  

---

## 🎯 Objectives

- Automate CV screening process  
- Reduce manual HR workload  
- Improve hiring response time  
- Enable structured candidate comparison  
- Minimize bias using AI-based scoring  
- Build scalable recruitment automation  

---

## 🧠 System Architecture

```
Gmail Trigger
      ↓
CV Extraction (PDF Parser)
      ↓
AI Evaluation Agent (Groq LLaMA 3)
      ↓
Scoring Engine
      ↓
Classification Logic
      ↓
Email Automation
      ↓
Database Update (Google Sheets)
      ↓
Interview Scheduling
```

---

## ⚙️ Technologies Used

- n8n
- Groq LLaMA 3 (70B)
- Gmail API (OAuth2)
- Google Sheets API
- JSON Parsing
- PDF Text Extraction

---

## 🔄 Workflow Breakdown

### 1️⃣ CV Reception

- Gmail Trigger monitors unread emails with attachments.
- Automatically detects incoming resumes.

---

### 2️⃣ Resume Parsing

- Extract File Node extracts text from PDF.
- CV content stored as structured variable (`cv_text`).

---

### 3️⃣ AI Candidate Evaluation

The AI Agent performs:

- Candidate information extraction  
- Job requirement retrieval from Google Sheets  
- Skills matching  
- Experience comparison  
- Education verification  
- Structured score calculation  

### 📊 Scoring Formula

```javascript
overall_score = (skills_match + experience_match + education_match) / 3
```

---

### 4️⃣ Decision Logic

- **Score ≥ 70 → Shortlisted**
- **Score < 70 → Rejected**
- **Job Closed → Closed**

---

### 5️⃣ Automated Email Responses

The system automatically sends:

- ✅ Interview invitation email  
- ❌ Rejection email  
- 📌 Position closed notification  

---

### 6️⃣ Interview Scheduling

Interview date is automatically generated:

```javascript
current_date + 2 days
```

Email includes:

- Interview date & time  
- Location  
- Instructions  

---

### 7️⃣ Database Structure

### 📁 Job Database (Google Sheets)

- Job ID  
- Position Title  
- Required Skills  
- Minimum Experience  
- Required Education  
- Interview Schedule  
- Job Status  

### 📁 Shortlisted Applicants Database

- Applicant ID  
- Candidate Name  
- Email  
- Phone  
- Skills Match Score  
- Experience Match Score  
- Education Match Score  
- Overall Score  
- Interview DateTime  
- Status  

---

## 📸 Screenshots

### Workflow Architecture

<p align="center">
  <img src="./Screenshots/Workflow_Architecture.png" alt="Workflow Architecture" width="800"/>
</p>

**Image Description:**  
The image displays the complete n8n workflow architecture including Gmail trigger, CV extraction node, AI evaluation agent (Groq LLaMA 3), scoring engine, classification logic, interview scheduling module, and Google Sheets database integration.

---

## 🔐 Security Considerations

- Gmail OAuth authentication  
- Secure Google Sheets access  
- No external storage outside Google ecosystem  
- Structured JSON AI output for controlled automation  

---

## 🚀 Key Features

- Fully automated recruitment pipeline  
- AI-based candidate scoring  
- Structured decision engine  
- Auto interview scheduling  
- Real-time email automation  
- Bias-reduced early-stage screening  
- Scalable architecture  

---

## 🏗 Future Improvements

- HR dashboard interface  
- CRM integration (HubSpot / Zoho)  
- PostgreSQL database upgrade  
- Candidate ranking analytics  
- Multi-job parallel processing  

---

## 📌 Business Impact

- Reduces manual CV screening time  
- Improves hiring speed  
- Enables structured and consistent evaluation  
- Minimizes human bias  
- Scalable for growing organizations  

---

## 👨‍💻 Author

**Sarmad Siyal**  
AI Automation Specialist | AI Agent Builder | AI Workflow Engineer
