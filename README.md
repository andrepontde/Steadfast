# 🧠 Steadfast (WIP)

**Steadfast** is an upcoming productivity-focused AI desktop assistant designed to help users accomplish their goals by dynamically adapting their digital environment based on behavior, intention, and context.

By combining behavioral monitoring, journaling analysis, and AI-driven automation, Steadfast will intelligently reward focus and reduce distractions — helping users stay on track in real time.

---

## 🚧 Project Status

> 🛠 This project is in active planning and early development.  
> Contributions and feedback are welcome!

---

## 🔮 Vision

The goal of Steadfast is to create a hybrid desktop app that:

- Understands what users want to accomplish
- Monitors their actual behavior (apps used, time spent, distractions)
- Uses AI to interpret context and recommend or trigger actions
- Rewards productive habits (e.g., by launching a focus setup)
- Penalizes distractions (e.g., blocking certain apps or websites)
- Uses journaling input to better align with user goals

Steadfast will aim to serve as both a **habit builder** and a **real-time focus coach** — seamlessly integrated into the user's daily workflow.

---

## 🧩 Planned Architecture

### 1. **System Agent (C#)**

A lightweight Windows service or tray application that monitors system-level behavior:

- Active window tracking
- Time spent in apps
- Registry changes
- File and network access
- App launch frequency

🔌 **Responsibilities:**

- Run on system startup
- Send behavioral data to the AI engine via local REST or socket
- Enforce blocking rules on "distraction" apps
- Launch productivity tools when triggered

---

### 2. **AI Engine (Python + FastAPI)**

A local REST API built with Python, responsible for:

- Processing behavioral data
- Integrating with GPT or Google Search APIs
- Analyzing notes written by the user (via the Steadfast Notes app)
- Generating insights, alerts, predictions
- Assigning "focus scores" or penalty thresholds
- Issuing commands back to the agent (e.g., block/unblock apps)

🧠 **Technologies:**
- `FastAPI` for API server
- `spaCy` or `transformers` for NLP
- GPT API integration for recommendations
- Local SQLite or simple JSON storage for user profile

---

### 3. **Steadfast Notes (Electron)**

A built-in journaling and productivity planning interface:

- Users can write goals, daily logs, tasks, intentions
- These entries will influence how the AI scores and guides behavior
- Serves as the "brain dump" and context engine for personalized productivity

💡 Example:
> If user writes: “I want to spend the morning writing my paper,”  
> The system will track behavior accordingly and discourage switching to entertainment apps.

---

### 4. **Frontend Dashboard (Electron or Web)**

An optional UI to:

- Display app usage stats, scores, and trends
- Visualize goal progress
- Offer control over settings, rules, and schedules
- Show motivational nudges or resource recommendations

---

## 🧬 Planned Features

| Feature | Description |
|--------|-------------|
| 🧭 Goal-Aware AI | Understand user intentions and adjust system accordingly |
| ⏱ App Usage Tracking | Monitor how long and how frequently apps are used |
| 📕 Journaling Context | Use user-written notes to detect productivity themes |
| 🧠 GPT Integration | Search for helpful tools, articles, and solutions |
| 🏁 Rewards System | Trigger events like launching productivity environments |
| ⛔ Distraction Blocking | Limit access to apps after a certain threshold |
| 💰 Debt Repayment System | Re-enable apps by completing productive work |
| 📊 Analytics UI | Show daily focus score, history, goal streaks |

---

## 🔧 Planned Tech Stack

| Layer | Tech |
|------|------|
| System Agent | C# (.NET 6+), Windows Service or Tray App |
| AI Engine | Python 3.11+, FastAPI, GPT API, NLP libraries |
| Notes App | Electron (React or Vanilla JS frontend) |
| Dashboard UI | Electron + TailwindCSS or WebView2 |
| Communication | HTTP/REST (localhost), Named Pipes or SocketIO (optional) |
| Storage | Local JSON, SQLite, or LiteDB |

---

## 🔄 Workflow Example (Future Flow)

1. User starts their day and logs a goal in Steadfast Notes.
2. AI Engine parses the goal and sets a "focus intent."
3. C# Agent tracks activity (e.g., VS Code used for 45 minutes, YouTube opened 3x).
4. AI detects possible distraction and sends block command to agent.
5. User completes a task, earning credits — YouTube is unblocked for 10 minutes.
6. At the end of the day, the dashboard shows a 74% productivity score and offers next-step tips.

---

## 📦 Installation (Planned)

> ⚠️ Coming soon — install instructions will be provided when components are stable.

### Target Platforms
- [x] Windows 10 / 11 (primary)
- [ ] macOS (experimental, limited support)
- [ ] Linux (future consideration)

---

## 💡 Inspiration

Steadfast is inspired by tools like:

- RescueTime
- Cold Turkey Blocker
- Notion
- Replika
- Habitica

…but aims to combine system-level awareness with personalized, AI-powered coaching.

---

## 🤝 Contributing

Contributions will be welcome once core modules are scaffolded.

To be added:

- Contribution guidelines
- Code of conduct
- Issue templates

---

## 📌 Roadmap

| Milestone | Status |
|----------|--------|
| C# Agent MVP | 🔜 Planned |
| Python AI Engine | ⏳ In Progress |
| Electron Notes App | 🔜 Planned |
| Frontend Dashboard | 🔜 Planned |
| GPT Integration | 🔜 Planned |
| Productivity Scoring | 🔜 Planned |

---

## 📄 License

TBD — Likely MIT or AGPL. Will be clarified before first release.

---

## 🌐 Stay Tuned

Follow the repo and check back for updates. This project is still in early development — but we’re building something powerful.

> _Built with focus, for focus._
