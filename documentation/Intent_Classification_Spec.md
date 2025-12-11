# Intent Classification Specification

**AI Advising Assistant – Intent & Utterance Categorization Framework**
*Anonymized Consulting Version*

---

## 1. Purpose of This Document

This document outlines a structured intent-classification model designed for an academic advising AI assistant prototype.
Its purpose is to:

* Define **core intent categories** the assistant must recognize
* Provide **sample anonymized student utterances** for training and testing
* Establish boundaries for **what the assistant can and cannot answer**
* Support future scaling into broader academic or administrative use cases

This version contains *fictional and generalized examples* suitable for public sharing.

---

## 2. Intent Category Framework

The project team identified **six primary intent domains** common across university advising scenarios. These domains capture high-volume, low-complexity topics that students frequently ask about.

### **Category A — Degree Planning & Course Sequencing**

Focus: Long-term academic progress, recommended course paths, prerequisite guidance.

**Example Utterances (Fictional):**

* “How should I sequence courses for my major?”
* “Can I take Course X and Course Y in the same semester?”
* “What do I still need to graduate?”
* “Is there a typical course plan for second-year students?”

---

### **Category B — Registration Troubleshooting**

Focus: Technical barriers and system-level errors students encounter during registration.

**Example Utterances (Fictional):**

* “The registration page says I’m missing a prerequisite.”
* “Why can’t I add a class even though seats are open?”
* “I’m getting a time conflict error—what does that mean?”
* “How do I join a waitlist?”

---

### **Category C — Academic Policies (General-Level)**

Focus: High-level explanations of institutional rules without giving legal or binding advice.

**Example Utterances (Fictional):**

* “What counts as full-time enrollment?”
* “What happens if I withdraw from a course?”
* “What’s the difference between pass/fail and letter grading?”
* “When is the last day to drop a class?”

**Guardrail Note:**
The assistant must avoid personalized academic standing guidance.

---

### **Category D — Transfer Credit & Prior Learning**

Focus: General interpretation of how outside credits may apply toward a degree.

**Example Utterances (Fictional):**

* “Can my community college course count toward this degree?”
* “How many transfer credits can I bring in?”
* “Where do I submit transcripts for evaluation?”

**Guardrail Note:**
The assistant must not confirm official transfer equivalencies or decisions.

---

### **Category E — Student Support Resources & Referrals**

Focus: Directing students to appropriate campus offices or tools.

**Example Utterances (Fictional):**

* “Who can I talk to about financial aid?”
* “Where do I get help with academic writing?”
* “Is there tutoring available for this course?”
* “How do I book an advising appointment?”

---

### **Category F — Administrative Processes & Forms**

Focus: Navigation of university systems and paperwork.

**Example Utterances (Fictional):**

* “How do I request an enrollment verification letter?”
* “Where do I find the form to change my major?”
* “What system do I use to check my academic status?”
* “How do I update my personal information?”

---

## 3. Out-of-Scope Intents

These questions must trigger escalation messages:

### 🔴 **Immigration / Visa Status**

* International student visa questions
* Work authorization inquiries

### 🔴 **Financial Aid, Billing, or Legal Advice**

* Cannot interpret financial or regulatory consequences

### 🔴 **Personalized Advising Decisions**

* “Tell me what classes I should take next semester.”
* “Am I on track to graduate?”
* “Should I drop this class?”

### 🔴 **Mental Health, Safety, or Wellness Issues**

Must direct to trained professionals.

---

## 4. Intent Detection Rules

### Rule 1 — Use Category-Level Response Logic

The assistant responds with a **high-level, general explanation**, not individualized decisions.

### Rule 2 — Identify High-Risk Keywords

Examples that require escalation:

* “CPT,” “visa,” “I-20,” “immigration”
* “probation,” “academic warning”
* “refund,” “billing,” “financial aid”

### Rule 3 — Always Provide a Next Step

The assistant must:

* Provide the general policy overview
* Link the user to the appropriate office or tool
* Recommend speaking with an advisor for personalized cases

---

## 5. Sample Intent Classification Table (Anonymized)

| Utterance Example                           | Classified Intent            | Notes                            |
| ------------------------------------------- | ---------------------------- | -------------------------------- |
| “What should I take first for this major?”  | Degree Planning              | Avoid personalized sequencing.   |
| “The system says I can’t register—why?”     | Registration Troubleshooting | Provide general reasons & steps. |
| “How many credits is full-time?”            | Academic Policies            | Keep general definitions only.   |
| “Can my overseas credits count here?”       | Transfer Credit              | Provide process, not decisions.  |
| “Where can I get tutoring?”                 | Student Support              | Direct to resources.             |
| “How do I request enrollment verification?” | Administrative Processes     | Link to form/process.            |

---

## 6. Testing Guidelines

### Success Criteria

An utterance is considered correctly classified when:

* It matches the appropriate category
* The assistant chooses the correct response template
* No protected or sensitive advice is provided

### Failure Modes to Monitor

* Overconfident academic or legal statements
* Misclassification between policy vs. registration
* Providing step-by-step instructions for internal systems beyond allowed scope

---

## 7. Future Recommendations

* Expand categories into sub-intents (e.g., prerequisites, co-requisites, graduation checks).
* Introduce pattern-based rejection responses for out-of-scope questions.
* Add multilingual support for international students.
* Integrate structured metadata for better RAG retrieval performance.

---

*This anonymized document reflects an intent classification model suitable for demonstrating conversational AI design principles in a higher-education context. All examples are fictional and generalized.*
