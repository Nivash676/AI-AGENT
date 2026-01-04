# Multi-Agent AI System
### LangGraph + FastAPI Powered Agentic Framework

---

## 📌 Overview
This project is an advanced multi-agent AI system designed to solve real-world problems using a centralized **Multi-Agent Orchestrator**. It combines reasoning, memory, and tool usage by integrating **Llama 3.3**, **FAISS**, live APIs, and **SQL databases** into a single intelligent framework.

## 🧠 System Architecture
The system follows an agentic workflow, where multiple specialized agents collaborate under a **LangGraph-based orchestrator** to process user queries, make decisions, and execute actions efficiently.



---

## 🌟 Specialized Agents

| Agent | Responsibility | Key Tools |
| :--- | :--- | :--- |
| **Weather Agent** | Identifies cities and fetches real-time data. | OpenWeather API |
| **RAG Agent** | Document-based QA (PDF/TXT) with web fallback. | FAISS, DuckDuckGo |
| **Scheduler Agent** | Logic-based meeting booking with condition checks. | SQLite, Custom Logic |
| **Database Agent** | Direct SQLite connection and record retrieval. | SQL Queries |

---


## 📁 Project Structure

```text
agentic_ai/
├── app/
│   ├── main.py          # FastAPI server & API routes
│   ├── agents.py        # LangGraph multi-agent orchestrator
│   ├── tools.py         # Weather, search, and SQL tools
│   ├── database.py      # SQLite configuration
│   └── vector_store.py  # FAISS indexing & embedding logic
├── .env                 # API keys (GROQ, OpenWeather)
└── README.md            # Project documentation

▶️ Running the Application

Start the FastAPI server using the following command:
          python -m app.main

The API will be available at http://127.0.0.1:8000. You can access the interactive Swagger documentation at /docs