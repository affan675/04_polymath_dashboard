# 🧠 Polymath Dashboard

> A personal productivity dashboard for Affan — featuring a daily quote, Pomodoro timer, habit tracker, quick notes, and a curated link hub. Designed for focus, discipline, and continuous learning.

![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=flat&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=flat&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=flat&logo=javascript&logoColor=%23F7DF1E)
![GitHub Pages](https://img.shields.io/badge/github%20pages-121013?style=flat&logo=github&logoColor=white)

---

## ✨ Features

- **🕒 Live Clock & Date** – Real‑time updates with a personalised greeting (morning/afternoon/evening/night).
- **💬 Daily Quote** – Random inspirational quotes, refreshable on demand.
- **⏱️ Pomodoro Timer** – 25 min focus / 5 min break sessions with auto‑start and audio‑visual cues.
- **✅ Daily Habits** – Track up to 6 habits with persistent streaks. Resets automatically each day.
- **📝 Quick Notes** – Auto‑saving textarea (debounced + on‑blur). Your thoughts are never lost.
- **🔗 Link Hub** – Curated resources for developers (MDN, freeCodeCamp, GitHub, Stack Overflow, YouTube).
- **🌗 Dark/Light Theme** – Toggle between themes; preference saved in `localStorage`.
- **📱 Fully Responsive** – Works seamlessly on desktop, tablet, and mobile devices.

---

## 🚀 Live Demo

> **Host it yourself** – see [Deployment to GitHub Pages](#-deployment-to-github-pages) below.  
> Or simply open `index.html` locally after cloning.

---

## 🛠️ Technologies

- **HTML5** – Semantic structure
- **CSS3** – Custom properties (theming), Flexbox, Grid, smooth animations
- **JavaScript (ES6)** – Modularised (IIFEs), local storage, DOM manipulation
- **LocalStorage API** – Persists habits, notes, theme preference, and Pomodoro state

---

## 📦 Installation (Local)

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/polymath-dashboard.git
   cd polymath-dashboard
Open the dashboard

Double‑click index.html or use a local development server:

bash
npx serve .
# or
python -m http.server 8000
Start using the dashboard – no build steps or dependencies required.

🧩 Usage
Quote – Click the 🔄 New Quote button for fresh inspiration.

Pomodoro – Hit Start to begin a focus session. The timer auto‑switches to break mode. Use Reset to go back to 25:00.

Habits – Click any habit row or the checkbox to mark it complete. Streaks increase when you complete a habit on consecutive days (resets automatically at midnight).

Notes – Type anything; content is saved 500ms after you stop typing or when the textarea loses focus.

Theme – Click the sun/moon button in the header to toggle light/dark mode.

Links – All external links open in a new tab.

🗂️ File Structure
text
polymath-dashboard/
└── index.html          # Single file containing all HTML, CSS, and JavaScript
No external assets, fonts, or libraries – everything is self‑contained for easy deployment.

🎨 Customisation
Modify the quote collection
Open index.html, find the QuotesModule array (around line 480), and add / remove quotes:

javascript
{ text: "Your custom quote", author: "Your Name" }
Change habits
Locate defaultHabits in the HabitsModule (approx. line 550):

javascript
{ id: 'your-id', name: '🏋️ Gym 1h', completed: false, streak: 0 }
Adjust Pomodoro durations
Look for WORK_DURATION and BREAK_DURATION (approx. line 660):

javascript
const WORK_DURATION = 25 * 60;   // 25 minutes
const BREAK_DURATION = 5 * 60;   // 5 minutes
Update link hub
Edit the <ul class="links__list"> section (around line 250) – add or remove list items.

💾 Data Persistence
All user data is stored in the browser's localStorage:

Key	Content
polymath_habits	Habits array (completed & streak)
polymath_habits_date	Last saved date (used for daily reset)
polymath_notes	Raw text from the notes area
polymath_theme	"light" or "dark"
Note: Clearing browser storage will reset all data.

☁️ Deployment to GitHub Pages
Push your code to a GitHub repository.

Go to the repository Settings → Pages (left sidebar).

Under Branch, select main (or master) and the / (root) folder.

Click Save.

After a few minutes, your dashboard will be live at:
https://your-username.github.io/polymath-dashboard/

✅ Because the dashboard is a single index.html, no extra configuration is needed.

🤝 Contributing
Contributions, issues, and feature requests are welcome!
Feel free to check the issues page.

Fork the project

Create your feature branch (git checkout -b feature/amazing)

Commit your changes (git commit -m 'Add some amazing feature')

Push to the branch (git push origin feature/amazing)

Open a Pull Request

📄 License
Distributed under the MIT License. See LICENSE file for more information (you can add a simple MIT license file if desired).

🙏 Acknowledgements
Inspired by the polymath spirit of Leonardo da Vinci and modern productivity systems.

Built with vanilla web technologies – no frameworks, just focus.

Made with ☕ and 🧠 by Affan
Keep learning, keep building.