### 🧠 MindCompass — Multi-Agent Well-Being Resource Navigator & Micro-Coach
A safe, non-diagnostic, multi-agent well-being assistant designed to help users navigate emotional overwhelm, stress, low focus, or everyday struggles—while staying ethical, resource-oriented, and safety-compliant.

MindCompass is built using multi-agent orchestration, lightweight memory, and an optional Gradio/Streamlit chat UI.

---

## ⭐ Why MindCompass?
People dealing with stress or emotional overwhelm often struggle to find trustworthy well-being resources or actionable steps quickly.

MindCompass provides:

🧭 Emotion detection

💬 Safe micro-coaching actions

🌱 Personalized 7-day mini well-being plans

🔗 Trusted “resources-only” mental-health navigation

🛡️ Crisis detection & safety guardrails (no therapy, diagnosis, or medical advice)

----
### 🧩 Multi-Agent Architecture

MindCompass Multi-Agent Orchestration — System Description

MindCompass follows a structured, safety-first multi-agent workflow that processes user messages in a controlled, ethical, and highly modular pipeline. Each agent is responsible for a distinct cognitive task, enabling the system to remain predictable, explainable, safe, and non-diagnostic.

The overall interaction begins with a user query and flows through a series of lightweight agents:

### 🔹 MindCompass Multi-Agent Workflow (Short Summary)

- **Safety Agent**  
  Screens user messages for crisis or self-harm signals and redirects to emergency help if needed.

- **Emotion Agent**  
  Extracts emotional cues (stress, overwhelm, sadness, focus issues) without performing any diagnosis.

- **Micro-Coach Agent**  
  Provides safe, practical 1–2 minute micro-actions (breathing, grounding, reflection prompts).

- **Resource Navigator**  
  Maps user needs to trusted, pre-verified well-being resources.

- **Plan Generator**  
  Creates an optional personalized 7-day micro-well-being plan.

- **Orchestrator**  
  Coordinates all agents and produces the final, clean, supportive response.


The diagram below illustrates the complete, step-by-step orchestration that powers MindCompass.

```mermaid
sequenceDiagram
    participant U as User
    participant SA as Safety Agent
    participant EA as Emotion Agent
    participant MC as Micro-Coach
    participant RN as Resource Navigator
    participant PG as Plan Generator
    participant R as Final Response

    U->>SA: Sends Query
    SA->>SA: Validate & Sanitize Input
    SA->>EA: Forward Cleaned Input
    EA->>EA: Emotion Interpretation
    EA->>MC: Send Context + Emotion
    MC->>MC: Clarify & Micro-Coach
    MC->>RN: Forward Refined Intent
    RN->>RN: Resource Mapping
    RN->>PG: Send Resource Insights
    PG->>PG: Create Structured Plan
    PG->>R: Generate Final Output
    R->>U: Return Response


```

-----
🔐 1. Safety Agent

Detects crisis signals (self-harm, suicidal language, severe distress).
If triggered → bypass all agents → deliver crisis hotlines & immediate help info.

