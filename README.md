# 🎯 GitGauge — GitHub Profile Auditor & Issue Finder

![Python](https://img.shields.io/badge/Python-3.7%2B-blue?logo=python&logoColor=white)
![Status](https://img.shields.io/badge/Status-In%20Development-yellow)
![License](https://img.shields.io/badge/License-MIT-green)

GitGauge is a command-line tool that audits a GitHub profile, scores it against
recruiter-relevant criteria, and surfaces beginner-friendly open-source issues matched to a
chosen language. It's built entirely with Python's standard library — no third-party
HTTP or data libraries — as a deliberate exercise in understanding what those libraries
normally abstract away.

---

## 📑 Table of Contents

- [Overview](#overview)
- [Key Features](#-key-features)
- [How It Works](#-how-it-works)
- [Tech Stack](#️-tech-stack)
- [Project Structure](#-project-structure)
- [Getting Started](#-getting-started)
- [Usage](#-usage)
- [Scoring Methodology](#-scoring-methodology)
- [Design Decisions](#-design-decisions)
- [Limitations](#-limitations)
- [Roadmap](#-roadmap)
- [License](#-license)

---

## Overview

GitGauge answers two questions for a developer building their portfolio:

1. **"How does my GitHub profile look to a recruiter or hiring manager?"**
2. **"What should I work on next to improve it?"**

It fetches a user's public repos from the GitHub REST API, scores the profile out of 100
across several weighted criteria, prints a prioritized punch list of fixes, and can search
for open "good first issue" tickets in a language of the user's choosing — ranked by how
approachable they look.

---

## 🔥 Key Features

| Feature | Description |
|---|---|
| 📊 Profile Scoring | Scores a GitHub profile out of 100 across weighted criteria |
| 🧾 Breakdown Report | Shows exactly where points were earned or lost, per criterion |
| ✅ Punch List | Prints the top 3 highest-impact fixes, in plain language |
| 🔍 Issue Finder | Searches GitHub for open "good first issue" tickets by language |
| 🧮 Approachability Ranking | Hand-written sort ranks issues by how beginner-friendly they are |
| 💾 Local Caching | Caches profile lookups to avoid unnecessary API calls |
| 🖥️ CLI Menu | Simple interactive menu — audit a profile or find issues |

---

## 🧠 How It Works

1. **Fetch** — Pulls a user's public repos via the GitHub REST API using only `urllib`.
2. **Score** — Evaluates the profile against weighted criteria: bio presence, repo
   descriptions, recent activity, stars, and original (non-fork) work.
3. **Advise** — Ranks criteria by points lost and prints the top 3 as actionable advice.
4. **Search** — Queries GitHub's search API for open, beginner-labeled issues in a chosen
   language.
5. **Rank** — Scores each issue's approachability (comment count + recency) and sorts them
   with a hand-written sorting algorithm.
6. **Cache** — Stores fetched results locally so repeat lookups don't burn API rate limits.

---

## ⚙️ Tech Stack

- **Python 3** — standard library only (`urllib`, `json`, `os`, `datetime`)
- **GitHub REST API** — repos and search endpoints
- No third-party HTTP libraries (`requests`) or data libraries at this stage — by design

---

## 📂 Project Structure
