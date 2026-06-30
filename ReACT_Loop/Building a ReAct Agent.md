# 🤖 Module 3: Building a ReAct Agent from Scratch

In the previous module, we learned how an LLM can use external tools. However, real-world AI agents often need to perform multiple reasoning steps before arriving at a final answer. This is where the **ReAct (Reason + Act)** framework comes into play.

In this module, we'll build a ReAct Agent completely from scratch using Python. Instead of relying on frameworks like LangChain or CrewAI, we'll implement the entire reasoning loop ourselves. The agent will think about the problem, choose the appropriate tool, observe the result, and continue reasoning until it has enough information to answer the user's query.

## 📚 Topics Covered

- What is ReAct?
- ReAct Prompting
- Thought → Action → Observation Loop
- Building the Agent Loop
- Tool Integration
- Multi-step Reasoning
- Agent Execution
- Testing the Agent

## 🎯 Learning Outcome

After completing this module, you will understand how modern AI agents repeatedly reason, use tools, observe results, and generate final answers. You'll also gain a solid understanding of the internal workflow used by many popular AI agent frameworks.

---

## 📚 References

- ReAct: Synergizing Reasoning and Acting in Language Models (Research Paper)  
  https://arxiv.org/abs/2210.03629

- OpenAI Function Calling Documentation  
  https://platform.openai.com/docs/guides/function-calling

- OpenRouter Documentation  
  https://openrouter.ai/docs