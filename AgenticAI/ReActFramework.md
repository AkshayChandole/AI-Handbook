
# [What is ReAct framework?](#What-is-ReAct-framework)

## ✅ What is the ReAct Framework?

**ReAct stands for “Reason + Act.”**

It is a framework for building AI agents where the model:

> **Reasons about a problem step-by-step and then takes actions (like calling tools), in an iterative loop.**

Instead of just generating a final answer, the model alternates between:

* 🧠 Reasoning (Thought)
* 🛠 Acting (Tool call)
* 👀 Observing (Tool result)

---

## 🔹 Why ReAct Was Introduced

Traditional LLMs:

* Either reason internally
* Or call tools blindly

ReAct combines both:
✔ Structured reasoning
✔ Tool usage
✔ Iterative improvement

This reduces hallucination and improves reliability.

---

## 🔹 Core Loop of ReAct

The pattern looks like:

```
Thought: I need to find the current weather.
Action: Call weather API
Observation: Weather is 32°C
Thought: Now I can answer the user.
Final Answer: It is currently 32°C.
```

This Think → Act → Observe loop continues until task is completed.

---

## 🔹 Step-by-Step Flow

1️⃣ User gives query
2️⃣ Model generates reasoning step
3️⃣ Model decides which tool to use
4️⃣ Tool executes
5️⃣ Result is fed back to model
6️⃣ Model reasons again
7️⃣ Final answer generated

---

## 🔹 Example

User:

> What is the square root of the current temperature in Mumbai?

ReAct Agent:

```
Thought: I need current temperature.
Action: Call weather API
Observation: 36°C
Thought: Now compute square root of 36.
Action: Call calculator
Observation: 6
Final Answer: The answer is 6.
```

Without ReAct → LLM might hallucinate temperature.

---

## 🔹 Benefits of ReAct

✔ Reduces hallucination
✔ Enables multi-step reasoning
✔ Makes decision process transparent
✔ Supports tool integration
✔ Improves task accuracy

---

## 🔹 ReAct vs Chain-of-Thought

| Chain-of-Thought    | ReAct             |
| ------------------- | ----------------- |
| Reasoning only      | Reason + Tool Use |
| No external actions | Calls tools       |
| Internal thinking   | Interactive loop  |

---

## 🔹 Where It’s Used

* Autonomous AI agents
* Tool-using LLM systems
* Research assistants
* Enterprise automation agents

---

## 🎯 40-Second Interview Answer

> The ReAct framework stands for Reason and Act. It is an agentic AI approach where the model alternates between reasoning steps and tool-based actions in a loop. The model generates a thought, performs an action like calling an API, observes the result, and then continues reasoning until it produces the final answer. This improves reliability and reduces hallucination.




> ReAct externalizes part of the model’s reasoning into observable steps, enabling structured tool use and better control over autonomous behavior.

---

