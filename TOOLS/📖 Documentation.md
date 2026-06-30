# 📖 Documentation

# Introduction

A Large Language Model has extensive knowledge but cannot directly interact with the outside world. For example, it cannot retrieve live weather information, search Wikipedia, calculate mathematical expressions using external code, or access databases. To perform these tasks, we provide the model with **tools**.

Tool Calling allows the model to decide **when** a tool is needed and **which** tool should be used, while the actual execution is performed by our Python application.

---

# Why Do LLMs Need Tools?

LLMs generate responses using the knowledge stored during training. They do not have real-time access to external information or the ability to execute functions.

By connecting tools to the model, we extend its capabilities beyond text generation. These tools can access APIs, perform calculations, retrieve information, manipulate files, or interact with other software systems.

---

# What is Tool Calling?

Tool Calling is the process where an LLM determines that additional information or an external action is required. Instead of answering immediately, it generates a structured request containing:

- Tool Name
- Required Arguments

The application receives this request, executes the corresponding function, and sends the result back to the model. The model then uses the observation to generate the final answer.

---

# JSON Tool Schema

Every tool is described using a JSON schema. The schema tells the model:

- Tool name
- Purpose of the tool
- Accepted parameters
- Required inputs

The model does not execute these tools directly. It only understands what tools are available and generates structured requests to use them.

---

# Tool Calling Workflow

The complete workflow follows these steps:

```text
User Query
     │
     ▼
Large Language Model
     │
     ▼
Select Tool
     │
     ▼
Generate Tool Call
     │
     ▼
Python Executes Tool
     │
     ▼
Tool Result
     │
     ▼
Large Language Model
     │
     ▼
Final Response
```

This separation of responsibilities is important:

- **LLM** → Decides which tool to use.
- **Python Application** → Executes the tool.
- **Tool** → Returns the requested information.
- **LLM** → Generates the final answer.

---

# Advantages

- Access to real-time information.
- Ability to interact with external APIs.
- More accurate and reliable responses.
- Extensible architecture for AI agents.

---

# Summary

In this module, we learned how Tool Calling enables Large Language Models to interact with external systems. Instead of relying only on their internal knowledge, models can request tools whenever additional information or actions are required. We explored how tools are defined using JSON schemas, how the model selects the appropriate tool, and how our Python application executes the requested function before returning the result back to the model.

Understanding Tool Calling is a major milestone because nearly every modern AI agent—from coding assistants to autonomous research agents—relies on this mechanism to interact with APIs, databases, search engines, and other external services. This module provides the foundation for the next step: building a **ReAct Agent**, where the model repeatedly reasons, selects tools, observes results, and continues until the task is complete.S