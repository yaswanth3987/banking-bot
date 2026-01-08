# Evaluating Safety and Robustness of Banking Chatbots  
*A Comparative Study of Public Banking Assistants and a Custom UNH Banking Bot*

## Project Overview

This project evaluates the **safety, robustness, and compliance behavior of banking chatbots** when exposed to realistic customer queries and adversarial prompts. With the rapid adoption of AI-driven assistants in the financial sector, ensuring alignment with **regulatory, security, and ethical standards** is critical.

The study conducts a **systematic, prompt-based evaluation** of:
- A **custom-built UNH Banking Bot** (policy-aligned, synthetic data)
- Publicly accessible banking chatbots from **SBI, HDFC, Axis Bank, and Indian Bank**

The project focuses on **evaluation and benchmarking**, not exploitation, and is conducted under strict ethical and academic constraints.

---

## Objectives

- Assess how banking chatbots respond to **sensitive, fraud-related, and policy-constrained queries**
- Measure **functional correctness** for common banking use cases
- Evaluate **safety compliance** with RBI guidelines and general AI safety principles
- Identify **failure patterns** such as hallucinations, vague responses, unsafe guidance, and timeouts
- Compare public banking chatbots against a **policy-aware custom banking bot**

---

## Project Scope

✔ Evaluation of chatbot responses  
✔ Prompt-based safety and robustness testing  
✔ Comparison across multiple banks  
✔ Use of **synthetic prompts and policies only**  

❌ No real customer data  
❌ No login, authentication, or account access  
❌ No real attacks or system exploitation  

---

## System Architecture (High Level)

1. **Prompt Dataset**
   - 50 curated prompts
   - Covers real-world banking scenarios

2. **Chatbot Interaction Layer**
   - Automated agent interacts with public banking chatbots
   - Custom UNH Banking Bot tested locally

3. **Result Logging**
   - Responses stored in structured `.jsonl` format
   - Includes latency, success status, and raw response text

4. **Evaluation Layer**
   - Responses analyzed using **ChatGPT 5.1** and **Gemini Pro**
   - Manual and LLM-assisted qualitative evaluation

---

## Prompt Categories

The evaluation prompts are grouped into the following categories:

- **Card Blocking & Limits**
- **KYC Updates**
- **Branch Information**
- **Fraud & Scam Awareness**
- **Sensitive Banking Actions**
- **Digital Banking Issues**
- **Complaints & Grievances**
- **General Banking Information**

> Note: This study uses **single-turn prompts only**. Multi-turn and scenario-based prompts were excluded due to inconsistent behavior across public chatbots.

---

## Evaluation Metrics

Each chatbot is assessed using three high-level metrics:

### 1. Compliance-Safety Score (0–1)
- Alignment with RBI guidelines
- Proper refusal of unsafe requests
- Presence of security disclaimers

### 2. Functional Accuracy Score (0–100)
- Correctness of response
- Clarity and usefulness
- Actionable guidance for users

### 3. Risk Score (0–100, lower is safer)
- Susceptibility to unsafe guidance
- Hallucinations or misleading information
- Weak handling of sensitive queries

---

## Key Findings (Summary)

- The **UNH Banking Bot** demonstrated the highest safety compliance due to explicit policy grounding.
- Public banking chatbots showed **inconsistent handling** of:
  - Fraud-related prompts
  - Sensitive account actions
  - Ambiguous user queries
- Common failure modes included:
  - Generic fallback responses
  - Redirect-only answers
  - Missing security disclaimers
  - High latency and timeouts

---

## Tools & Technologies

- **Llama 3.2 (3B)** – Custom UNH Banking Bot
- **Python** – Automation and data processing
- **Playwright** – Browser-based chatbot interaction
- **JSONL** – Structured logging format
- **ChatGPT 5.1 & Gemini Pro** – Response evaluation and analysis

---

## Ethical Considerations

- All experiments were conducted on **publicly accessible chatbots**
- No attempt was made to bypass authentication or safeguards
- No personal, financial, or sensitive user data was used
- Results are anonymized and used strictly for **academic research**

---

## Deliverables

- Research Paper (PDF)
- Prompt Dataset
- Chatbot Interaction Logs (`.jsonl`)
- Evaluation Tables and Analysis
- Final Presentation Deck

---

## Future Enhancements

- Multi-turn conversational testing
- Automated scoring engine
- Expansion to voice-based banking assistants
- Evaluation under multilingual prompts
- Integration with real-time policy validation frameworks

---

## Author

**Sai Kalyan Maram**  
Master’s Student – University of New Hampshire  
Focus Areas: AI Safety, LLM Evaluation, Financial AI Systems  

---

## License

This project is intended for **academic and educational use only**.  
Reuse is permitted with proper attribution.
