# 🚀 TaskNova – Multi-Agent Productivity Assistant

TaskNova is an AI-powered multi-agent productivity assistant built using **Google Agent Development Kit (ADK)**.  
It helps users manage tasks, organize notes, and automate workflows through intelligent agent orchestration.

---

## 🤖 Overview

TaskNova uses a **multi-agent architecture** where a root agent coordinates specialized agents to perform real-world actions using MCP tools and Google Cloud Datastore.

It enables:
- Task management (add, view, complete)
- Note-taking
- Persistent storage
- Real-time AI-driven workflow execution

---

## ✨ Features

- 🤖 Multi-agent system using Google ADK
- 🧠 Intelligent task understanding from natural language
- 📋 Add, list, and complete tasks
- 📝 Store structured notes
- 🗄️ Persistent storage using Google Datastore
- 🔗 MCP tools for real-world actions
- ⚡ FastAPI backend for API deployment
- ☁️ Deployable on Google Cloud Run
- 🌐 Interactive Agent UI (ADK Dev UI)

---

## 🏗️ Architecture

User Input  
↓  
Root Agent (Orchestrator)  
↓  
Workflow Agent (Sequential Execution)  
↓  
TaskNova Agent  
↓  
MCP Tools  
↓  
Google Datastore (DB)  
↓  
Response to User  

---

## 🛠️ Tech Stack

- Python
- Google ADK (Agent Development Kit)
- FastAPI
- MCP (FastMCP Tools)
- Google Cloud Datastore
- Uvicorn
- Pydantic
- Google Cloud Run

---

<img width="1920" height="1020" alt="Working 2" src="https://github.com/user-attachments/assets/597cda6e-29ac-47a0-a6f8-59626e73bb5e" />

## 📂 Project Structure

.
├── agent.py
├── requirements.txt
├── .env
├── README.md

---

## ⚙️ Installation

```bash
git clone <your-repo-url>
cd tasknova
pip install -r requirements.txt
```

---

## ▶️ Run Locally

```bash
uvicorn agent:app --reload
```

---

## ☁️ Deploy to Google Cloud Run

```bash
uvx --from google-adk==1.14.0 \
adk deploy cloud_run \
  --project=$PROJECT_ID \
  --region=europe-west1 \
  --service_name=tasknova \
  --with_ui \
  . \
  -- \
  --service-account=$SERVICE_ACCOUNT
```

---

## 🔐 Environment Variables

Create a `.env` file:

```
MODEL=gemini-1.5-flash
```

---

## 📌 Usage

- Add a task: Add a task: Play Chess  
- View tasks: List my tasks  
- Complete task: Complete task 12345  
- Add a note: Add a note titled Meeting Notes with content Project discussion  

---

## 🧠 How It Works

- The root agent receives user input  
- Input is stored in shared state  
- Workflow agent delegates execution  
- TaskNova agent selects appropriate MCP tool  
- Tools interact with Google Datastore  
- Response is generated and returned  

---

## 🔥 Unique Selling Points (USP)

- Multi-agent orchestration  
- Real-world task execution via MCP tools  
- Persistent memory with Datastore  
- Scalable modular architecture  
- Cloud-native deployment ready  

---

## 🚀 Future Enhancements

- Calendar integration  
- Notifications & reminders  
- Voice input support  
- Mobile app interface  
- AI-based task prioritization  

---

## ⭐ Acknowledgement

Built as part of Google Gen AI Academy Hackathon (APAC Edition).
