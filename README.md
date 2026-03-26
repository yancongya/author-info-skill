# 🎯 Author Info Skill

用于存储和检索作者信息的 Agent Skill。

[![MIT License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![GitHub Stars](https://img.shields.io/github/stars/yancongya/author-info-skill?style=flat)](https://github.com/yancongya/author-info-skill/stargazers)

---

## 💡 痛点

在日常开发中，我们经常需要处理作者信息：

- 📝 写 README 文档需要添加作者联系方式
- 🌐 开发网页时导航栏需要展示作者信息
- 📄 编写开源项目文档需要作者简介
- 💰 需要展示打赏/赞助方式

每次都要手动复制粘贴相同的信息，非常麻烦！

## ✨ 解决方案

有了这个 Skill，AI 可以自动获取你的作者信息：

- 只需要告诉 AI *"这是我的作者信息"* 或 *"获取作者信息"*
- AI 会自动读取 `skills/author-info/data/` 中的配置
- 无需重复手动输入，节省时间

---

## 📖 使用指南

### 1. Fork 项目

点击 [Fork](https://github.com/yancongya/author-info-skill/fork) 将项目 fork 到你的 GitHub 仓库。

### 2. 修改作者信息

编辑 `skills/author-info/data/` 下的文件：

| 文件 | 说明 |
|------|------|
| `author.json` | 昵称、简介、邮箱、所在地 |
| `links.json` | GitHub，B站、小红书、博客等链接 |
| `donate.json` | 支付宝、微信、爱发电等打赏方式 |
| `resources/` | 头像、二维码等图片 |

### 3. 安装到 IDE

将修改后的 `skills` 目录复制到 IDE 配置目录：

| IDE | 路径 |
|-----|------|
| Cursor | `%APPDATA%/Cursor/skills/` |
| Claude Code | `%APPDATA%/Claude/skills/` |
| Windsurf | `%APPDATA%/Windsurf/skills/` |

> 💡 也可以使用 [skills-npm](https://github.com/antfu/skills-npm) 自动链接

### 4. 开始使用

在 IDE 中直接提问：
- *"获取作者的基本信息"*
- *"作者的 GitHub 是什么"*
- *"如何打赏作者"*

---

## 📁 项目结构

```
skills/author-info/
├── SKILL.md              # Skill 定义文件
└── data/
    ├── author.json       # 基本信息
    ├── links.json        # 社交链接
    ├── donate.json       # 打赏方式
    └── resources/        # 图片资源
```

---

## 👤 作者

<img src="skills/author-info/data/resources/avatar.webp" width="120" height="120" alt="头像">

- **昵称**: 烟囱鸭
- **简介**: 一个做动画的
- **邮箱**: 2655283737@qq.com
- **所在地**: 广州, 中国
- **GitHub**: [yancongya](https://github.com/yancongya)
- **小红书**: [烟囱鸭](https://xhslink.com/m/9v4RK5HQzsc)
- **B站**: [烟囱鸭](https://space.bilibili.com/100881808/)

---

## 💰 打赏

<p align="center">
  <img src="skills/author-info/data/resources/alipay-qrcode.jpg" width="150" alt="支付宝">
  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
  <img src="skills/author-info/data/resources/wechat-qrcode.jpg" width="150" alt="微信">
</p>

<p align="center">
  <strong>支付宝</strong> &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <strong>微信</strong>
</p>

<p align="center">
  <a href="https://ifdian.net/a/tycon">爱发电</a>
</p>

---

## 🌐 English Version

[README_EN.md](README_EN.md)

---

## 📄 License

MIT License © 2024 [Tycon](https://github.com/yancongya)