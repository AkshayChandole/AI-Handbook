# [What is hallucination?](#What-is-hallucination)



## ✅ What is Hallucination in LLMs?

**Hallucination is when a language model generates information that sounds correct and confident but is factually incorrect, fabricated, or not grounded in reality.**

In simple words:

> The model makes things up.

---

## 🔹 Why Do LLMs Hallucinate?

Because LLMs:

* Do not “know” facts
* Do not access real-time truth (unless connected to tools)
* Only predict the next most probable token

They generate responses based on learned probability patterns, not verified knowledge.

---

## 🔹 Example

Prompt:

> Who won the Nobel Prize in Physics in 2025?

If the model was trained only up to 2023, it may:

* Invent a name
* Give a confident but fake answer

That’s hallucination.

---

## 🔹 Types of Hallucination

### 1️⃣ Factual Hallucination

Incorrect facts.

### 2️⃣ Citation Hallucination

Fake references or research papers.

### 3️⃣ Logical Hallucination

Wrong reasoning steps.

### 4️⃣ Fabricated Details

Invented statistics, dates, names.

---

## 🔹 Root Causes

1. Probabilistic next-token prediction
2. Lack of grounding in external data
3. Over-generalization from training patterns
4. Insufficient context
5. Ambiguous prompts

---

## 🔹 How to Reduce Hallucination?

#### ✅ 1. Use RAG (Retrieval Augmented Generation)

Ground model using real documents.

#### ✅ 2. Lower Temperature

Reduce randomness.

#### ✅ 3. Better Prompting

Ask model to cite sources.

#### ✅ 4. Fine-Tuning

Domain-specific training.

#### ✅ 5. Tool Integration

Connect model to:

* Databases
* APIs
* Search engines

---

## 🔹 Important Insight

LLMs are not designed to say:

> "I don't know"

They are trained to produce the most probable continuation.

So they may prefer:

> A plausible answer
> instead of
> Admitting uncertainty

---

## 🎯 Interview Answer

> Hallucination occurs when a language model generates incorrect or fabricated information while sounding confident. It happens because LLMs predict the next token based on probability rather than verified facts. Hallucination can be reduced using retrieval augmentation, better prompting, lower temperature, and grounding the model in external data.


> Hallucination is fundamentally a misalignment between probability and truth — the model optimizes for likely text, not factual correctness.

---
