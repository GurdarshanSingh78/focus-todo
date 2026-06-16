<div align="center">

```
███████╗ ██████╗  ██████╗██╗   ██╗███████╗
██╔════╝██╔═══██╗██╔════╝██║   ██║██╔════╝
█████╗  ██║   ██║██║     ██║   ██║███████╗
██╔══╝  ██║   ██║██║     ██║   ██║╚════██║
██║     ╚██████╔╝╚██████╗╚██████╔╝███████║
╚═╝      ╚═════╝  ╚═════╝ ╚═════╝ ╚══════╝
```

**Your daily command center. Built with intention.**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-focus--todo.vercel.app-7c6eff?style=for-the-badge&logo=vercel&logoColor=white)](https://focus-todo-taupe.vercel.app/)
[![HTML](https://img.shields.io/badge/HTML-Single%20File-e34c26?style=for-the-badge&logo=html5&logoColor=white)](./index.html)
[![No Dependencies](https://img.shields.io/badge/Dependencies-Zero-26d0ce?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-f0b429?style=for-the-badge)](#license)

<br/>

![focus. app screenshot](https://focus-todo-taupe.vercel.app/)

</div>

---

## What is this?

**focus.** is a zero-dependency, single-file productivity app designed for students and builders who want a command center that actually looks as serious as the work they're doing.

No React. No build step. No npm install. One `.html` file — open it, and it works.

> *"Build your day with intention. One task at a time."*

---

## Features

### Task management
- Add tasks with a **category**, **custom time**, and instant keyboard shortcut (`Enter` to submit)
- Toggle tasks complete with a satisfying checkmark animation
- Delete tasks with a single click
- Filter by category — Study, Work, Health, Personal, Urgent, or Done
- Color-coded left-border accent on every task, keyed to its category

### Pomodoro focus timer
- Full **25 / 5 / 25 / 5 / 25 / 5 / 25 / 15** minute cycle (4 work sessions → long break)
- Start, Pause, Resume, Reset, and Skip phase controls
- Session dot indicators track your progress through the 4-session cycle
- Page `<title>` updates live with the countdown while running (`25:00 — focus`)
- Toast notification at every phase transition

### Motivation engine
- 18 hand-picked quotes on discipline, study, and consistency
- Click the quote card to cycle to the next one with a fade transition

### Live stats dashboard
- Completed · Total tasks · Done today (%) · Remaining — updated in real time
- Animated progress bar with a glowing teal indicator dot at the current position

### Design
- Deep space dark theme — `#080810` base with ambient purple/teal radial glows
- `Space Grotesk` display face for numbers and the logo
- `JetBrains Mono` for the live clock, data labels, and category tags
- Micro-interactions: slide-in on add, `translateX` lift on hover, colored glow accents
- Fully responsive down to mobile
- Respects `prefers-reduced-motion`
- Accessible — ARIA roles, keyboard navigation, visible focus rings

### Persistence
- Tasks saved to `localStorage` — survive page refresh and browser restarts
- No account, no server, no data ever leaves your device

---

## Getting started

### Option 1 — Just open it

```bash
# clone the repo
git clone https://github.com/YOUR_USERNAME/focus-todo.git

# open directly in browser — no server needed
open index.html
```

### Option 2 — Deploy to Vercel (recommended)

```bash
git clone https://github.com/YOUR_USERNAME/focus-todo.git
cd focus-todo
```

Then go to [vercel.com](https://vercel.com) → **Add New Project** → import this repo → **Deploy**.

That's it. Vercel detects the static HTML automatically. Your app is live in ~10 seconds.

Every `git push` to `main` triggers an automatic redeploy.

---

## Project structure

```
focus-todo/
├── index.html      # The entire app — HTML + CSS + JS in one file
└── README.md       # This file
```

No `package.json`. No `node_modules`. No config files. No framework.

---

## Keyboard shortcuts

| Key | Action |
|-----|--------|
| `Enter` | Add current task |
| Click quote card | Next motivational quote |
| Click task circle | Toggle complete / incomplete |

---

## Categories

| Category | Color | Use for |
|----------|-------|---------|
| 📚 Study | Purple | Lectures, assignments, reading, revision |
| 💼 Work | Gold | Projects, deadlines, meetings |
| 🏃 Health | Green | Workouts, hydration, sleep |
| ✨ Personal | Rose | Errands, hobbies, self-care |
| 🔥 Urgent | Teal | Anything due today or overdue |

---

## Pomodoro cycle

```
[Work 25m] → [Break 5m] → [Work 25m] → [Break 5m]
[Work 25m] → [Break 5m] → [Work 25m] → [Long Break 15m]
```

After every 4 work sessions the cycle resets. The four dots in the timer section track where you are in the current cycle.

---

## Customization

Everything lives in `index.html`. The design tokens are CSS custom properties at the top of the `<style>` block:

```css
:root {
  --accent:  #7c6eff;   /* primary purple */
  --gold:    #f0b429;   /* work category */
  --teal:    #26d0ce;   /* urgent category */
  --rose:    #f06292;   /* personal category */
  --green:   #56cf94;   /* health category */
  /* ... */
}
```

Change `--accent` to shift the whole app's primary color in one line.

To add your own quotes, find the `quotes` array in the `<script>` block and add objects in the format:

```js
{ t: "Your quote text here.", a: "— Author Name" },
```

---

## Tech stack

| Layer | Choice | Why |
|-------|--------|-----|
| Structure | HTML5 | Zero overhead |
| Styling | Vanilla CSS + custom properties | No build step, full dark mode |
| Logic | Vanilla JS | No framework needed at this scale |
| Fonts | Google Fonts (Space Grotesk + JetBrains Mono + Inter) | CDN, no install |
| Storage | `localStorage` | Private, offline, instant |
| Hosting | Vercel | Free, instant deploys, global CDN |

---

## Browser support

Works in all modern browsers — Chrome, Firefox, Safari, Edge. No polyfills required.

---

## License

MIT — do whatever you want with it.

---

<div align="center">

Built by **Gurdarshan** · [Live at focus-todo-taupe.vercel.app](https://focus-todo-taupe.vercel.app/)

*Stay consistent. Every task counts.*

</div>
