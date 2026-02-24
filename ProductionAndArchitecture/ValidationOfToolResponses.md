
# [How do you validate tool responses?](#How-do-you-validate-tool-responses)



## ✅ How Do You Validate Tool Responses?

Tool response validation ensures:

> The response is correct, safe, expected, and usable before passing it back to the model or user.

Validation happens in multiple layers.

---

## 🔹 1️⃣ Schema Validation (First Layer – Mandatory)

Every tool must have a **strict output schema**.

Example schema:

```json
{
  "type": "object",
  "properties": {
    "temperature": { "type": "number" },
    "unit": { "type": "string" }
  },
  "required": ["temperature", "unit"]
}
```

When tool responds:

```json
{
  "temperature": 32,
  "unit": "C"
}
```

Backend validates:

✔ Correct type
✔ Required fields present
✔ No unexpected fields

If invalid → reject.

---

## 🔹 2️⃣ Data Type & Range Validation

Even if schema matches, validate logical constraints:

* Temperature must be within realistic bounds
* Price must be non-negative
* Date must not be future (if not allowed)

Example:

```id="8nfw21"
temperature = 5000°C → invalid
```

Schema passed, but logically wrong.

---

## 🔹 3️⃣ Source Verification

Ensure tool data is:

* From trusted source
* Not tampered
* API returned success status (200 OK)
* Authenticated

Never pass raw error messages to model.

---

## 🔹 4️⃣ Sanitization Before Reinjecting to LLM

If tool returns:

* HTML
* SQL strings
* Script-like content
* Sensitive info

Sanitize before adding to prompt.

This prevents:

* Prompt injection
* Context poisoning

---

## 🔹 5️⃣ Business Rule Validation

Example:

If tool returns:

> User balance: -$10,000

Business logic may reject:

* Impossible states
* Fraud indicators
* Policy violations

---

## 🔹 6️⃣ Cross-Validation (Optional Advanced)

For critical systems:

* Call second tool for verification
* Validate against cached data
* Use validator agent

Example:

* Financial systems
* Medical systems

---

## 🔹 7️⃣ Confidence & Consistency Check

Check:

* Does output contradict prior memory?
* Does it conflict with previous tool results?

If inconsistent → trigger reflection or retry.

---

## 🔹 8️⃣ Error Handling Strategy

Handle:

* Tool timeout
* Partial response
* API failure
* Malformed JSON

Options:

* Retry
* Fallback tool
* Ask user clarification
* Escalate to human

---

## 🔹 9️⃣ Logging & Observability

Always log:

* Tool input
* Tool output
* Validation result
* Rejection reason

Important for debugging agent workflows.

---

## 🔹 🔟 Security Validation

Ensure:

* Tool cannot execute arbitrary commands
* Tool arguments are sanitized
* No privilege escalation
* Rate limits enforced

---

## 🔹 Example Full Flow

```
1. LLM requests tool call
2. Backend validates schema
3. Tool executes
4. Response validated against schema
5. Business rules applied
6. Sanitized output injected into prompt
7. Final response generated
```

---

## 🎯 Interview Answer

> I validate tool responses using strict schema validation, logical constraint checks, and business rule enforcement before reinjecting the data into the model. I sanitize outputs to prevent prompt injection, verify source authenticity, and handle failures through retries or fallbacks. In production systems, tool validation is treated like API contract enforcement to ensure safety and reliability.

> Tool validation is essentially enforcing deterministic contracts between probabilistic models and external infrastructure.

---
