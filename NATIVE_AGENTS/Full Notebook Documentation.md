## 📖 Full Notebook Documentation
### 1. Overview
This notebook serves as an educational framework for understanding **Autonomous AI Agents**. It demonstrates how to move beyond simple chat completion into "Agentic workflows" where an LLM can use external tools to solve complex, multi-step problems.

### 2. Core Architectures

#### A. The ReAct Pattern (Simple Agent)
- **Concept**: "Reason + Act". The model explicitly writes out its thoughts before taking an action.
- **Logic**: The agent loop uses regular expressions (`re.search`) to find specific patterns in the model's text (e.g., `THOUGHT:`, `ACTION:`, `ACTION_INPUT:`).
- **Pros**: Easy to understand and works with any model that can follow text instructions.
- **Cons**: Brittle. If the model misses a colon or fails to generate valid JSON in the middle of a sentence, the parser fails.

#### B. Native Function Calling (Native Agent)
- **Concept**: The model is aware of tools at the API level.
- **Logic**: Instead of parsing text, the system receives a structured `tool_calls` object from the API. The 'Thought' process is internal to the model's weights.
- **Pros**: Highly robust, handles structured data perfectly, and is the industry standard for production agents.
- **Cons**: Requires models specifically trained for function calling.

### 3. Toolset Breakdown

| Tool Name | Type | Description |
| :--- | :--- | :--- |
| `search_wikipedia` | Information | Fetches summaries from Wikipedia using a two-stage robust search (Direct -> Search Fallback). |
| `calculate` | Logic | Evaluates mathematical expressions safely using a restricted character set. |
| `get_current_date` | Utility | Provides real-time context (Date/Time) to the model. |
| `run_python` | Code | (Coding Agent only) Executes arbitrary Python code in a subprocess. |
| `read_file` / `write_file` | File System | (Coding Agent only) Allows the agent to persist data or modify the local environment. |

### 4. Key Functions

- `run_agent()`: The entry point for the ReAct loop.
- `run_native_agent()`: The entry point for the API-integrated function calling loop.
- `run_code_agent()`: A specialized ReAct loop designed for debugging and file manipulation.

### 5. Troubleshooting
- **Rate Limits**: If using `openrouter/free`, you may occasionally hit rate limits. The agent is designed to retry or report failures.
- **Tool Errors**: Observations are passed back to the model. If a tool fails (e.g., Wikipedia returns 404), the model is instructed to try a different query or approach.