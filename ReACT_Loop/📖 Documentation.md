# 📖 Documentation

# Introduction

As AI systems become more capable, answering complex questions often requires more than a single response from the language model. Some problems require searching for information, performing calculations, verifying results, or using multiple tools before producing the final answer.

The **ReAct (Reason + Act)** framework addresses this challenge by allowing an AI agent to repeatedly reason, perform actions, observe the results, and continue the process until the task is completed. This iterative workflow makes AI agents significantly more powerful than traditional chatbots.

---

# What is ReAct?

ReAct stands for **Reason + Act**.

Instead of generating an answer immediately, the language model first reasons about the problem, decides whether it needs a tool, executes the tool through the application, observes the returned information, and then continues reasoning.

This process continues until the model has collected enough information to produce the final answer.

---

# The ReAct Loop

A ReAct Agent follows a continuous reasoning cycle.

```text
User Query
      │
      ▼
Reason (THOUGHT)
      │
      ▼
Choose Tool (ACTION)
      │
      ▼
Execute Tool
      │
      ▼
Observation
      │
      ▼
Reason Again
      │
      ▼
Repeat Until...
      │
      ▼
FINAL ANSWER
```

Each iteration helps the agent gather additional information before making its final decision.

---

# ReAct Prompting

The behavior of a ReAct agent is controlled through a carefully designed system prompt. The prompt instructs the model to think before acting, use only one tool at a time, wait for observations, and generate a final answer only after sufficient information has been collected.

Unlike standard prompting, ReAct prompting encourages structured reasoning and tool usage.

---

# Building the Agent Loop

The core of a ReAct Agent is the agent loop.

During every iteration, the following steps occur:

1. Send the conversation history to the language model.
2. Read the model's reasoning.
3. Check whether the model requested a tool.
4. Execute the selected tool.
5. Return the observation to the model.
6. Repeat the process until the model generates a final answer.

This loop enables the agent to solve multi-step problems instead of relying on a single model response.

---

# Tool Integration

The language model never executes tools directly.

Instead, it produces structured outputs indicating which tool should be used and what arguments should be passed. Our Python application executes the requested tool, collects the observation, and sends it back to the model for the next reasoning step.

This separation ensures that the model focuses on reasoning while the application handles execution.

---

# Advantages of ReAct

- Solves multi-step problems.
- Supports external tools and APIs.
- Produces more reliable responses.
- Enables iterative reasoning.
- Forms the foundation of modern AI agent frameworks.

---

# Summary

In this module, we built a ReAct Agent completely from scratch and explored how iterative reasoning enables AI systems to solve complex problems. We learned how the model alternates between reasoning and actions, how tools are integrated into the reasoning process, and how observations guide the next decision.

We also implemented the complete agent loop ourselves, allowing the language model to repeatedly think, select tools, observe results, and continue until it generated the final answer. This architecture closely resembles the internal workflow of many modern AI agent frameworks while giving us complete control over every step.

Understanding the ReAct loop is an essential milestone in Agentic AI because it demonstrates how autonomous agents reason and interact with external systems. In the next module, we'll go one step further by tracing every iteration, analyzing token usage, measuring costs, and understanding the challenges of **Context Engineering** in long-running AI agents.