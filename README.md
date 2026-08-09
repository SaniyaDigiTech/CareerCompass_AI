🎯 CareerCompass AI

AI-Powered Personalized Career & Job Intelligence Assistant

CareerCompass AI is a Streamlit-based AI career guidance assistant designed to help students and early-career professionals understand their skills, explore suitable technology career paths, analyze their resumes, identify skill gaps, and create personalized career roadmaps.

The application uses an LLM-powered conversational interface to guide users through career decisions instead of providing only generic job suggestions.

✨ Key Features

💬 AI Career Conversation

Discuss your current skills, interests, and career confusion.

Get personalized career guidance through a conversational interface.

🎯 Career Path Recommendation

Explore suitable roles based on your current skills.

Examples include:

Forward Deployed Engineer (FDE)

AI/ML Engineer

Generative AI / Applied AI Engineer

Agentic AI Engineer

API / Backend Engineer

Data Scientist / Data Analyst

📄 Resume Analysis

Upload your resume in:

PDF

DOCX

TXT

PNG

JPG / JPEG

Extract resume content and analyze skills, projects, education, and experience.

🧠 Skill Gap Analysis

Compare your current profile with potential career paths.

Identify skills that should be improved for your target role.

🎓 Internship Guidance

Get guidance on whether an internship would be useful before applying for full-time roles.

Receive suggestions for practical experience and portfolio development.

🗺️ Personalized Career Roadmap

Get concise next steps based on your current profile and career goal.

Includes skills to learn and project directions.

💾 Conversation Memory

Chat history is stored using SQLite so the assistant can maintain conversation context.

🔐 User Authentication

Local username/password authentication.

Session-based access to the application.

⚡ Response Monitoring

Request ID

Session ID

Model information

Response duration

🧠 How CareerCompass AI Works

                    User
                     │
                     ▼
             Career Conversation
                     │
                     ▼
              Skill Understanding
                     │
            ┌────────┴────────┐
            ▼                 ▼
       Career Paths       Resume Upload
                              │
                              ▼
                       Resume Extraction
                              │
                              ▼
                       Resume Analysis
                              │
                              ▼
                       Skill Matching
                              │
                              ▼
                     Skill Gap Analysis
                              │
                              ▼
                 Internship / Job Guidance
                              │
                              ▼
                 Personalized Roadmap

🛠️ Tech Stack

Technology

Purpose

Python

Core application

Streamlit

Web interface

LangChain

LLM application orchestration

LangChain Core

Prompt and message handling

Groq

LLM API

Llama 3.3 70B

Conversational AI model

SQLite

Users, conversations and resume data

PyPDF

PDF text extraction

python-docx

DOCX text extraction

Pillow

Image processing

Tesseract OCR

Text extraction from resume images

📁 Project Structure

CareerCompass-AI/
│
├── app.py
├── requirements.txt
├── README.md
├── .gitignore
│
├── Assets/
│   └── CareerCompass_AI_Logo.png
│
└── screenshots/
    ├── login.png
    ├── chatbot.png
    ├── resume-upload.png
    └── resume-analysis.png

Runtime files such as the SQLite database, logs, uploaded resumes, and secrets should not be committed to GitHub.

🚀 Installation

1. Clone the repository

git clone YOUR_GITHUB_REPOSITORY_URL
cd CareerCompass-AI

2. Create a virtual environment

Windows:

python -m venv venv
venv\Scripts\activate

macOS / Linux:

python3 -m venv venv
source venv/bin/activate

3. Install dependencies

pip install -r requirements.txt

4. Run the application

streamlit run app.py

The application will open in your browser.

🔑 Groq API Key

CareerCompass AI requires a Groq API key to communicate with the LLM.

The current application accepts the API key through the Streamlit sidebar.

Never commit your API key to GitHub.

Do not add secrets such as:

gsk_...

to source files, README files, screenshots, or Git history.

📄 Resume Analysis Flow

Upload Resume
      │
      ▼
Preview File
      │
      ▼
Click "Analyze Resume"
      │
      ▼
Extract Text
      │
      ├── PDF → PyPDF
      ├── DOCX → python-docx
      ├── TXT → Text decoding
      └── Image → Tesseract OCR
      │
      ▼
Store Extracted Resume
      │
      ▼
Send Resume Context to AI
      │
      ▼
Career Analysis
      │
      ▼
AI Response in Chat

For image-based resume analysis, Tesseract OCR must be installed on the system in addition to the Python packages.

💬 Example Questions

Career Direction

I know Python and Machine Learning, and I also know GenAI and Agentic AI. I'm confused about which career path I should choose.

Role Comparison

Which is a better match for me: FDE, AI Engineer or API Engineer?

Resume Analysis

Based on my resume, which career path is the strongest match for me?

Skill Gaps

What skills am I missing for an AI Engineer role?

Internship

I don't have internship experience. Should I do an internship before applying for jobs?

Roadmap

Give me a 6-month roadmap to become job-ready for this role.

🔐 Data & Privacy

CareerCompass AI uses a local SQLite database for application data such as:

User accounts

Conversation history

Resume metadata and extracted resume text

Feedback

Do not commit the generated database file or personal resumes to a public GitHub repository.

For a production deployment, additional security measures should be implemented for authentication, secrets management, data encryption, and user privacy.

⚠️ Current Limitations

Salary information is currently treated as general career guidance rather than guaranteed live compensation data.

Exact job openings and salary figures should be verified through current job portals and official company sources.

Google login in the current code is a demo placeholder rather than a production Google OAuth implementation.

Image resume analysis requires Tesseract OCR.

Scanned/image-only PDFs may require an OCR-based PDF processing pipeline.

🔮 Future Improvements

Planned improvements include:

🔐 Real Google OAuth authentication

🔎 Live job and internship search

💰 Live salary and stipend intelligence with source attribution

📊 Resume-to-job match scoring

🎯 Career path scoring

🧠 Advanced skill-gap analysis

📄 Improved OCR for scanned PDFs

🎤 AI interview preparation

⚖️ Job comparison

☁️ Production deployment

🔒 Improved production-grade authentication and data security

🎥 Project Demo

A short screen recording can demonstrate the complete workflow:

Login
  ↓
Career Conversation
  ↓
Skill Analysis
  ↓
Resume Upload
  ↓
Analyze Resume
  ↓
Career Recommendation
  ↓
Skill Gap
  ↓
Internship / Job Guidance
  ↓
Career Roadmap

👩‍💻 Author

Saniya Patel

Built as an AI-powered career guidance project using Python, Streamlit, LangChain, Groq, SQLite, and resume-processing tools.

⭐ Project Goal

Don't just find a job. Find the right career path.

If you find this project useful, consider giving the repository a ⭐.
