# Phase D — Instruction Set Integration  
**ISOM 360 – Advising Chatbot Project**

## Purpose
Phase D explains how the team transfers the finalized Instruction Set (from the Design Pack) into the Custom GPT environment. This step ensures consistent behavior, tone, escalation rules, and category boundaries.

---

## 1. Locate the Instruction Field
1. Open **ChatGPT Plus → Explore GPTs → Your Custom GPT → Build tab**  
2. Find the field labeled **"Instructions"**.  
   - This is where the system-level behavior logic is stored.

---

## 2. Paste the Final Instruction Set
1. Open the Design Pack (Phase 1 – Instruction Set).  
2. Copy **all content** from the Instruction Set block, including:
   - Purpose  
   - Scope (six advising categories)  
   - Knowledge Sources  
   - Style & Tone  
   - Escalation Directory  
   - Out-of-Scope Templates  
   - Response Model  
3. Paste directly into the GPT Instruction field **without editing**.

---

## 3. Verify Required Components
Confirm that the following appear clearly:

### **A. Purpose**
Defines that the bot supports student advising in a clear, friendly manner.

### **B. Scope – Six Categories**
1. Registration in Workday  
2. Academic Standing  
3. Program of Study  
4. Residency & Double Counting  
5. Holds in Workday  
6. Credit Load & Overload  

### **C. Knowledge Sources**
- Use uploaded Knowledge Base (KB) files first.  
- If browsing is needed, restrict to official academic sites.  
- Always cite the source.

### **D. Style / Tone**
- ≤ 200 words  
- Clear, student-friendly, policy-accurate  
- Paraphrased, not copied verbatim

### **E. Escalation Directory**
List the correct advising offices for referral.

### **F. Out-of-Scope Templates**
Standard OOS categories:
- Financial Aid  
- Visa/Immigration  
- GPA/Prediction  
- FERPA / Sensitive Records  

### **G. Response Model**
1. Identify category  
2. Retrieve KB chunk  
3. Compose answer  
4. Cite source  
5. Redirect if out-of-scope  

---

## 4. Save & Confirm
- Click **Save → Continue**  
- Reopen the bot to confirm that all sections remain in the Instruction field  

