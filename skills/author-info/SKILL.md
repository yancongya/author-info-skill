---
name: author-info
description: 获取作者信息（昵称、简介、联系方式、社交链接、打赏二维码）。当用户询问作者是谁、联系方式、如何打赏、GitHub链接、作者有哪些项目等场景时触发。
---

# Author Info Skill

用于获取存储在 JSON 文件中的作者信息。

## 数据文件

| 文件 | 说明 |
|------|------|
| `data/author.json` | 基本信息（昵称、简介、邮箱、所在地） |
| `data/links.json` | 社交链接（GitHub、B站、小红书等） |
| `data/donate.json` | 打赏方式（支付宝、微信、爱发电） |
| `data/resources/` | 图片资源（头像、二维码） |

## 触发场景

当用户询问以下问题时，使用此 Skill：
- "作者是谁" / "作者信息" / "获取作者信息"
- "作者的 GitHub 是什么" / "作者博客"
- "如何打赏作者" / "赞助作者"
- "作者的头像/二维码在哪里"
- 编写 README 需要插入作者信息
- 生成网页需要作者联系方式

## 输出格式

根据用户需求，选择合适的格式输出：

### 1. 纯文本
```
昵称：烟囱鸭
邮箱：2655283737@qq.com
GitHub：https://github.com/yancongya
```

### 2. Markdown 表格
```markdown
| 项目 | 内容 |
|------|------|
| 昵称 | 烟囱鸭 |
| 邮箱 | 2655283737@qq.com |
| GitHub | [yancongya](https://github.com/yancongya) |
```

### 3. HTML
```html
<p>昵称：烟囱鸭</p>
<p>邮箱：<a href="mailto:2655283737@qq.com">2655283737@qq.com</a></p>
```

### 4. 图片嵌入（README 等）
```markdown
![头像](skills/author-info/data/resources/avatar.webp)

## 打赏

| 支付宝 | 微信 |
|--------|------|
| ![alipay](skills/author-info/data/resources/alipay-qrcode.jpg) | ![wechat](skills/author-info/data/resources/wechat-qrcode.jpg) |
```

## 使用示例

- "获取作者基本信息" → 读取 `data/author.json`，返回 Markdown 格式
- "作者的 GitHub 是什么" → 读取 `data/links.json`，提取 GitHub 字段
- "如何打赏作者" → 读取 `data/donate.json`，列出打赏方式和二维码
- "在 README 中添加作者信息" → 读取所有 JSON，输出 Markdown 表格格式
- "生成作者介绍页面" → 读取所有 JSON，输出 HTML 格式