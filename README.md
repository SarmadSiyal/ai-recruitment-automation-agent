# 🤖 AI Recruitment Intelligence Automation System

A production-ready AI-powered recruitment automation system that intelligently screens CVs, evaluates candidates using LLM-based scoring, validates applications, classifies applicants, auto-schedules interviews, and streamlines hiring operations with a professional candidate experience.

---

## 🚀 Project Overview

The **AI Recruitment Intelligence Automation Platform** is an end-to-end hiring automation solution designed to reduce manual HR workload and improve recruitment efficiency.

Built using:

- **n8n** – Workflow Automation Engine  
- **Groq LLaMA 3 (70B)** – Large Language Model  
- **Gmail API** – Email Intake & Communication  
- **Google Sheets** – Recruitment CRM & Job Database  
- **JavaScript** – Smart Interview Scheduling Logic  

The system automatically:

- 📥 Monitors incoming candidate applications  
- 📎 Accepts only emails with attachments  
- 📄 Validates CV file format (PDF only)  
- 🧠 Extracts and evaluates candidate profiles using AI  
- 📊 Scores applicants against job requirements  
- 🟢 Classifies candidates (Shortlisted / Rejected / Position Closed)  
- 📅 Generates optimized interview schedules  
- 📧 Sends professional automated responses  
- 🗂 Maintains structured candidate records  
- 👥 Notifies HR team with interview details  

---

## 🎯 Objectives

- Automate CV screening and candidate evaluation  
- Reduce repetitive HR workload  
- Improve response time to applicants  
- Create structured candidate comparison process  
- Improve hiring consistency using AI scoring  
- Deliver scalable recruitment operations  
- Maintain professional candidate communication  

---

# 🧠 Production Workflow Architecture

```text
Inbound CV Email Listener
        ↓
Fetch Candidate Email Content
        ↓
Validate PDF Attachment Format
   ├── Invalid File → Request PDF CV + Mark Reviewed
   └── Valid File
            ↓
Extract CV Text from PDF
            ↓
Prepare Candidate Data Payload
            ↓
AI Candidate Evaluation Engine
            ↓
Fetch Open Job Requirements
            ↓
Normalize Evaluation Results
            ↓
Check Job Vacancy Status
   ├── Closed → Send Position Closed Email
   └── Open
          ↓
Check Candidate Shortlist Status
   ├── Shortlisted Flow
   │      ↓
   │ Send Confirmation Email
   │ Store Candidate Record
   │ Delay (Human-like Review)
   │ Generate Interview Schedule
   │ Send Interview Invitation
   │ Update CRM
   │ Notify HR Team
   │
   └── Rejected Flow
          ↓
      Send Confirmation Email
      Delay (Manual Review Simulation)
      Send Rejection Email

--------------------------------------------------------------------------------

## ⚙️ TECHNOLOGIES USED

• n8n
• Groq LLaMA 3 (70B)
• Gmail API (OAuth2)
• Google Sheets API
• JavaScript
• PDF Text Extraction
• JSON Structured Output
• AI Decision Workflows

--------------------------------------------------------------------------------

## 🔄 WORKFLOW BREAKDOWN

1️⃣ Candidate Application Intake

• The system monitors new Gmail messages
• Only Inbox emails with attachments are processed
• Prevents irrelevant email execution

--------------------------------------------------

2️⃣ File Validation Layer

• Checks whether attachment is in PDF format

If Invalid:

• Sends professional email requesting PDF CV
• Marks email as reviewed
• Ends process

If Valid:

• Continues to AI screening process

--------------------------------------------------

3️⃣ Resume Parsing Engine

• Extracts text from PDF CV
• Structures candidate information:

  - Full Name
  - Email
  - Phone Number
  - Skills
  - Experience
  - Education

--------------------------------------------------

4️⃣ AI Candidate Evaluation Engine

• Fetches open job requirements from Google Sheets
• Compares candidate profile against job criteria
• Calculates:

  - Skills Score
  - Experience Score
  - Education Score

Overall Score:

overall_score = (skills_score + experience_score + education_score) / 3

--------------------------------------------------

5️⃣ Vacancy Status Logic

• Checks whether the job position is open

If Closed:

• Sends position closed notification to candidate

--------------------------------------------------

6️⃣ Candidate Classification Logic

If Open Role:

--------------------------------------------------

✅ Shortlisted Candidate Flow

• Sends application received confirmation
• Stores candidate in CRM sheet
• Adds short delay for human-like review
• Generates interview date & time
• Sends interview invitation with:

  - Date
  - Time
  - Location
  - Google Maps Link

• Updates CRM with interview schedule
• Sends HR notification email

--------------------------------------------------

❌ Rejected Candidate Flow

• Sends application received confirmation
• Waits before rejection response
• Sends polite rejection email
• Marks email as processed

--------------------------------------------------------------------------------

## 📁 DATABASE STRUCTURE

Job Requirements Sheet

• Job ID
• Position Title
• Required Skills
• Minimum Experience
• Required Education
• Job Status
• Hiring Priority

--------------------------------------------------

Candidate CRM Sheet

• Candidate ID
• Full Name
• Email
• Phone
• Skills Score
• Experience Score
• Education Score
• Overall Score
• Final Decision
• Interview Date
• Interview Time
• Status

--------------------------------------------------------------------------------

## 🔐 SECURITY & RELIABILITY

• Gmail OAuth2 Authentication
• Controlled Google Sheets Access
• Structured AI JSON Output
• No public candidate data exposure
• Professional communication flow
• Production-ready logic separation

--------------------------------------------------------------------------------

## 🚀 KEY FEATURES

• Intelligent CV Screening
• AI Candidate Scoring
• PDF Validation Layer
• Vacancy Status Check
• Interview Auto Scheduling
• CRM Record Management
• Human-like Delayed Communication
• HR Team Notifications
• Scalable Hiring Operations

--------------------------------------------------------------------------------

## 📈 BUSINESS IMPACT

• Reduces manual CV screening time
• Improves hiring speed
• Standardizes candidate evaluation
• Enhances candidate experience
• Saves recruiter time
• Scales recruitment efficiently

--------------------------------------------------------------------------------

## 🏗 FUTURE IMPROVEMENTS

• HR Dashboard
• ATS Integration
• PostgreSQL Upgrade
• Candidate Ranking Dashboard
• WhatsApp Candidate Notifications
• Multi-role Hiring Pipelines
• Calendar Auto Booking

--------------------------------------------------------------------------------

## 👨‍💻 AUTHOR

Sarmad Siyal
AI Automation Specialist | AI Agent Builder | Workflow Engineer
