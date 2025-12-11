# Advising AI Assistant – Discovery Packet (v1)

**Team:** AI Advising Assistant Project – Group 5
**Date:** September 2025
**Client Context:** Undergraduate Academic Advising Office at a business-focused university
**Instructor / Sponsor:** Course instructor for “AI for Business Bots”

---

## 1. Problem Statement

The university’s academic advising system is under pressure from:

* **Growing student diversity:** Many students are international, transfer, or first-generation and are unfamiliar with the local higher-education system.
* **Complex academic rules:** Degree requirements, elective options, prerequisite chains, and transfer credit rules are difficult to interpret from static documents.
* **Limited advising capacity:** Students often wait several days for basic questions to be answered, especially during registration and add/drop periods.
* **High stakes for errors:** Incorrect course selections can delay graduation, impact financial aid, or create issues with academic standing and enrollment status.

**Core problem:**
Students struggle to get timely, accurate answers to *high-frequency, low-complexity* questions, while advisors are overloaded with repetitive inquiries instead of spending time on complex, high-value conversations.

---

## 2. Project Goal

Design and prototype an **AI-powered advising assistant** that:

1. Handles routine, policy-based advising questions 24/7.
2. Guides students toward appropriate resources (website pages, forms, offices).
3. Escalates complex or high-risk cases to human advisors with context.
4. Reduces advisor workload while improving the student experience.

The project focuses on **no-code / low-code LLM tooling**, with emphasis on:

* Knowledge-base design and chunking
* Prompt and conversation-flow design
* Guardrails and escalation logic
* Clear documentation for future iteration

---

## 3. Target Users & Personas

### 3.1 Primary User Personas

1. **New International / Transfer Student**

   * Needs help understanding program structure, transfer credits, and course sequence.
   * Frequently confused by terminology and system navigation.

2. **Continuing Student Planning Upcoming Semester**

   * Needs to confirm prerequisites, course combinations, and graduation progress.
   * Wants quick answers during registration rush.

3. **Student with Academic Risk or Edge Cases**

   * On academic warning / probation or has unusual credit history.
   * May require escalation to an advisor for nuanced decisions.

### 3.2 Internal Stakeholders

* **Advisors & Program Coordinators:** Need reduced volume of repetitive queries and better-prepared students in appointments.
* **Academic Leadership:** Interested in student satisfaction, time-to-degree, and more consistent communication of policies.
* **IT / Data Owners:** Responsible for integrating any future version with internal systems (if approved).

---

## 4. Scope for Prototype (Semester Project)

**In scope:**

* Design of conversation flows for common advising scenarios
* Creation and structuring of a *sample* advising knowledge base
* Prompt templates and system instructions for the AI assistant
* Guardrail rules (when to stop, when to escalate)
* No-code implementation using an LLM platform and web demo link
* Documentation of assumptions, limitations, and risks

**Out of scope:**

* Direct integration with student records systems
* Real-time access to official degree audits
* Automated changes to enrollment or records
* Formal policy changes or official advising decisions

---

## 5. High-Priority Use Cases

The team identified several **high-frequency question clusters** the assistant should support in a first version:

### Use Case 1 – Degree Planning & Course Sequencing

* Understanding recommended course order within a major or concentration
* Checking prerequisites and co-requisites
* Exploring how many remaining courses are needed for graduation (at a high level)

### Use Case 2 – Transfer & Prior Credit Interpretation

* How previously completed courses may apply to the current degree plan
* General rules for maximum transferable credits
* Guidance on which office to contact for official evaluations

### Use Case 3 – Registration & System Navigation

* Troubleshooting common registration errors (time conflicts, missing prerequisites, holds)
* Explaining key dates (add/drop periods, withdrawal deadlines)
* Guiding students to correct forms and portals

### Use Case 4 – Policy & Academic Standing Clarification

* General explanations of full-time / part-time status definitions
* High-level overview of academic standing categories
* When to speak directly with an advisor or another office (e.g., financial aid)

**Note:** The assistant is designed to give **general guidance only**, not make binding decisions.

---

## 6. Success Metrics (Prototype Level)

The prototype will be considered successful if it can:

1. Correctly interpret user intent and route to the appropriate knowledge chunk **for a curated set of test questions**.
2. Provide answers that are:

   * **Accurate** at a general-policy level
   * **Consistent** with the documented knowledge base
   * **Clear** and understandable to non-expert students
3. Demonstrate guardrails such as:

   * Stopping when information is uncertain
   * Encouraging students to contact an advisor for complex cases
   * Avoiding personalized academic or legal advice
4. Be usable in a short demo session by:

   * Student testers (peers)
   * The instructor and internal stakeholders

---

## 7. Constraints & Assumptions

* The assistant operates on **sample, anonymized knowledge content**, not live institutional systems.
* All data used in this prototype is either:

  * Public, high-level academic information, or
  * Fictional content created solely for demonstration.
* The assistant must **not**:

  * Access or store real student records
  * Make binding commitments about graduation eligibility or financial aid
  * Give immigration, legal, or medical advice
* Implementation will favor **no-code platforms** so the focus is on:

  * Conversation design
  * Knowledge structuring
  * Prompt and guardrail quality

---

## 8. Risks & Guardrails

### Key Risks

* Misinterpretation of ambiguous questions
* Over-confidence in responses when information is incomplete
* Misuse of the assistant for questions outside its scope

### Guardrail Strategies

* System prompt clearly stating scope and limitations
* Explicit escalation phrases such as:
  “For this situation, please speak with an academic advisor.”
* Categorization of **“high-risk topics”** (e.g., academic standing, financial or immigration-related implications), which always trigger escalation or cautious guidance.
* Logging of example interactions (in test mode) to refine prompts and knowledge chunks.

---

## 9. Next Steps (From Discovery to Design)

1. **Refine use-case list** into 3–4 core flows for the prototype.
2. **Create a structured knowledge base**:

   * Categories (e.g., degree planning, registration, policies)
   * Individual chunks summarized in student-friendly language
3. **Design conversation flows** for each use case:

   * Greeting and intent detection
   * Clarifying questions
   * Response templates
   * Escalation and wrap-up
4. **Implement a first iteration** using a no-code LLM platform.
5. **Run stress tests** with sample questions and document:

   * Successes
   * Failure modes
   * Improvement ideas for a future version.

---

*This document is an anonymized, high-level summary of the discovery work for an academic advising AI assistant. It is intended for portfolio and educational purposes only and does not represent any specific institution’s official advising policies.*
