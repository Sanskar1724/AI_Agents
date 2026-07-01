# 🤖 AI Agent Frameworks: Simple vs. Native

This notebook provides a hands-on exploration of two primary ways to build AI Agents that can use external tools: **ReAct (Reason + Act)** and **Native Function Calling**.

## 📋 Features
- **Simple ReAct Agent**: Uses custom string parsing and a specific system prompt to manage thoughts and actions.
- **Native Function-Calling Agent**: Leverages modern LLM APIs (via OpenRouter) to handle tool selection and argument generation natively.
- **Coding Agent Extension**: A specialized version of the agent equipped with file I/O and shell execution capabilities.
- **Real-World Tools**: Integrated with Wikipedia search, a safe math calculator, and real-time clock access.

## 🛠️ Setup

1. **API Key**: Ensure you have an [OpenRouter](https://openrouter.ai/) API key.
2. **Colab Secrets**: Add your key to the Colab secrets manager (key icon on the left) with the name `OPENROUTER_API_KEY`.
3. **Dependencies**: Run the first code cell to install `openai` and `requests`.

## 🏗️ Architecture

### 1. Simple ReAct Agent
Uses the `run_agent()` function. It expects the model to output text in the following format:
- `THOUGHT:` Reasoning process.
- `ACTION:` Name of the tool to use.
- `ACTION_INPUT:` JSON arguments for the tool.

### 2. Native Agent
Uses the `run_native_agent()` function. It does not use regex parsing. Instead, it sends a JSON schema of tools to the model, and the model responds with a structured `tool_calls` object.

### 3. Coding Agent
A high-capability version that can:
- `read_file` / `write_file`: Manipulate local storage.
- `run_python`: Execute code and observe output/errors.
- `list_files`: Inspect the directory structure.

## 🚀 How to Run

To start the simple agent:
```python
run_agent("What is 25 * 42?")s