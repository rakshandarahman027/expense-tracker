# Expense Tracker

A browser-based personal expense tracker that logs spending across multiple payment methods (cash, Octopus, Alipay, Mastercard, Visa) and visualises where the money goes.

**Live demo:** https://rakshandarahman027.github.io/expense-tracker/
**Repo:** https://github.com/rakshandarahman027/expense-tracker

## Why I built this

I pay for things using too many different methods — cash, Octopus, Alipay, card — and I had no idea where my money actually went each month. Spreadsheets were too much friction, so I built a single-page tool I could actually use every day.

## What it does

- **Log an expense** — amount, payment method, category, optional note
- **See the running list** — newest first, with date, amount, method, category and note
- **Totals at a glance** — all-time total and this-month total
- **Filter by payment method** — e.g. only show Octopus spending
- **Summary by method** — how much went on cash vs Octopus vs Alipay vs card
- **Spending charts** — category breakdown, payment method breakdown, and daily spend over the last 30 days
- **Calendar view** (October 2026) — daily totals, with high-spend days highlighted
- **Clear all** — with confirmation

## What I found in my own data

After logging my own expenses for two weeks, three patterns stood out:

1. **Food was the largest category**, taking up a much bigger share of my spending than I expected. Seeing it charted made the habit visible in a way a bank statement never did.
2. **Weekend spending ran roughly 3× higher than weekdays** — small daily purchases during the week, then bigger one-off spends on Saturdays and Sundays.
3. **Octopus was my second-largest payment method** — I had assumed it was a minor top-up card, but the chart showed it was a significant share of my monthly spend.

These findings changed how I budget: I now set a weekly cap on food and check the daily-spend chart before the weekend.

## How it works

- **Single file:** everything (HTML, CSS, JavaScript) lives in `index.html`. No frameworks, no libraries, no build step, no installs.
- **Data storage:** expenses are saved in the browser via `localStorage`. They survive a refresh and closing the tab, but they do **not** sync across devices — each browser has its own list.
- **Hosting:** served as a static site via GitHub Pages.

## Known limitations (honest scope)

- **No cross-device sync.** Data lives in one browser. A future version would use a cloud database.
- **No editing or deleting individual expenses** yet — only "clear all."
- **No authentication or user accounts.**
- **Calendar is hardcoded to October 2026** for demonstration. A real version would have previous/next month navigation.
- **No CSV export** yet.

## Tech

- Vanilla HTML, CSS, JavaScript
- `localStorage` for persistence
- GitHub Pages for hosting
- Built with AI-assisted development (vibe coding) — see below

## How I built it

This project was built using an AI-assisted workflow:

1. **Plan first** — I described the tool in plain English and asked the AI for a plan before any code.
2. **One commit per idea** — initial build, then one feature at a time, so the Git history reads like a story.
3. **A deliberate bug, then a fix** — I asked the AI to skip input validation on the first pass, so the empty-amount crash was a real bug to demo and fix in a separate commit.
4. **Hand-checked output** — AI sometimes leaked markdown formatting into the code; I checked and cleaned each file before committing.

## Commit history

1. Add first version of expense tracker
2. Add monthly total and clear all button
3. Fix crash when amount is empty or zero
4. Add summary by payment method
5. Add spending charts for visual analysis
6. Add October 2026 calendar view

## Running it locally

Clone the repo and open `index.html` in any browser. That's it.

