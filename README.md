# MedGemma Prenatal Care Assistant

---

### Team
- **Vittal Badami** — AI Engineering, System Architecture, Prompt Design  
- **Sowmithry Krishnamoorthy** — UX/UI Design, Medical Domain Expertise, Data Integration

---

### Problem Statement
Pregnancy is a time of uncertainty, anxiety, and frequent questions—especially for first-time mothers and those with high-risk pregnancies. Globally, 45% of pregnant women lack adequate prenatal care (WHO, 2023). Medical questions arise 24/7, but clinics operate limited hours. Existing apps provide generic advice, ignoring individual medical histories, allergies, and pregnancy types. This leads to preventable complications, unnecessary ER visits, and increased anxiety for mothers and families.

---

### Overall Solution
MedGemma Prenatal Care Assistant is a compassionate, AI-powered companion that delivers personalized, actionable guidance to expectant mothers—anytime, anywhere. Leveraging Google’s MedGemma 4B-IT medical language model, our system intelligently routes user queries to specialized agents (Symptom Analyzer, Report Explainer, Week Tracker, Daily Care Planner, General Advisor) based on context and user profile. Every response is tailored using real-time intent classification and the patient’s medical history, pregnancy week, allergies, and more. The assistant provides risk assessments, explains lab reports, offers daily care plans, and answers general questions, all with medical disclaimers and context-aware advice.

---

### Technical Details
- **Model:** Google MedGemma 4B-IT, deployed with 4-bit quantization for efficient inference on free GPUs (Kaggle/Colab).
- **Architecture:** Dual MedGemma calls per query—first for intent classification (routing agent), second for specialized agent response.
- **Agents:** Five expert-crafted agents (Symptom Analyzer, Report Explainer, Week Tracker, Daily Care Planner, General Advisor) with personalized system prompts.
- **Robust JSON Extraction:** Custom logic to recover and parse model outputs, even when truncated or malformed.
- **User Profile Integration:** One-time profile setup (age, weight, pregnancy week/type, medical history, allergies, blood group, pregnancy history) used for all recommendations.
- **UI:** Gradio web app with six tabs, color-coded risk badges, responsive design, and accessibility features.
- **Error Handling:** Retry logic, logging, and medical disclaimers for safety and reliability.
- **Deployment:** Zero-cost, scalable, and privacy-respecting (no data storage, all processing on-device).

**Impact:**  
Empowers mothers with instant, personalized medical guidance, reduces anxiety, improves early risk detection, and democratizes access to prenatal care globally.
