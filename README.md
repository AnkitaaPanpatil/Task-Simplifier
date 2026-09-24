# ⚡ Task Simplifier — AI Productivity & Daily Organizer

**Task Simplifier** is an intelligent, neuroscience-backed task manager and daily schedule optimizer designed to eliminate initiation friction, cognitive overload, and decision fatigue. By pairing natural language task parsing with an AI-powered micro-action decomposer, an Eisenhower priority matrix, circadian rhythm time-blocking, and an integrated deep work sprint timer, Task Simplifier transforms overwhelming to-do lists into clear, frictionless momentum.

---

## 🌟 Key Features

### 1. 🧠 AI Task Decomposer (Cognitive Load Reducer)
- **Friction-Free Breakdown**: Large, intimidating goals (e.g., *"Prepare quarterly financial audit"*) often trigger psychological avoidance. With one click on **"Simplify"**, the integrated Gemini engine decomposes the task into 3–4 sequential, low-resistance micro-actions (under 15 minutes each).
- **Progress Tracking**: Interactive subtask check-offs with dynamic percentage completion bars on each task card.
- **Resilient Fallback**: Includes a built-in heuristic decomposition algorithm that functions automatically even without an active internet connection or API key.

### 2. ✍️ Natural Language Quick-Add Bar
- Ingest complex task parameters in a single conversational sentence:
  - *Example:* `"File tax return before Friday 5pm urgent #finance 45m"`
- The smart parser automatically extracts:
  - **Title**: Cleaned of priority tags and duration markers.
  - **Eisenhower Priority**: Detects `urgent`, `asap`, `p1`, `p2`, `p3`, `p4`.
  - **Category**: Identifies `#health`, `#personal`, `#learning`, `#work`.
  - **Estimated Duration**: Parses patterns like `45m`, `30 min`, `15 mins`.
  - **Cognitive Load Weight**: Automatically computed from duration and complexity.

### 3. 🎯 Multi-View Productivity Framework
- **Smart List View**: Categorized task list with cognitive load tags, inline subtasks, and quick action shortcuts.
- **Eisenhower Matrix View (2×2)**:
  - **P1: Do First** — Urgent & Important (critical deadlines, crises).
  - **P2: Schedule** — Important, Not Urgent (high-leverage growth, health, deep work).
  - **P3: Delegate / Fast-Track** — Urgent, Not Important (interruptions, quick admin).
  - **P4: Eliminate / Defer** — Low priority or backlog items.
- **Circadian Time-Blocking View**: Automatically distributes your daily tasks across optimal biological energy windows:
  - `09:00 AM – 10:30 AM`: Peak Morning Flow (High prefrontal focus).
  - `11:00 AM – 12:00 PM`: Urgent Standups & Deadlines (P1 execution).
  - `01:30 PM – 03:00 PM`: Steady Post-Lunch Cadence (Moderate tasks).
  - `04:00 PM – 05:00 PM`: Low-Stakes Admin & Inbox Zero (Low-energy wind-down).

### 4. ⏱️ Deep Work Engine (Pomodoro Sprint)
- Anchor any task directly to the active timer HUD with the crosshair button.
- Choose between **25m Work Sprint**, **5m Rest Break**, or **50m Deep Flow**.
- **Pure Web Audio Synthesizer**: Uses native browser Web Audio oscillators to generate pleasant, distraction-free chimes on sprint completion—no external audio files required.

### 5. 🤖 AI Productivity Coach "Athena"
- Built-in conversational assistant for overcoming task paralysis, afternoon energy dips, and prioritization dilemmas.
- Prompt shortcuts for immediate advice:
  - *“Priority Overwhelm”* — Tactical triage when everything feels urgent.
  - *“Afternoon Reset”* — Physiology-based micro-breaks for post-lunch fatigue.

### 6. 💾 Local Storage Persistence
- All tasks, priority assignments, subtasks, timer sessions, and completion states are stored locally in the browser (`localStorage`).
- Zero account registration or server backend required.

---

## 🛠️ Technology Stack

| Layer | Technology | Details |
| :--- | :--- | :--- |
| **Markup & Layout** | HTML5 Semantic Elements | Fully responsive grid and modal overlays |
| **Styling & Theme** | Tailwind CSS CDN | Modern dark mode aesthetic (`slateDark-950` / Violet accents) |
| **Typography & Icons** | Inter, JetBrains Mono, FontAwesome 6.5 | Clean data hierarchy and modern iconography |
| **Sound Engine** | Web Audio API | Custom sine/triangle wave synthesized chimes |
| **Artificial Intelligence** | Google Gemini API (`gemini-3-flash`) | Structured task decomposition and productivity coaching |
| **Storage & State** | Client-Side Vanilla JS + `localStorage` | Fast, zero-dependency local data persistence |

---

## 📂 File Structure

```text
├── task_simplifier_app.html    # Standalone single-file application (HTML, CSS, JS)
└── README.md                   # Comprehensive project documentation
```

---

## 🚀 Quick Start & Installation

Because Task Simplifier is built as a single, self-contained file, no complex installation, Node.js packages, or build steps are required.

### Method 1: Direct File Launch (Easiest)
1. Download `task_simplifier_app.html`.
2. Double-click the file to open it in your default web browser (Chrome, Firefox, Safari, Edge, or Brave).

### Method 2: Local HTTP Server (Recommended)
Running via a local web server provides the best performance for browser APIs:

```bash
# Using Python 3
python -m http.server 8080

# Using Node.js npx
npx serve .
```

Open your browser and navigate to:
```text
http://localhost:8080/task_simplifier_app.html
```

---

## 🔑 Configuring the Gemini API Key

Task Simplifier runs out-of-the-box using built-in heuristic fallback logic. To connect live, high-precision AI capabilities powered by Google Gemini:

1. Open `task_simplifier_app.html` in your favorite code editor (VS Code, Sublime, etc.).
2. Locate the `apiKey` variable in the `triggerTaskDecompose()` and `submitAiAdviceQuery()` functions:
   ```javascript
   const apiKey = "YOUR_GEMINI_API_KEY_HERE";
   ```
3. Get a free API key from [Google AI Studio](https://aistudio.google.com/).
4. Paste your key into both variables, save the file, and refresh your browser.

> **Security Note:** If you deploy this repository publicly to GitHub Pages, leave the `apiKey` string empty or allow users to input their key dynamically to protect your quota.

---

## 💡 How to Use: The 3-Step Anti-Procrastination Flow

1. **Dump and Parse**:
   - Type your daily tasks into the top bar using shorthand:
     `"Prepare slides for client demo tomorrow urgent 30m #work"`
   - Hit **Enter**. The system categorizes it, marks it as P1, and sets a 30-minute estimated duration.
2. **Decompose High-Friction Tasks**:
   - Spot any task that gives you hesitation or anxiety.
   - Click the **"Simplify"** button. The AI will slice it into 3–4 micro-actions under 15 minutes each.
   - Click **"Apply Subtasks"** to embed them directly into the parent card.
3. **Anchor & Sprint**:
   - Click the crosshairs icon on the first micro-action to anchor it to the timer.
   - Press **"Start Sprint"** and focus solely on that 10–15 minute step.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE). Feel free to adapt, customize, and integrate it into your personal productivity setup or workflow systems.
