Multi-Agent AI System
LangGraph + FastAPI Powered Agentic Framework
📌 Overview
This project is an advanced multi-agent AI system designed to solve real-world problems using a centralized Multi-Agent Orchestrator. It combines reasoning, memory, and tool usage by integrating Llama 3.3, FAISS, live APIs, and SQL databases into a single intelligent framework.
🧠 System Architecture
The system follows an agentic workflow, where multiple specialized agents collaborate under a LangGraph-based orchestrator to process user queries, make decisions, and execute actions efficiently.
🌟 Specialized Agents
1. Weather Agent
Identifies city names from user input
Fetches real-time weather data using the OpenWeather API
Returns structured and readable weather responses
2. Resume / Knowledge Agent (RAG)
Performs document-based question answering using FAISS
Supports PDF and TXT file uploads
Falls back to DuckDuckGo web search if local context is insufficient
3. Smart Scheduler Agent
Applies logical reasoning before booking meetings
Validates weather conditions prior to scheduling
Stores approved schedules in the SQLite database
4. Database Agent
Connects directly to SQLite
Retrieves and displays stored records
Supports structured SQL-based queries

📁 Project Structure
Copy code

agentic_ai/
├── app/
│   ├── __init__.py
│   ├── main.py          # FastAPI server & API routes
│   ├── agents.py        # LangGraph multi-agent orchestrator
│   ├── tools.py         # Weather, search, and SQL tools
│   ├── database.py      # SQLite configuration
│   └── vector_store.py  # FAISS indexing & embedding logic
├── .env                 # Environment variables (create manually)
└── README.md            # Project documentation
⚙️ Environment Configuration
Create a .env file in the project root and add your API keys:
Copy code
Env
GROQ_API_KEY=your_key_here
OPENWEATHER_API_KEY=your_key_here
▶️ Running the Application
Copy code
Bash
python -m app.main
