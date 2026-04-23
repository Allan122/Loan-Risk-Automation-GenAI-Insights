# Loan Risk Automation & GenAI Insights
This repository contains an end-to-end automation solution for financial risk analysis. It leverages **n8n** for workflow orchestration and **GenAI (LLaMA 3.3 70B)** to transform raw loan data into actionable business intelligence and human-readable transparency.
## 📂 Project Structure
 * **/workflows**: Contains Workflow1.json (Executive Reporting) and Workflow2.json (Loan Explanation).
 * **/screenshots**: Visual evidence of successful workflow execution and green-check verification.
## 🛠️ Tech Stack
 * **Automation:** n8n
 * **AI Model:** LLaMA 3.3 70B (via Groq/OpenAI Node)
 * **Data Handling:** JavaScript (n8n Code Node)
 * **API Integration:** REST API (HTTP Request Node / Webhooks)
 * **Testing:** httpbin.org (Post-request verification)
## 🚀 Workflows & GenAI Usage
### 🔹 Workflow 1: Executive Risk Reporting
**Problem Statement:** Manual monitoring of loan portfolios is inefficient. Leadership needs immediate, high-level summaries of risk exposure without digging through raw datasets.
 * **Logic Flow:** Schedule Trigger ➡️ JS Code Node ➡️ AI Model ➡️ HTTP Request (Alert)
 * **GenAI Implementation:**
   * **Input:** Portfolio metrics (Total Loans, % Bad Loans, Regional Trends).
   * **Prompt Strategy:** Role-based (Chief Risk Officer). Instructed to identify high-risk drivers and maintain professional executive tone.
   * **Output:** A structured email summary highlighting that Grade 'E' and 'F' loans are the primary drivers of loss.
### 🔹 Workflow 2: On-Demand Loan Explainer
**Problem Statement:** Borrowers often lack transparency regarding why a loan is flagged as "Bad." This workflow provides instant, automated clarity to the user.
 * **Logic Flow:** Webhook ➡️ JS Code Node ➡️ AI Model ➡️ HTTP Request (Return Payload)
 * **GenAI Implementation:**
   * **Input:** Granular borrower data (DTI: 42%, Grade: E, Interest Rate: 21.5%).
   * **Prompt Strategy:** Interpretive & Empathetic. Instructed to simplify financial jargon and compare the profile to a "Good" loan benchmark.
   * **Output:** A human-readable explanation explaining that high debt-to-income ratios and high interest rates are the primary risk factors.
## 📸 Execution Evidence
> *Note: Place your screenshots here in the GitHub preview.*
> 
 1. **Workflow 1 Overview:** <img width="1311" height="380" alt="Workflow 1" src="https://github.com/user-attachments/assets/14380acb-7813-45ed-839a-a8059c28ca35" />
 2. **Workflow 2 Overview:** <img width="1464" height="433" alt="Workflow 2" src="https://github.com/user-attachments/assets/00d99c52-38aa-47cd-abab-62641e388bc6" />
 3. **Workflow 1 Sample AI Output:** 
 4. **Workflow 1 Sample AI Output:** <img width="1798" height="843" alt="Sample AI Output Workflow 2" src="https://github.com/user-attachments/assets/3e461c3c-07c1-47ce-870d-a5ef7b47408d" />

## 💡 Key Insights
 * **Scalability:** By using **HTTP Request** nodes instead of basic email nodes, these workflows can be integrated into any modern ERP or CRM system.
 * **Accuracy:** Using the **LLaMA 3.3 70B** model ensures that the risk analysis remains contextually aware of financial nuances like DTI (Debt-to-Income) impact.
 * **Efficiency:** Automated 100% of the manual report-writing process for the risk department.

**Project developed by:** Allan Alex
**Final Submission Date:** June 22, 2026
