
# [What is RAG?](#what-is-rag)

## ✅ What is RAG (Retrieval-Augmented Generation)?

**RAG is a technique that improves LLM responses by retrieving relevant external information and providing it to the model before generating an answer.**

Instead of relying only on training data, the model is grounded using real documents.

---

## 🔹 Why Do We Need RAG?

LLMs:

* Have limited knowledge cutoff
* Hallucinate
* Don’t know private/company data
* Cannot access real-time info

RAG solves this by:

> Retrieve relevant data → Add to prompt → Generate grounded answer

---

## 🔹 How RAG Works (Step-by-Step)

#### 1️⃣ User Query

```
"What is our company leave policy?"
```

#### 2️⃣ Convert Query to Embedding

Query → vector representation

#### 3️⃣ Search in Vector Database

Find similar documents using cosine similarity.

#### 4️⃣ Retrieve Relevant Documents

Example:

* Leave policy PDF chunk
* HR document section

#### 5️⃣ Augment Prompt

LLM receives:

```
Context:
[Retrieved company leave policy text]

Question:
What is our company leave policy?
```

#### 6️⃣ Generate Final Answer

Model answers using retrieved content.

---

## 🔹 Architecture Components

* Embedding Model
* Vector Database (FAISS, Pinecone, etc.)
* Retriever
* LLM
* Prompt Template

---

## 🔹 Why RAG Reduces Hallucination

Because:

* Model answers using retrieved documents
* Grounded in actual data
* Less guessing

---

## 🔹 When to Use RAG?

* Enterprise chatbots
* Knowledge base Q&A
* Legal document assistants
* Engineering documentation
* Private company data systems

---

## 🔹 RAG vs Fine-Tuning

| RAG                     | Fine-Tuning      |
| ----------------------- | ---------------- |
| No weight updates       | Updates weights  |
| Dynamic data            | Static knowledge |
| Works with private docs | Needs retraining |
| Easier to maintain      | Expensive        |

In production systems → RAG is preferred.

---

## 🎯 45-Second Interview Answer

> RAG, or Retrieval-Augmented Generation, is a technique where we retrieve relevant documents from an external knowledge base and provide them to the LLM as context before generating a response. This grounds the model in factual information, reduces hallucination, and allows it to answer questions about private or real-time data without retraining the model.




> RAG separates knowledge storage from reasoning — embeddings handle retrieval, and the LLM handles generation.

---



