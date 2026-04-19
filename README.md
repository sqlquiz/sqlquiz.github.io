# 🗃️ SQL Quiz

An interactive web-based quiz application to test and improve your SQL database knowledge with expertly crafted questions across multiple categories.

**[▶ Launch Quiz](https://sqlquiz.github.io)**

![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

## 📋 Overview

SQL Quiz is a single-page application built with vanilla HTML, CSS, and JavaScript — no frameworks, no dependencies, no build step. It runs entirely in the browser and stores all progress locally.

Each question presents **5 randomly selected options** from a pool of 7, ensuring a fresh experience every time you take the quiz.

## ✨ Features

### 🎯 Quiz Engine
- Questions spanning multiple SQL categories
- **5 randomized options** per question (selected from 7 possible answers)
- **3 difficulty levels** — Easy, Medium, Hard
- Configurable question count
- Detailed explanations for every answer

### ⏱️ Timer System
- Configurable per-question timer (15, 30, 45, 60 seconds or disabled)
- Visual countdown with color-coded warnings
- Automatic answer reveal when time expires

### 💾 Progress Persistence
- Quiz state saved to `localStorage` automatically
- Resume unfinished quizzes across sessions
- Settings remembered between visits

### 🏆 Achievements & Tracking
- Unlockable awards
- Visit counter and quiz completion tracker
- Best score tracking
- Daily streak system with fire indicator
- Per-category score breakdown in results

### 🎉 Celebrations
- Confetti animation for high scores
- Congratulations popup with earned awards
- Tiered messages based on performance

### 📊 Results Dashboard
- Final score with percentage
- Correct / Wrong / Time breakdown
- Category-by-category performance bars
- Personalized feedback message

## 📚 Categories

| # | Category | # | Category |
|---|---|---|---|
| 1 | SQL Basics | 11 | Transactions |
| 2 | SELECT Queries | 12 | Views |
| 3 | WHERE & Filtering | 13 | Stored Procedures |
| 4 | JOINs | 14 | Triggers |
| 5 | GROUP BY & HAVING | 15 | Window Functions |
| 6 | Subqueries | 16 | Performance & Optimization |
| 7 | INSERT, UPDATE, DELETE | 17 | Data Types |
| 8 | Table Design | 18 | Constraints |
| 9 | Indexes | 19 | SQL Functions |
| 10 | Normalization | 20 | Best Practices |

Each category contains questions with a balanced mix of Easy, Medium, and Hard difficulty.

## 🚀 Getting Started

### Option 1 — Use Online

Visit **[sqlquiz.github.io](https://sqlquiz.github.io)** — nothing to install.

### Option 2 — Run Locally

```bash
git clone https://github.com/sqlquiz/sqlquiz.github.io.git
cd sqlquiz.github.io
```

Open `index.html` in any browser. No server required.

### Option 3 — Serve Locally

```bash
# Python 3
python -m http.server 8000

# Node.js (npx)
npx serve .
```

Then open `http://localhost:8000`.

## 🏗️ Project Structure

```
sqlquiz.github.io/
├── index.html      # Entire application (single file)
└── README.md       # This file
```

The application is intentionally contained in a **single HTML file** with embedded CSS and JavaScript for maximum portability — download one file and you have the complete quiz.

## ⚙️ Quiz Settings

| Setting | Options | Default |
|---|---|---|
| **Category** | All Categories or any single category | All Categories |
| **Difficulty** | All, Easy, Medium, Hard | All |
| **Questions** | 10, 20, 50, 100, All | 10 |
| **Timer** | Off, 15s, 30s, 45s, 60s | 30s |

Settings are persisted in `localStorage` and restored on next visit.

## 🏅 Awards

| Award | Requirement |
|---|---|
| 👋 First Steps | First visit |
| 🎯 Quiz Starter | Complete 1 quiz |
| 📚 Dedicated Learner | Complete 5 quizzes |
| 🏆 SQL Expert | Complete 10 quizzes |
| 👑 Quiz Master | Complete 25 quizzes |
| ✅ Passing Grade | Score ≥ 70% |
| ⭐ High Achiever | Score ≥ 90% |
| 💯 Perfectionist | Score 100% |
| 🔥 On Fire | 3-day streak |
| ⚡ Week Warrior | 7-day streak |
| 🌟 Monthly Master | 30-day streak |
| 💪 Century Club | 100 correct answers total |
| 🧠 Knowledge Seeker | 500 correct answers total |
| 🎖️ Triple Perfect | 3 perfect quizzes |

## 🔧 Technical Details

- **Zero dependencies** — no frameworks, libraries, or build tools
- **Single file** — all HTML, CSS, and JavaScript in one file
- **Offline capable** — works without internet after initial load
- **Responsive design** — adapts to mobile, tablet, and desktop
- **LocalStorage** — all data stored client-side, nothing sent to servers
- **SVG favicon** — inline data URI, no external files
- **Accessible** — semantic HTML, keyboard navigable, high contrast

## 🤝 Contributing

Contributions are welcome! Here are some ways to help:

- **Add questions** — expand the question bank
- **New categories** — suggest or add new SQL topic categories
- **Bug reports** — open an issue if something isn't working
- **UI improvements** — enhance accessibility, animations, or design
- **Translations** — help localize the quiz for other languages

### Adding a New Question

Questions follow this structure inside the `allQuestions` object:

```javascript
{
    question: "Your question text here?",
    options: [
        "Correct answer",           // index 0 = correct
        "Wrong answer one",         // indices 1-6
        "Wrong answer two",
        "Wrong answer three",
        "Wrong answer four",
        "Wrong answer five",
        "Wrong answer six"
    ],
    correct: 0,
    explanation: "Explanation of why the answer is correct.",
    difficulty: "easy"  // "easy", "medium", or "hard"
}
```

> **Note:** The first option (`index 0`) is always the correct answer. The quiz engine randomizes the display order automatically. Provide exactly **7 options** — the engine selects 5 at random (always including the correct one).

## 📄 License

MIT License

## 🔗 Links

- **Live App:** [sqlquiz.github.io](https://sqlquiz.github.io)
- **Repository:** [github.com/sqlquiz/sqlquiz.github.io](https://github.com/sqlquiz/sqlquiz.github.io)
- **Issues:** [github.com/sqlquiz/sqlquiz.github.io/issues](https://github.com/sqlquiz/sqlquiz.github.io/issues)
