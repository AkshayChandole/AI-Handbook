
# [What is reflection in agents?](#What-is-reflection-in-agents)

## ✅ What is Reflection in AI Agents?

**Reflection is a technique where an AI agent reviews its own previous reasoning or actions, identifies mistakes, and improves its future decisions.**

In simple terms:

> The agent thinks about its own thinking.

It’s like self-correction.

---

## 🔹 Why Is Reflection Needed?

Agents can:

* Make wrong assumptions
* Use wrong tools
* Follow poor reasoning paths
* Get stuck in loops

Reflection allows the agent to:

✔ Detect mistakes
✔ Revise strategy
✔ Improve accuracy
✔ Learn from failure

---

## 🔹 How Reflection Works

Typical flow:

1️⃣ Agent attempts solution
2️⃣ Produces intermediate reasoning
3️⃣ Evaluates its own output
4️⃣ Identifies flaws
5️⃣ Regenerates improved reasoning

---

## 🔹 Simple Example

Problem:

> Solve 25 × 4

Agent mistakenly says 80.

Reflection step:

```
Let me verify.
25 × 4 = 100.
Correction: The answer is 100.
```

The agent self-corrects.

---

## 🔹 Reflection in Agent Loop

Enhanced loop becomes:

```
Think → Act → Observe → Reflect → Refine → Final Answer
```

Reflection adds an evaluation stage before finalizing output.

---

## 🔹 Types of Reflection

### 1️⃣ Immediate Reflection

Check reasoning before final answer.

### 2️⃣ Delayed Reflection

After task completion, analyze what worked and what failed.

### 3️⃣ Memory-Based Reflection

Store mistakes to avoid repeating them.

---

## 🔹 Reflection vs Chain-of-Thought

| Chain-of-Thought       | Reflection                 |
| ---------------------- | -------------------------- |
| Step-by-step reasoning | Evaluate reasoning quality |
| Linear thinking        | Self-evaluation            |
| Before answer          | After reasoning            |

---

## 🔹 Benefits

✔ Reduces hallucination
✔ Improves reasoning accuracy
✔ Enables adaptive learning
✔ Prevents repeated mistakes

---

## 🔹 Tradeoffs

* More computation
* More tokens
* Higher latency

---

## 🎯 Interview Answer

> Reflection in AI agents is the ability of the system to evaluate its own reasoning or actions and correct mistakes before producing a final answer. It adds a self-evaluation step in the agent loop, improving reliability and reducing errors in complex tasks.

> Reflection introduces meta-reasoning — the agent reasons not only about the task but also about the quality of its own reasoning.

---

