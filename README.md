# 🎯 GitGauge

**GitHub Profile Auditor & Beginner Issue Finder**

GitGauge is a command-line tool that scores a GitHub profile against recruiter-relevant criteria and helps you find beginner-friendly open-source issues to work on. Built entirely with Python's standard library — no `requests`, no third-party libraries — as a way to actually understand what those libraries usually hide.

> **"Audit. Improve. Contribute."**

---

## 🔥 Key Features

- 📊 Scores a GitHub profile out of 100 across weighted criteria
- 🧾 Breaks down exactly where points were earned or lost
- ✅ Prints the top 3 highest-impact fixes for your profile
- 🔍 Searches GitHub for open "good first issue" tickets by language
- 🧮 Ranks issues by approachability using a hand-written sort
- 💾 Caches lookups locally to avoid burning API rate limits
- 🖥️ Simple interactive CLI menu

---

## 🧠 How It Works

1. Fetches your public repos from the GitHub API
2. Scores your profile on bio presence, repo descriptions, recent activity, stars, and original vs forked repos
3. Ranks your weakest areas and prints the top 3 fixes
4. Searches GitHub for open, beginner-labeled issues in a language you pick
5. Ranks those issues by approachability (comments + age) and sorts them

---

## ⚙️ Tech Stack

- Python 3 (standard library only — `urllib`, `json`, `os`, `datetime`)
- GitHub REST API

---

## 🚀 Getting Started

### Setup

```bash
git clone https://github.com//gitgauge.git
cd gitgauge
export GITHUB_TOKEN=your_token_here
```

Never hardcode your token — it's read from the environment and `.env` is gitignored.

### Run

```bash
python3 main.py
```
GitGauge

Audit a profile
Find issues
Quit


---

## ⚠️ Notes

- Scores are a heuristic I designed, not a prediction — the breakdown shows exactly why you got the score you got
- Caching has no expiry yet, that's coming later
- This is Stage 1 of a bigger project — Stage 2 adds pandas-based cohort comparisons and charts

---

<div align="center">

**GitGauge** — *Audit. Improve. Contribute.*

</div>
