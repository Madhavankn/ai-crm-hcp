# 🧠 AI-First CRM – HCP Interaction Module

## 🚀 Overview

The **AI-First CRM – HCP Interaction Module** is a smart customer relationship management system designed for **pharmaceutical field representatives** to efficiently log and manage interactions with Healthcare Professionals (HCPs).

This system introduces an **AI-driven workflow** where users can log interactions using either:

* 📋 Structured Form Input
* 💬 Conversational Chat Interface

The application leverages **LangGraph + Groq LLM (Gemma2-9B-IT)** to automatically extract, summarize, and structure interaction data—reducing manual effort and improving accuracy.

---

## 🎯 Key Features

* 🔄 Dual Input Modes (Form + Chat)
* 🧠 AI-powered data extraction & summarization
* 🏥 HCP interaction tracking
* ✏️ Edit logged interactions
* 📊 Sentiment analysis (Positive / Neutral / Negative)
* 📌 Smart follow-up recommendations
* 🗂️ Interaction history tracking

---

## 🏗️ Tech Stack

| Layer        | Technology                                  |
| ------------ | ------------------------------------------- |
| Frontend     | React.js + Redux                            |
| Backend      | FastAPI (Python)                            |
| AI Framework | LangGraph                                   |
| LLM          | Groq (gemma2-9b-it, llama-3.3-70b optional) |
| Database     | PostgreSQL / MySQL                          |
| Styling      | Google Inter Font                           |

---

## 🧩 System Architecture

```text
Frontend (React + Redux)
        ↓
Backend (FastAPI)
        ↓
LangGraph AI Agent
        ↓
Groq LLM (Gemma2-9B-IT)
        ↓
Database (PostgreSQL/MySQL)
```

---

## 🧠 LangGraph AI Agent

The **LangGraph agent** is the core intelligence layer responsible for:

* Understanding user input (chat/form)
* Extracting key entities (HCP, products, follow-ups)
* Generating structured summaries
* Triggering CRM tools
* Enhancing data quality using LLM reasoning

---

## 🔧 LangGraph Tools

### 1️⃣ Log Interaction (MANDATORY)

* Converts raw input into structured CRM data
* Uses LLM for:

  * Entity extraction
  * Summarization

**Example Output:**

```json
{
  "hcp_name": "Dr. Sharma",
  "products": ["Insulin"],
  "summary": "Discussed diabetes treatment and dosage plan",
  "follow_up": "Next Monday"
}
```

---

### 2️⃣ Edit Interaction (MANDATORY)

* Allows users to modify existing records
* Supports updates like:

  * Follow-up date
  * Notes
  * Products discussed

---

### 3️⃣ Get Interaction History

* Retrieves past interactions for a given HCP
* Helps in relationship tracking

---

### 4️⃣ Suggest Next Action

* Recommends next steps:

  * Schedule meeting
  * Send product brochure
  * Plan follow-up

---

### 5️⃣ Sentiment Analysis

* Detects interaction tone:

  * Positive
  * Neutral
  * Negative
* Helps prioritize engagement

---

## 🔄 AI Workflow

```text
User Input (Chat/Form)
        ↓
Intent Detection
        ↓
Entity Extraction
        ↓
Summarization
        ↓
Validation
        ↓
Tool Execution
        ↓
Database Storage
```

---

## 📁 Project Structure

```text
ai-crm-hcp/
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── redux/
│   │   └── App.js
│
├── backend/
│   ├── main.py
│   ├── langgraph_agent.py
│   ├── tools.py
│   ├── db.py
│   └── models.py
│
├── database/
│   └── schema.sql
│
└── README.md
```

---

## ⚙️ Installation & Setup

### 🔹 Prerequisites

* Node.js
* Python 3.9+
* PostgreSQL/MySQL
* Groq API Key

---

### 🔹 Backend Setup

```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

---

### 🔹 Frontend Setup

```bash
cd frontend
npm install
npm start
```

---

## 🧪 Sample Test Input

```text
Met Dr. Sharma, discussed insulin, follow-up next week
```

---

## 📊 Database Schema

| Column         | Type      |
| -------------- | --------- |
| id             | INT       |
| hcp_name       | VARCHAR   |
| products       | JSON      |
| summary        | TEXT      |
| follow_up_date | DATE      |
| sentiment      | VARCHAR   |
| created_at     | TIMESTAMP |

---

## 📹 Demo Video Includes

* Frontend walkthrough (Form + Chat)
* AI processing demonstration
* LangGraph tools execution
* Backend API explanation
* Project structure overview

---

## 💡 AI-First Impact

* ⏱️ Reduces manual CRM entry by **~60%**
* 📈 Improves data accuracy and consistency
* 🤖 Enables intelligent decision-making for field reps

---

## 🔮 Future Enhancements

* 🎤 Voice-to-text interaction logging
* 📅 Calendar & reminder integration
* 📊 Analytics dashboard
* 🔔 Smart notifications
* 🧠 Personalized HCP insights

---

## 👨‍💻 Author

**Madhavan K**
B.Tech – Information Technology
Aspiring Software Engineer | Cloud & AI Enthusiast

---
