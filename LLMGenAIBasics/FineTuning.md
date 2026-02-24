# [What is fine-tuning?](#What-is-fine-tuning)


## ✅ What is Fine-Tuning?

**Fine-tuning is the process of taking a pre-trained model and training it further on a smaller, task-specific dataset to adapt it to a particular problem.**

Instead of training from scratch, we reuse the knowledge the model already learned.

---

## 🔹 Why Fine-Tuning Is Needed?

Training large models from scratch:

* Requires massive data
* Requires huge compute
* Takes weeks or months

So we:

1. Start with a pretrained model (like an LLM trained on internet text)
2. Train it further on domain-specific data

Example:

* Base model → general knowledge
* Fine-tuned model → medical chatbot / coding assistant / CAD assistant

---

## 🔹 How It Works Internally

1. Load pretrained weights
2. Provide labeled or task-specific data
3. Compute loss on new data
4. Backpropagate gradients
5. Update weights slightly

The model adjusts its parameters to specialize.

---

## 🔹 Example

Base model:

> Can answer general questions.

After fine-tuning on legal documents:

> Becomes better at legal Q&A.

---

## 🔹 Types of Fine-Tuning

### 1️⃣ Full Fine-Tuning

All model parameters are updated.

### 2️⃣ Parameter-Efficient Fine-Tuning (PEFT)

Only small parts of model are trained.
Examples:

* LoRA
* Adapters
* Prefix tuning

This reduces memory and compute cost.

---

## 🔹 Fine-Tuning vs Prompting

| Fine-Tuning           | Prompt Engineering    |
| --------------------- | --------------------- |
| Changes model weights | No weight changes     |
| Permanent improvement | Temporary instruction |
| Needs training data   | Just better prompts   |

---

## 🔹 When Do We Use Fine-Tuning?

* Domain adaptation
* Style adaptation
* Instruction following
* Custom behavior
* Improving accuracy on specific tasks

---

## 🎯 30-Second Interview Answer

> Fine-tuning is the process of taking a pretrained model and training it further on a smaller, task-specific dataset to adapt it for a particular use case. Instead of training from scratch, we update the model’s weights slightly so it becomes specialized while retaining its general knowledge.

---
