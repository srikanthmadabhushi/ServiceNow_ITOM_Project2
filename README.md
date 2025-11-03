# ServiceNow_ITOM_Project2
AI detected
# ITOM Project 2: Agentic AI Auto-Remediation Flow

### 🧠 Overview
This project demonstrates how **Agentic AI** enables self-healing automation in **ServiceNow ITOM (Yokohama PDI)**.  
It simulates AI detecting a critical event, creating an incident, performing automated remediation, and updating status — reducing mean time to recovery (MTTR) and operational load.

---

### ⚙️ Components Used
- **Module:** IT Operations Management (ITOM)
- **Plugins:** Event Management, Discovery
- **Table:** `AI Remediation Events`
- **Flow Designer:** Trigger on record update
- **Logic:** If Severity = Critical → Incident + Auto-Remediation → Status = Resolved

---

### 🧩 Flow Logic
1. **Trigger:** Record inserted or updated in `AI Remediation Events`
2. **Condition:** If `Severity = Critical` and `Remediation_Status = Pending`
3. **Action 1:** Create Incident (Category = Operations, Impact = High)
4. **Action 2:** Update Event → Status = Running → AI_Action_Note = “Remediation started”
5. **Action 3:** Wait (2 seconds)
6. **Action 4:** Update Event → Status = Resolved → AI_Action_Note = “System stabilized. Incident auto-resolved by AI Flow.”

---

### 🧪 Test Scenario
| Service Name | Issue Type | Severity | Expected Outcome |
|---------------|-------------|-----------|----------------|
| Database 01 | CPU Failure | Critical | Incident auto-created and auto-resolved |
| App Server 02 | Network Down | Medium | No action triggered |

### 🧭 Key Learning
- Demonstrated **Agentic AI autonomy** for proactive IT operations  
- Showcased **self-healing workflows** in ServiceNow  
- Reduced manual intervention via automated incident handling  
- Reinforces **AI-driven reliability engineering**

---

### 🧾 Evidence Diagram
![Flow Diagram](Diagrams/Flow Diagram.png)
