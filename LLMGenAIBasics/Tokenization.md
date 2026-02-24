# [What is tokenization?](#What-is-tokenization?)

## ✅ What is Tokenization?

**Tokenization** is the process of breaking raw text into smaller units called **tokens**, which a language model can process.

Since models cannot understand raw text directly, we convert text into numerical tokens before feeding it into the model.

---

## 🔹 Why Do We Need Tokenization?

Neural networks operate on numbers, not strings.

So we must convert:

```
"I love AI"
```

Into something like:

```
[154, 892, 4210]
```

Each number represents a token ID from the model’s vocabulary.

---

## 🔹 Types of Tokenization

### 1️⃣ Word-Level Tokenization

Splits text by words.

```
"I love AI"
→ ["I", "love", "AI"]
```

❌ Problem: Huge vocabulary size.

---

### 2️⃣ Character-Level Tokenization

Splits into characters.

```
"I love"
→ ["I", " ", "l", "o", "v", "e"]
```

❌ Problem: Too many tokens, longer sequences.

---

### 3️⃣ Subword Tokenization (Used in LLMs ✅)

Most modern LLMs use subword techniques like:

* BPE (Byte Pair Encoding)
* WordPiece
* SentencePiece

Example:

```
"unbelievable"
→ ["un", "believ", "able"]
```

This reduces vocabulary size while handling rare words.

---

## 🔹 What Happens Internally?

1. Text → split into tokens
2. Each token → mapped to integer ID
3. IDs → converted into embeddings
4. Model processes embeddings

---

## 🔹 Example

Input:

```
"ChatGPT is powerful"
```

Tokenized as:

```
["Chat", "G", "PT", " is", " powerful"]
```

Converted to:

```
[5432, 88, 921, 102, 7788]
```

Then fed into the model.

---

## 🔹 Important Interview Concepts

#### 🔸 Vocabulary

Predefined list of all possible tokens.

#### 🔸 Context Length

More tokens = more memory usage.

#### 🔸 Special Tokens

* `<BOS>` (Beginning of sentence)
* `<EOS>` (End of sentence)
* `<PAD>` (Padding)
* `<UNK>` (Unknown token)

---

## 🎯 30-Second Interview Answer

> Tokenization is the process of converting raw text into smaller units called tokens, which are then mapped to numerical IDs so a language model can process them. Modern LLMs use subword tokenization techniques like BPE or WordPiece to efficiently handle vocabulary size and rare words.

---
