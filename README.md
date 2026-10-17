# PeakPlan — Energy-Based Day Planner

**Stop fighting your energy. Schedule hard tasks when your brain is sharpest.**

PeakPlan is a single-file web app that plans your day around your natural energy rhythm. You tell it when your peak hours are (or pick a chronotype like Morning Lark or Night Owl), dump your tasks into an inbox with an energy demand rating, and tap **Auto-Plan My Day**. Demanding tasks land inside your peak window; easy tasks fill the low-energy dips — with 15-minute breathers between blocks.

Live demo: **https://abhiramunni.github.io/peakplan/**

## Who it's for

Anyone who ends the day wondering where their focus went — students, developers, freelancers, and knowledge workers who want their hardest work done during the hours their brain actually cooperates.

## Features

- **3-step onboarding** — optional name, chronotype picker (Morning Lark / Day Steady / Night Owl / Custom peak hours), and a 30-second "how it works" tour. Runs once, stored locally.
- **Animated energy curve** — a beautiful SVG curve of your day computed from your chronotype and peak hours, with your peak window shaded gold, a pulsing peak marker, hour ticks, and a live "right now" line. It sits right above your schedule so you can see *why* each task landed where it did.
- **Task inbox** — add tasks with title, estimated duration (15/30/45/60/90/120 min chips), priority (Must / Should / Nice), and energy demand (Low / Medium / High). Edit and delete any task.
- **Smart auto-planner** — one tap schedules everything between your wake and sleep times. High-energy tasks are placed into your peak window first, Must-priority tasks before Shoulds and Nices, with zero overlaps and automatic 15-minute gaps. A plain-language summary explains the result ("2 high-energy tasks placed in your 10:00 AM–1:00 PM peak window").
- **Timeline schedule** — vertical timeline of your planned day. Every block shows its time, priority, energy-demand and current-energy badges. Tap a block to start a focus session, mark it done, shift it earlier/later, or send it back to the inbox.
- **Distraction-free focus timer** — fullscreen countdown with a progress ring, pause/resume/reset, and a gentle completion state that offers to mark the task done.
- **Stats dashboard** — today's completion %, tasks completed, "peak-hour hits" (high-energy tasks finished inside your peak window), a 7-day bar chart, and a day streak counter (also shown in the header).
- **Settings** — display name, wake/sleep times, peak-hour editor, chronotype switcher, JSON data export, reset-day, and clear-all-data.
- **Beginner-friendly UX** — helper text under every input, tooltips on non-obvious controls, friendly empty states, and plain-language explanations throughout.
- **Mobile-first, offline-capable** — responsive layout, bottom tab bar, works with no network after first load (only external request is the Inter font).

## How to use

1. **Onboard (first visit only)** — enter your name (optional), pick the chronotype closest to your rhythm, and read the 30-second tour.
2. **Add tasks** — open the Inbox tab, type a task title, pick a duration chip, a priority, and an energy demand. Repeat for everything on your plate.
3. **Auto-plan** — back on the Plan tab, tap **Auto-Plan My Day**. Read the summary to see where things landed and why.
4. **Work the plan** — tap any timeline block to start a focus session, or mark it done when finished. Shift blocks around if your day changes.
5. **Track progress** — the Stats tab updates live: completion %, peak-hour hits, the 7-day chart, and your streak.
6. **Tune** — in Settings, adjust wake/sleep times or your peak window any time your rhythm changes, then re-run Auto-Plan.

## Tech stack

- Vanilla HTML, CSS, and JavaScript — no frameworks, no build step, no backend
- `localStorage` for all persistence (profile, tasks, plan, history)
- Inline SVG for the energy curve, icons, and timer ring — zero external images
- Google Fonts (Inter) via CDN with system-font fallback
- One self-contained `index.html` (~63 KB)

## Data & privacy

Everything stays in your browser's `localStorage` under the key `peakplan_v1`. The app makes **zero network calls** of its own (the only external request is loading the Inter font), has no accounts, no analytics, and no tracking. Use **Download my data (JSON)** in Settings to export everything, or **Clear all data** to wipe it permanently.

## Author

Built by **Abhiram Unni** — https://github.com/abhiramunni
