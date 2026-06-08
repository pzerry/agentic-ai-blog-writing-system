# 🚀 Agentic AI Blog Writing System

An end-to-end multi-agent content generation platform built using **LangGraph**, **Groq**, **LangSmith**, and **Streamlit**.

This project automatically researches a topic, plans a blog structure, generates content using parallel AI agents, adds relevant visual content, and produces a complete markdown blog ready for publishing.

---

## 🎯 Why I Built This

Most AI writing tools are simple prompt wrappers that generate content in a single step.

I wanted to explore how modern **Agentic AI systems** work by building a workflow where multiple specialized agents collaborate to create high-quality technical content.

The system mimics a real content team:

* A Router decides what needs research.
* A Research Agent gathers evidence from the web.
* A Planner creates a content strategy.
* Multiple Writer Agents generate sections in parallel.
* A Reducer combines everything into a polished article.
* An Image Agent adds supporting visuals.

---

## 🏗️ Architecture

```text
User Topic
    │
    ▼
 Router Agent
    │
    ▼
 Research Agent (DDGS)
    │
    ▼
 Planner Agent
    │
    ▼
 Parallel Writer Agents
    │
    ▼
 Reducer Agent
    │
    ▼
 Image Planning Agent
    │
    ▼
 Final Blog
```

---

## ✨ Key Features

### Multi-Agent Workflow

Built using LangGraph state machines and agent orchestration.

### Intelligent Research Routing

Automatically determines whether a topic requires:

* No research
* Limited research
* Research-heavy generation

### Research-Augmented Generation (RAG)

Uses DuckDuckGo Search to gather evidence and ground generated content.

### Parallel Content Generation

Multiple writer agents generate sections simultaneously, reducing generation time.

### Automated Visual Content

Creates image prompts and embeds supporting diagrams into generated blogs.

### LangSmith Observability

Tracks:

* Agent execution
* Prompt flows
* State transitions
* Debugging traces

### Interactive UI

Simple Streamlit interface for generating blogs from a single topic prompt.

---

## 🛠️ Tech Stack

### AI & Agent Frameworks

* LangGraph
* LangChain
* Pydantic

### Models

* Groq

  * Llama 3.1 8B Instant
  * Llama 3.3 70B Versatile

### Research

* DDGS (DuckDuckGo Search)

### Images

* Pollinations AI

### Observability

* LangSmith

### Frontend

* Streamlit

---

## ⚙️ How It Works

### Step 1 — Routing

The Router Agent determines whether the topic requires external research.

### Step 2 — Research

If research is needed, the system generates search queries and gathers evidence from the web.

### Step 3 — Planning

The Planner Agent creates a detailed blog outline with writing objectives.

### Step 4 — Parallel Writing

Multiple Writer Agents generate individual sections independently.

### Step 5 — Reduction

All generated sections are merged into a coherent article.

### Step 6 — Image Planning

The system identifies where diagrams or visuals would improve understanding.

### Step 7 — Publishing

A final markdown document is generated and saved locally.

---

## 📂 Project Structure

```text
blog-writing-agent/
│
├── bwa_backend.py
├── bwa_frontend.py
│
├── images/
│
├── README.md
├── requirements.txt
├── .env.example
└── .gitignore
```

---

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/blog-writing-agent.git

cd blog-writing-agent
```

Create a virtual environment:

```bash
python -m venv .venv

source .venv/bin/activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a `.env` file:

```env
GROQ_API_KEY=your_groq_api_key

LANGCHAIN_API_KEY=your_langsmith_api_key
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=blog-writing-agent
```

---

## ▶️ Run the Application

```bash
streamlit run bwa_frontend.py
```

---

## 🧪 Example Topics

* Building Production-Ready Multi-Agent Systems with LangGraph
* Agentic AI Design Patterns
* RAG vs Agentic RAG
* How LangGraph Works: Router, Planner, Workers, and Reducers Explained
* AI Agent Architectures for Enterprise Applications

---

## 📈 What This Project Demonstrates

* Agentic AI Design
* Multi-Agent Orchestration
* LangGraph Workflows
* Research-Augmented Generation
* Parallel Agent Execution
* Prompt Engineering
* LangSmith Tracing
* Production-Style AI Application Development

---

## 🔮 Future Improvements

* Vector Database Integration
* Human-in-the-Loop Review
* SEO Optimization Agent
* Multi-Language Support
* WordPress Publishing
* Fact Verification Agent
* Scheduled Content Generation

---

## 👩‍💻 Author

**Pooja Sharma**

AI Engineer | Agentic AI | LangGraph | LLM Applications

If you found this project useful, consider giving it a ⭐ on GitHub.
