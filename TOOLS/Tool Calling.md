# 🛠️ Module 2: Tool Calling

Large Language Models are excellent at reasoning and generating text, but they cannot interact with external systems on their own. They cannot fetch live weather data, search the internet, perform file operations, or query databases unless they are provided with tools.

In this module, we learn how to extend an LLM by providing it with external tools. We'll define tools using JSON schemas, allow the model to choose the appropriate tool, execute the tool in Python, and return the result back to the model. This process is known as **Tool Calling** and forms the foundation of modern AI agents.

## 📚 Topics Covered

- Why LLMs Need Tools
- Tool Calling
- JSON Tool Schema
- Tool Selection
- Tool Execution
- Tool Response
- Complete Tool Calling Workflow

## 🎯 Learning Outcome

After completing this module, you will understand how an LLM selects tools, how your Python application executes those tools, and how the model uses the returned information to generate its final response.

---

## 📚 References

- OpenAI Function Calling Documentation  
  https://platform.openai.com/docs/guides/function-calling

- OpenRouter Tool Calling Documentation  
  https://openrouter.ai/docs/features/tool-calling

- JSON Schema Documentation  
  https://json-schema.org/S