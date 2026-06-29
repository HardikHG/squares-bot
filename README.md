
# 🌿 green-squares-bot

> **An automated GitHub Actions bot that maintains consistent contribution graph activity through scheduled commits.**

![GitHub Workflow Status](https://img.shields.io/badge/GitHub%20Actions-Auto%20Commit%20Bot-brightgreen?logo=github)

---

## 💡 What is `green-squares-bot`?

**green-squares-bot** is a production-ready bot that automatically generates commits to maintain an active GitHub contribution graph. It uses GsitHub Actions to schedule daily commits across multiple time zones, providing consistent activity tracking and historical records of all operations.

This project automates routine commit generation tasks through **GitHub Actions**, scheduled workflows (CRON), and Git operations — delivered as a reliable, transparent automation tool.

---

## Features

- 🔁 **Automated Commits on Variable Days**  
  Generates 3 to 5 commits per week on randomly selected days for natural activity distribution.

- **Multiple Commits per Day**  
  Produces between 3 to 15 commits per day with realistic variation patterns.

- 🕒 **Distributed Scheduling**  
  Scheduled runs throughout the day (Morning, Afternoon, Evening) to distribute activity naturally.

- 🧠 **Human-like Commit Messages**  
  Uses randomly selected messages and patterns to simulate organic development activity.

- 📜 **Commit History Logging**  
  Maintains detailed logs in `commit_log.txt` for operational tracking and auditing.

- **Production-Ready**  
  Designed for reliable, continuous operation with automated error handling and push conflict resolution.

---

## ⚙️ How It Works

This project uses a `commit.py` Python script executed through a scheduled GitHub Actions workflow (`.github/workflows/activity.yml`).

The workflow runs daily at three times:

- 🌅 **Morning:** `06:00 UTC` (11:30 AM IST)  
- 🌞 **Afternoon:** `12:00 UTC` (5:30 PM IST)  
- 🌙 **Evening:** `15:45 UTC` (9:15 PM IST)  

Each run performs:

1. 🧾 Git checkout  
2. ⚙️ Git identity setup  
3. 🎲 Weekly randomization of 3–5 commit days  
4. ✍️ Running `commit.py` to generate 3–15 commits on commit days  
5. 🗂️ Updating random files with quotes and messages  
6. 🔄 Pull latest changes with rebase  
7. 📤 Push commits if ahead  

---

## 🚀 Getting Started

### Clone the repo:

```bash
git clone https://github.com/YOUR_USERNAME/green-squares-bot.git
cd green-squares-bot
```

### Push to your own GitHub repository:

```bash
git git remote rm origin
git remote add origin https://github.com/YOUR_USERNAME/green-squares-bot.git
git branch -M main
git push -u origin main
```

Make sure the repository is **public** so commits show up on your GitHub profile contribution graph!

---

## 🔧 File Structure

```
green-squares-bot/
├── commit.py             # Main commit generator script
├── daily_log.txt         # Rotating dummy file
├── progress.md           # Rotating dummy file
├── inspiration.txt       # Rotating dummy file
├── commit_log.txt        # Records commit history
└── .github/
    └── workflows/
        └── activity.yml  # GitHub Actions workflow
```

---

## 🤝 Contributing

Contributions are welcome! 🎉  
If you have ideas for:
- Better commit logic  
- Cool new features  
- Code cleanup or optimization  
