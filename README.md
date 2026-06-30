# 🤖 Agentic AI from Scratch

> Learn how to build AI Agents from scratch using Python, OpenRouter, Tool Calling, ReAct, Code Agents, and Native Function Calling—without relying on high-level frameworks.

This repository is a **hands-on learning guide** that explains how modern AI agents work internally. Instead of using frameworks like LangChain or CrewAI from the beginning, we implement every component ourselves to understand the complete agent workflow.

By the end of this repository, you'll know how an AI agent communicates with an LLM, uses external tools, reasons through complex tasks, executes code, and performs native function calling.

---

## 🚀 Learning Roadmap

```
LLM API
    │
    ▼
Tool Calling
    │
    ▼
ReAct Agent
    │
    ▼
Agent Tracing & Context Engineering
    │
    ▼
Code Agent
    │
    ▼
Native Function Calling
```

---

## 📂 Repository Structure

```
Agentic-AI/
│
├── 01_LLM_API/
│   ├── README.md
│   ├── Documentation.md
│   └── LLM_API.ipynb
│
├── 02_Tool_Calling/
│   ├── README.md
│   ├── Documentation.md
│   └── Tool_Calling.ipynb
│
├── 03_ReAct_Agent/
│   ├── README.md
│   ├── Documentation.md
│   └── ReAct_Agent.ipynb
│
├── 04_Agent_Tracing/
│   ├── README.md
│   ├── Documentation.md
│   └── Agent_Tracing.ipynb
│
├── 05_Code_Agent/
│   ├── README.md
│   ├── Documentation.md
│   └── Code_Agent.ipynb
│
└── 06_Native_Function_Calling/
    ├── README.md
    ├── Documentation.md
    └── Native_Function_Calling.ipynb
```

---

# 📚 Modules

## 📡 Module 1 — LLM API

Learn how applications communicate with Large Language Models through APIs.

**Topics**

- API Fundamentals
- OpenRouter
- Authentication
- Request–Response Lifecycle
- Temperature
- Token Usage

---

## 🛠️ Module 2 — Tool Calling

Enable an LLM to use external tools by defining JSON schemas and executing Python functions.

**Topics**

- Tool Calling
- JSON Schema
- Function Execution
- Tool Responses
- Complete Tool Workflow

---

## 🤖 Module 3 — ReAct Agent

Build a complete **Reason + Act** agent from scratch.

**Topics**

- ReAct Prompting
- Agent Loop
- Thought
- Action
- Observation
- Multi-step Reasoning

---

## 💻 Module 4 — Code Agent

Build an AI coding assistant capable of interacting with files and executing Python code.

**Topics**

- File I/O
- Python Execution
- Code Generation
- Directory Management
- Multi-step Coding Tasks

---

## ⚡ Module 5 — Native Function Calling

Learn how modern LLMs perform built-in function calling without manual parsing.

**Topics**

- Function Schemas
- Native Tool Calling
- Structured Outputs
- Production Workflow

---

# 🛠️ Technologies Used

- Python
- Google Colab
- OpenRouter API
- JSON Schemas
- Wikipedia API
- Python Standard Library

---

# 🎯 What You'll Learn

After completing this repository, you'll be able to:

- Understand how AI agents work internally.
- Build your own ReAct Agent.
- Integrate external APIs as tools.
- Design custom tool schemas.
- Build Code Agents.
- Analyze token usage and context growth.
- Implement Native Function Calling.
- Understand the foundation of frameworks like LangChain, LangGraph, CrewAI, AutoGen, and OpenAI Agents SDK.

---

# 📖 Prerequisites

- Basic Python
- Functions
- JSON
- APIs (recommended)
- No prior AI Agent experience required

---

# ▶️ Getting Started

1. Clone the repository.

```bash
git clone https://github.com/your-username/Agentic-AI.git
```

2. Install dependencies.

```bash
pip install openai requests
```

3. Add your OpenRouter API Key.

```python
OPENROUTER_API_KEY = "your_api_key"
```

4. Open the notebooks in Google Colab or Jupyter Notebook.

5. Follow the modules in numerical order.

---

# 📚 References

- OpenRouter Documentation  
  https://openrouter.ai/docs

- OpenAI API Documentation  
  https://platform.openai.com/docs

- ReAct Research Paper  
  https://arxiv.org/abs/2210.03629

- JSON Schema  
  https://json-schema.org/

- Python Documentation  
  https://docs.python.org/3/

---

# ⭐ Support

If you found this repository helpful:

⭐ Star the repository

🍴 Fork it

📢 Share it with others

---

## 📄 License

This project is intended for educational purposes and personal learning.
