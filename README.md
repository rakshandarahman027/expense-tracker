# Expense Tracker

A browser-based personal expense tracker. Log what you spend, pick how you paid, and see where your money goes.

**Built with vibe coding** — I described what I wanted in plain English, an AI wrote the code, and I iterated through Git commits to add features and fix bugs.

**Live demo:** https://rakshandarahman027.github.io/expense-tracker/
**Repo:** https://github.com/rakshandarahman027/expense-tracker

## Why I built this

I pay for things using too many different methods — cash, Octopus, Alipay, card — and I had no idea where my money actually went each month. Spreadsheets were too much friction, so I built a tool I'd actually use.

## What it does

- Log an expense — amount, payment method, category, optional note
- See the running list, newest first
- Totals — all-time and this month
- Filter by payment method
- Summary showing how much went on each method
- Clear all (with confirmation)

## How I built it (vibe coding workflow)

1. **Plan first** — I described the tool in plain English and asked the AI for a plan before any code.
2. **One commit per idea** — initial build, then one feature at a time, so the Git history reads like a story.
3. **A deliberate bug, then a fix** — I told the AI to skip input validation on purpose, so the empty-amount crash became a real bug to fix in a separate commit.
4. **Hand-checked the output** — AI sometimes leaked markdown formatting into the code, so I checked and cleaned each file before committing.

## Tech

- One `index.html` — HTML, CSS, JavaScript, no frameworks, no installs
- Data saved in the browser via `localStorage` (survives refresh, but doesn't sync across devices)
- Hosted on GitHub Pages

