# 🎓 AI Advising Assistant – A Knowledge-Grounded Academic Advising Chatbot  
### A No-Code LLM Prototype Supporting Undergraduate Advising Across the Business School
<img width="1536" height="1024" alt="AI Banner for Project" src="https://github.com/user-attachments/assets/c0556aff-2e6f-4e57-af65-e6859bcaf5d5" />

## 🌟 Project Overview  
This repository documents the full design, development, and implementation of an **AI-powered advising assistant**, created as the capstone group project for **ISOM 360 – AI for Business Bots**. The goal was to build a safe, helpful, and policy-aligned chatbot to support undergraduate academic advising at a university’s business school.

According to the official project brief, the chatbot was intended to *“assist students in finding answers to curriculum and advising questions across different majors… and recognize its limitations while escalating to a human advisor when appropriate.”* :contentReference[oaicite:0]{index=0}

Our solution is built entirely using **no-code LLM tools (Custom GPT)** and a carefully structured knowledge base with guardrails. The prototype was successfully demonstrated to faculty and leadership at the end of the semester.

---

## 💡 Why We Built This Chatbot  
Undergraduate advising offices face the same recurring challenges every semester:

- Students struggle to interpret curriculum rules, prerequisites, workload expectations, and registration errors.  
- Advisors receive **hundreds of repetitive questions**—many simple and procedural.  
- International and transfer students face additional complexity navigating the American credit system, course sequencing, and platform terminology.  
- The advising office cannot always deliver 24/7 support, especially during peak registration periods.  

These challenges create:

- long wait times  
- inconsistent information across different communication channels  
- advisor burnout  
- students making preventable academic mistakes  

👉 Our mission was to design a scalable AI tool that supports both students *and* advisors by handling **high-frequency, low-complexity queries**, while escalating nuanced cases to humans.

---

## 🎯 Value Proposition  
### **For Students**  
- 24/7 access to accurate, easy-to-understand advising explanations  
- Clear guidance on registration, curriculum rules, and academic processes  
- Friendly, non-judgmental responses  
- Easier navigation of systems like Workday, program evaluations, and course planning  

### **For Advisors and the University**    
- Reduces repetitive workloads so advisors focus on complex conversations  
- Ensures consistent messaging aligned with official policy  
- Helps identify when escalation is required (overloads, academic standing, transfer evaluations, etc.)  
- Serves as a foundation for future expansion (personalized planning, multilingual support, integrations)  

---

## 🛠 How the Chatbot Works  
This prototype uses a **no-code architecture** built around four major components:

### **1. System-Level Instruction Set**  
A detailed instruction package defining:

- bot identity  
- scope (six advising categories)  
- tone & writing rules  
- allowed knowledge sources  
- escalation logic  
- safe completion model  
- out-of-scope templates  

This ensures consistent, guardrail-safe responses.

---

### **2. Knowledge Base (KB) — Chunked Micro-Documents**  
We created dozens of **small, modular knowledge chunks**, each covering:

- a single advising concept  
- student-friendly explanations  
- examples & definitions  
- when to escalate to a human advisor  
- official source citations  

This chunking strategy reduces hallucinations and improves retrieval accuracy.

---

### **3. Retrieval + Response Model**  
The assistant:

1. Detects category from user query  
2. Retrieves relevant micro-chunk  
3. Generates a student-friendly explanation  
4. Cites the policy source  
5. Adds next-step instructions  
6. Escalates when appropriate  

---

### **4. Conversation Starters & UX Layer**  
We added 12–18 curated example questions that appear on the chatbot’s homepage to guide new users toward common advising issues:

- “What does ‘waitlisted’ mean?”  
- “How do I change my major?”  
- “Why do I have a registration hold?”  
- “Can I take 18 credits next semester?”  

These reduce friction and help first-time users begin interacting immediately.

---

## 📘 Repository Structure  
This repository includes everything from the initial discovery phase to the final prototype demo.

## 📁 Repository Structure  

```
📦 root  
├─ 📂 documentation  
│  ├─ Intent_Classification_Spec.md  
│  ├─ Knowledge_Base_Design.md  
│  ├─ Prototype_Design_Pack.md  
│  ├─ Stress_Testing_Results.md  
│  │
│  ├─ 📂 deliverables  
│  │  ├─ Deliverable_1.md  
│  │  ├─ Deliverable_2.md  
│  │  ├─ Deliverable_3.md  
│  │  └─ Deliverable_4.md  
│  │
│  └─ 📂 implementation  
│     ├─ Phase-D_Instruction-Set.md  
│     ├─ Phase-E_Upload-Knowledge-Base.md  
│     ├─ Phase-F_Conversation-Starters.md  
│     └─ Prototype-Step-by-Step-Guide.md  
│
├─ 📂 project_output  
│  ├─ Final_Presentation.pdf  
│  └─ Chatbot_Demo_Link.md  
│
└─ 📂 media  
   ├─ 📂 diagrams  
   └─ 📂 thumbnails  
```

---

## 🚀 Live Demo  
Click below to try the **AI Advising Assistant Prototype**:

👉 **https://chatgpt.com/g/g-690d0d873cbc819199558d84c982e6a4-ram-adviser**

*(The live version uses anonymized content and safe guardrails.)*

---

## 🧪 Stress Testing & Evaluation  
After implementation, the bot underwent structured testing across:

- intent detection accuracy  
- ambiguity handling  
- boundary/guardrail compliance  
- hallucination prevention  
- multi-intent scenarios  

Results demonstrated strong safety performance, correct escalation behavior, and reliable retrieval grounded in the KB.

Full results here:  
➡ **documentation/Stress_Testing_Results.md**

---

## 🎤 Final Presentation  
The final version of the project was presented to:

- Faculty  
- Program leadership  
- The SBS Dean  

The audience responded positively to the bot’s clarity, structure, and escalation handling—particularly the KB design.  
The main feedback noted:

- Manual KB updates can be time-consuming  
- The prototype performs best under ChatGPT Plus (Free tier showed more hallucinations under long prompts)

Slides available here:  
📄 **/project_output/Final_Presentation.pdf**

---

## 🌱 Future Enhancements  
This prototype paves the foundation for a more advanced advising system with:

- personalized program tracking  
- real-time integration with student information systems  
- multilingual support for international students  
- advanced RAG pipelines with embeddings  
- advisor dashboard with summary logs  
- automated registration error explanation  

---

## 👥 Team & Contributions  
This project was completed as part of a semester-long collaboration in **ISOM 360 – AI for Business Bots**.

My contributions included:

- Knowledge Base design (chunking, structure, writing)  
- System-level prompt engineering  
- Conversation Starter design  
- Stress testing  
- Architecture documentation  
- Creating the final GitHub documentation  
- Presenting the prototype at the final showcase  

---

## 📜 License  
This project is intended for academic, portfolio, and educational use.  
No real student data or confidential advising information is included.
