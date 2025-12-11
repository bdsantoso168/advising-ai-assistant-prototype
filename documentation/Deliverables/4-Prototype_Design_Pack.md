# AI Advising Assistant — Prototype Design Pack

**Anonymized & Portfolio-Ready Version**

---

## 1. Overview

This document presents the design of an **AI-powered advising assistant prototype** developed for a university’s academic support environment.

The prototype demonstrates how AI can streamline routine advising interactions, reduce administrative workload, and improve student access to timely information — using **no-code LLM tools** and a structured knowledge base.

All content in this document is anonymized and generalized.

---

## 2. System Goals

The solution aims to:

* Provide **consistent, accurate, and policy-aligned** responses for common advising questions
* Reduce advisor workload by addressing **high-volume, low-complexity** inquiries
* Offer 24/7 access to academic guidance and campus resources
* Escalate nuanced or complex situations to a human advisor with context
* Demonstrate a scalable and modular AI architecture that can be expanded in future phases

---

## 3. High-Level Architecture (Conceptual)

Below is the conceptual architecture describing how the assistant processes, retrieves, and generates information.

```
User → LLM Interface → Intent Classifier → Knowledge Retrieval Layer → Response Generator → User
```

### **3.1 Components**

#### **A. LLM Front-End Interface**

* Web-based chat UI powered by a no-code AI builder
* Handles user queries, message formatting, and user session state

#### **B. Intent Classifier**

* Identifies which advising domain (e.g., degree planning, registration, policies) the question belongs to
* Routes ambiguous queries to clarifying prompts

#### **C. Knowledge Retrieval Layer (RAG-Lite)**

* Searches curated knowledge chunks
* Returns context to the model for grounded responses
* Includes general policies only — no confidential institutional data

#### **D. Response Generator**

* LLM generates responses using:

  * KB chunks
  * Guardrail prompts
  * Response style guides

#### **E. Escalation Layer**

Triggers referral messages when:

* The question requires personalized advising
* The question touches financial, immigration, or confidential issues
* The assistant is uncertain

---

## 4. Detailed Diagram (Text Version)

To be replaced by an image diagram (optional).
This text structure is safe for GitHub.

```
                         ┌───────────────────────────┐
                         │        User Query         │
                         └──────────────┬────────────┘
                                        │
                         ┌──────────────▼────────────┐
                         │     LLM Front-End UI      │
                         └──────────────┬────────────┘
                                        │
                         ┌──────────────▼────────────┐
                         │     Intent Classifier      │
                         └──────────────┬────────────┘
                                        │
                         ┌──────────────▼────────────┐
                         │ Knowledge Retrieval Layer │
                         │    (Chunk-based RAG)      │
                         └──────────────┬────────────┘
                                        │
                         ┌──────────────▼────────────┐
                         │     Response Generator     │
                         └──────────────┬────────────┘
                                        │
                         ┌──────────────▼────────────┐
                         │  Advisor Escalation Logic │
                         └──────────────┬────────────┘
                                        │
                         ┌──────────────▼────────────┐
                         │         Final Output       │
                         └────────────────────────────┘
```

If you'd like, I can generate a **DALL·E diagram** version of this later.

---

## 5. System Prompt & Guardrail Strategy

### **5.1 System Prompt Principles**

The assistant is instructed to:

* Provide general guidance only
* Avoid individualized advising decisions
* Redirect sensitive topics to human advisors
* Use clear, student-friendly explanations
* Ground all answers in the knowledge base
* Never invent policies or official rules

---

### **5.2 Guardrail Examples**

**Guardrail 1 – Avoid Personalized Academic Advice**

> “I can provide general information, but for personalized recommendations about your course plan, please speak with an academic advisor.”

**Guardrail 2 – High-Risk Topics**
Automatically escalate if user asks about:

* Immigration/visa compliance
* Financial aid consequences
* Academic standing or warnings
* Legal disputes or appeals

**Guardrail 3 – Data Safety**
Assistant must not store or access personal data.

---

## 6. Conversation Flow Design

### **6.1 Greeting & Clarification**

Example:

> “Hi! I can help with general advising questions. What would you like to know?”

If intent unclear:

> “Just to clarify, are you asking about registration, degree planning, or academic policies?”

---

### **6.2 Retrieval & Response Construction**

Steps:

1. Detect intent
2. Retrieve relevant KB chunks
3. Generate answer using templates
4. Apply guardrails
5. Provide next steps or escalation

---

### **6.3 Escalation Flow**

If escalation required:

```
Assistant → Provide general info → Explain limitation → Refer to advisor → Link appointment system (fictional)
```

Example:

> “This topic depends on your individual academic record, so I’m unable to give specific guidance. Please contact an advisor using the scheduling tool.”

---

## 7. UX Writing Style Guide (Used in Prototype)

* Use short paragraphs and clear explanations
* Assume the user may be new to academic systems
* Encourage self-service but provide links when appropriate
* Never overload user with long text blocks
* Always end responses with **one actionable next step**

---

## 8. Stress Testing & Quality Assurance

A series of test prompts (fictionalized) were used to evaluate:

* Intent detection accuracy
* Clarity of responses
* Behavior under ambiguous or multi-part questions
* Guardrail activation reliability
* Handling of out-of-scope topics

### **Testing Categories**

| Test Type               | Purpose                           | Example                                                 |
| ----------------------- | --------------------------------- | ------------------------------------------------------- |
| **Boundary Tests**      | Ensure reject/redirect works      | “How many credits do *I personally* need to graduate?”  |
| **Ambiguity Tests**     | Check clarifying responses        | “Can I take this course?”                               |
| **Hallucination Tests** | Prevent creation of fake policies | “What’s the maximum GPA penalty for late registration?” |
| **Stress Tests**        | Multiple intents at once          | “I can’t register, also how many credits is full-time?” |

---

## 9. Future Development Roadmap

### **Phase 1 — Enhanced RAG Pipeline**

* Embeddings-based retrieval
* Chunk-level metadata
* Confidence scoring

### **Phase 2 — Personalized Features (Secure Mode)**

* Connect to student profile via authorized APIs
* Automatic detection of scheduling issues
* Program audit summaries

### **Phase 3 — Multilingual Support**

* Support for international student queries
* Simplified English mode

### **Phase 4 — Expanded Use Cases**

* Financial literacy & administrative FAQs
* Campus services
* Student life workflows
* Faculty onboarding support

---

## 10. Ethical & Compliance Considerations

* No personal data is processed in prototype
* Advising recommendations remain non-binding
* High-risk categories redirect to qualified staff
* System avoids legal, medical, or immigration opinions
* AI usage follows transparency guidelines (user informed AI is used)

---

*This anonymized Prototype Design Pack demonstrates the workflow, architecture, and logic of an advising AI assistant for academic environments. It is intended for educational, portfolio, and research purposes only.*
