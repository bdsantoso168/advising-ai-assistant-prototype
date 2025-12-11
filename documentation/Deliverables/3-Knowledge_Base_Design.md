# Knowledge Base Design & Chunking Blueprint

**AI Advising Assistant – Anonymized Documentation**
*For Portfolio and Public GitHub Use*

---

## 1. Purpose of the Knowledge Base (KB)

The Knowledge Base provides structured, domain-specific information that enables the AI assistant to:

* Deliver **consistent**, **policy-aligned**, and **easy-to-understand** answers
* Improve accuracy by grounding LLM responses in curated content
* Reduce hallucinations through retrieval-augmented generation (RAG) patterns
* Support future expansion into additional academic or administrative areas

This KB contains **fictional examples and generalized academic information**, not tied to any specific institution.

---

## 2. Principles Used in KB Design

### **2.1. High-Level, Non-Binding Information Only**

The KB avoids:

* Confidential advising rules
* Personalized degree decisions
* Legal, financial, or immigration implications

Only general, safe, and widely applicable academic concepts are included.

---

### **2.2. Student-Friendly Writing Style**

All chunks follow these guidelines:

* Use **plain language**, avoiding bureaucratic terminology
* Keep chunks **short**, **scannable**, and **context-independent**
* Begin with **summary statements** before details
* Include **“when to seek an advisor”** escalation triggers

---

### **2.3. Modular Chunk Structure**

Each chunk represents a **single concept**.

This improves:

* Retrieval accuracy
* Intent-to-chunk mapping
* Scalability (easy to add or modify sections)

---

## 3. KB Architecture Overview

The project team defined the KB using a **three-tier structure**:

### **Tier 1 – Category (Macro Intent Area)**

Represents broad advising topics.
Examples: Course Planning · Registration · Policies · Transfer Credit · Student Support · Admin Processes

---

### **Tier 2 – Subcategory (Topic Group)**

Breaks large areas into logical clusters.
Example under Course Planning:

* Prerequisites
* Co-requisites
* Degree Requirements
* Typical Course Paths

---

### **Tier 3 – Chunk (Atomic Unit of Knowledge)**

Each chunk covers a single concept such as:

* "What is a prerequisite?"
* "General definition of full-time status"
* "What is a waitlist?"
* "When to escalate to an advisor?"

Each chunk is standalone.

---

## 4. Chunk Template (Used for All Entries)

Every chunk follows the standard format:

```
Chunk ID: <unique identifier>
Category: <high-level area>
Subcategory: <topic>
Summary: <2–3 sentence overview>
Details: <expanded explanation, examples, disclaimers>
When to Escalate: <conditions requiring advisor interaction>
```

This template ensures clarity and uniformity.

---

## 5. Example KB Chunks (Fictional & Safe)

Below are **sample anonymized chunks** demonstrating structure, tone, and content.
These **do not represent any real institution’s policies**.

---

### **Chunk CP-01: Prerequisite Definition**

**Category:** Course Planning
**Subcategory:** Prerequisites

**Summary:**
A prerequisite is a course or requirement that must be completed before enrolling in another course.

**Details:**
Prerequisites ensure that students have the foundational knowledge needed to succeed in higher-level coursework.
If a student attempts to register for a course without meeting the prerequisite, the system may prevent enrollment.

**When to Escalate:**
If a student believes they completed an equivalent course elsewhere or has unique circumstances requiring an exception.

---

### **Chunk CP-04: Typical Course Path Overview**

**Category:** Course Planning
**Subcategory:** Degree Planning

**Summary:**
Many programs follow a recommended progression that spreads foundational, intermediate, and advanced courses across multiple semesters.

**Details:**
A typical path includes introductory courses early on, skill-building courses in the middle semesters, and capstone or specialization courses near the end.
This structure helps balance workload and prepare students for advanced topics.

**When to Escalate:**
When a student has transfer credits, accelerated timelines, or academic standing considerations.

---

### **Chunk RG-02: Registration Time Conflict**

**Category:** Registration
**Subcategory:** Troubleshooting

**Summary:**
A time conflict occurs when two classes overlap or occur too close together.

**Details:**
Most systems require that classes fully avoid overlapping time blocks to ensure attendability.
Even small overlaps can prevent registration.

**When to Escalate:**
If the student needs guidance on finding alternative sections or understands the conflict but still cannot register.

---

### **Chunk AP-03: Full-Time Status**

**Category:** Academic Policies
**Subcategory:** Enrollment Status

**Summary:**
Full-time enrollment generally means taking a minimum number of credits per semester.

**Details:**
Many institutions define full-time status as 12 or more credits for undergraduate students.
This may impact financial aid, billing, and academic progress.

**When to Escalate:**
If the student has questions involving financial aid, billing impacts, or legal/visa matters.

---

### **Chunk TC-01: Transfer Credit – General Rules**

**Category:** Transfer Credit
**Subcategory:** Overview

**Summary:**
Transfer credits represent coursework completed at another institution that may apply toward a degree.

**Details:**
Universities evaluate course content, accreditation, and relevance before determining how credits apply.
Students typically submit transcripts for a formal evaluation.

**When to Escalate:**
For course-specific equivalency decisions or individual evaluations.

---

### **Chunk SR-05: Academic Support Resources**

**Category:** Student Resources
**Subcategory:** Support Services

**Summary:**
Universities offer tutoring, academic coaching, writing support, and other services to help students succeed.

**Details:**
Support services often include group workshops, one-on-one tutoring, writing center consultations, and specialized support for certain subjects.

**When to Escalate:**
If a student needs personalized academic planning or accommodations.

---

## 6. Chunking Rules Used in the Prototype

### **Rule 1 — Each chunk covers one idea only**

No combined concepts such as “prerequisites + co-requisites”.

### **Rule 2 — Chunks must be independent**

A chunk should be fully understandable without viewing any other chunk.

### **Rule 3 — Use short chunks (100–180 words)**

Supports accurate retrieval in RAG.

### **Rule 4 — Include escalation logic in every chunk**

Protects the assistant from giving overconfident or inappropriate guidance.

### **Rule 5 — No institution-specific data**

All wording is general and academically universal.

---

## 7. Future Enhancements

### Recommended next steps for improving the KB:

* Expand chunks into multilingual versions
* Add metadata tags (e.g., difficulty, student level, risk category)
* Use embeddings for vector-based retrieval
* Create automated tests to check for hallucinations
* Add “not-sure” responses for ambiguous queries

---

*This document is an anonymized blueprint demonstrating how knowledge-base chunking can support a higher-education advising AI assistant. It is generated for instructional and portfolio purposes only.*
