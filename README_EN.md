# 🎯 Author Info Skill

Agent Skill for storing and retrieving author information.

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/yancongya/author-info-skill?style=flat)](https://github.com/yancongya/author-info-skill/stargazers)

---

## 💡 The Problem

In daily development, we often need to deal with author information:

- 📝 Writing README docs requires adding author contact
- 🌐 Building websites needs author info in navigation
- 📄 Writing open source project docs needs author bio
- 💰 Want to show donate/sponsor methods

Manually copying and pasting the same information every time is tedious!

## ✨ The Solution

With this Skill, AI can automatically get your author info:

- Just tell AI *"Here's my author info"* or *"Get author info"*
- AI will automatically read config from `skills/author-info/data/`
- No more manual input, saves time!

---

## 📖 Usage Guide

### 1. Fork the Project

Click [Fork](https://github.com/yancongya/author-info-skill/fork) to fork this repository to your GitHub account.

### 2. Modify Author Info

Edit files in `skills/author-info/data/`:

| File | Description |
|------|-------------|
| `author.json` | Name, bio, email, location |
| `links.json` | GitHub, Bilibili, Xiaohongshu, blog links |
| `donate.json` | Alipay, WeChat, Afdian donate methods |
| `resources/` | Avatar, QR codes images |

### 3. Install to IDE

Copy the modified `skills` folder to IDE config directory:

| IDE | Path |
|-----|------|
| Cursor | `%APPDATA%/Cursor/skills/` |
| Claude Code | `%APPDATA%/Claude/skills/` |
| Windsurf | `%APPDATA%/Windsurf/skills/` |

> 💡 You can also use [skills-npm](https://github.com/antfu/skills-npm) for auto-linking

### 4. Start Using

Just ask in your IDE:
- *"Get author basic info"*
- *"What's author's GitHub"*
- *"How to donate to author"*

---

## 📁 Project Structure

```
skills/author-info/
├── SKILL.md              # Skill definition
└── data/
    ├── author.json       # Basic info
    ├── links.json        # Social links
    ├── donate.json       # Donate methods
    └── resources/        # Image resources
```

---

## 🌐 中文版

[README.md](README.md)

---

## 📄 License

MIT License © 2024 [Tycon](https://github.com/yancongya)
