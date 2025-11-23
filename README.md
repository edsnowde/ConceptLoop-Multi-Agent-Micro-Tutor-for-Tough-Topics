# ConceptLoop-Multi-Agent-Micro-Tutor-for-Tough-Topics

### *Agents for Good — Education Track · Kaggle AI Agents Intensive Capstone · 2025*

## 📌 Overview

ConceptLoop is a **multi-agent AI tutoring system** designed to help students learn complex technical concepts through **step-by-step micro-teaching, adaptive explanations, quick quizzes, and progress-tracking memory**.

The system transforms any topic (e.g., *Binary Search*, *Recursion*, *Probability*, *Photosynthesis*) into a guided learning experience powered by sequential AI agents.
This solution targets **students with limited access to structured learning resources**, helping them learn faster and more effectively.

---

## 🎯 Problem Statement

Many students struggle to learn difficult subjects alone because:

* They don’t know **where to start** or **how to break topics into steps**
* Learning material is often too overwhelming or advanced
* Teachers cannot provide personalized explanations or continuous progress support
* Self-learning lacks feedback loops and real-time assessment

---

## 💡 Solution

ConceptLoop provides a **guided micro-learning system** using **multi-agent AI orchestration**, where:

1. A **Planner Agent** breaks a topic into small steps
2. A **Tutor Agent** explains each step clearly with examples
3. A **Quiz Agent** checks understanding and improves weak concepts
4. A **Coach Agent** coordinates agents, loops weak answers, and stores progress

This creates a **personalized, adaptive learning path** that feels like studying with a real human tutor.

---

## 🧬 Key Innovations & Novelty

| Feature               | Description                                                      |
| --------------------- | ---------------------------------------------------------------- |
| 🧠 Multi-Agent System | Planner, Tutor, Quiz, Coach orchestrated sequentially            |
| 🔁 Adaptive Looping   | If user performs poorly, agent re-explains and re-quizzes        |
| 🔍 Built-in Tools     | Uses `google_search` tool for real-world examples & research     |
| 🧰 Custom Tool        | `update_progress` logs understanding level for each step         |
| 🧠 Memory & Sessions  | Stored with `InMemorySessionService` and `MemoryService`         |
| 🧪 Auto-Reasoning     | Uses agent tool-calling to trigger planning, tutoring & quizzing |
| 📚 Long-Term Learning | Saves past sessions and tailors future difficulty                |

> Designed to significantly improve accessibility to education anywhere, anytime.

---

## 🧱 Architecture

```
User
 |
 ↓
Coach Agent (Orchestrator)
 |--- Planner Agent → Break topic into steps
 |--- Tutor Agent → Explain step with examples (uses google_search tool)
 |--- Quiz Agent → Ask questions & evaluate
 |--- update_progress Tool → Save learning progress
 |
 ↓
Memory Service (Personal learning history)
```

---

## 🛠 Tech Stack

| Component       | Technology                          |
| --------------- | ----------------------------------- |
| LLM             | Gemini 2.5 Flash                    |
| Agent Framework | Google ADK (Python)                 |
| Tools           | google_search, custom tool, memory  |
| Environment     | Kaggle Notebook                     |
| Deployment      | Kaggle Notebook + GitHub repository |

---

## 🧪 Demonstrated Course Concepts

☑ Multi-Agent System (planner, tutor, quiz, coach)
☑ Sequential agent orchestration + looping conditions
☑ Built-in tools (`google_search`)
☑ Custom tool (`update_progress`)
☑ Sessions & memory (`InMemorySessionService`, `InMemoryMemoryService`)
☑ Observability & event tracing via debug runner prints

---

## 🚀 How to Run (Kaggle Notebook)

### Step 0 — Setup

```
!pip install google-adk google-genai
```

### Step 1 — Set API Key

```
import os
os.environ["GOOGLE_API_KEY"] = "YOUR_KEY"
```

### Step 2 — Run the notebook cells in order

Use:

```
await run_once("I want to understand binary search from scratch.")
```

---

## 📌 Example Output

```
🧠 Steps planned → Tutor explanation → Quiz questions → Progress logged
```

and stored into long-term memory for later improvement.

---

## 📁 Repository Structure

```
/notebook
   └── conceptloop.ipynb
/README.md
/images/architecture.png (optional)
```

---

## 🌍 Impact

ConceptLoop democratizes access to high-quality education — especially for:

* Rural and under-resourced students
* Learners without access to tutors
* Beginners struggling with foundational CS topics

It creates a personalized learning companion that is scalable, repeatable, and always available.

---

## 🏁 Future Enhancements

| Upgrade                         | Benefit                                   |
| ------------------------------- | ----------------------------------------- |
| Speech agent + voice output     | Accessible for visually impaired students |
| Web UI & progress dashboard     | Track mastery over time                   |
| Domain-specific learning models | Engineering, medical, legal prep          |
| Multilingual support            | Increase global accessibility             |

---

## 📜 License

MIT License

---

## 👤 Author

**Syed Fuzail**
AI/ML Developer | DSU | ACM | Kaggle Participant 2025

---

## ⭐ Acknowledgements

Thanks to **Google AI**, **Kaggle**, and the **Agents Intensive community** for guidance and technology.

---

## 💬 Feedback & Contributions

Pull requests and improvements welcome!


