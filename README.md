# Jia Liu — Personal Website

仿照 [Harry Yang 个人主页](https://hyang.org/) 风格构建的 Jia Liu 个人学术主页。
原始内容来源：[jialiu.people.ust.hk](https://jialiu.people.ust.hk/)

---

## 文件结构

```
jialiu-website/
├── index.html        # 网站主文件（所有内容均在此文件）
├── profile.jpg       # [待补充] 个人头像（需手动添加）
├── highlight_*.jpg   # [待补充] Highlights 轮播图片（需手动添加）
└── README.md         # 本说明文档
```

---

## 可修改的位置一览

### 1. 基本信息（Hero 区域）— `index.html` 第 ~200 行

| 需修改内容          | 位置说明                                                              |
| ------------------- | --------------------------------------------------------------------- |
| 个人头像            | 将照片命名为 `profile.jpg` 放入目录                                   |
| 姓名                | `<h1>Jia Liu 劉佳</h1>`                                               |
| 职位简介            | `<h1>` 下方的 `<p>` 段落                                              |
| Email 链接          | `href="mailto:jialiu@ust.hk"`                                         |
| CV 链接             | `href="http://jialiu.people.ust.hk/JiaLiu_CV.pdf"`                    |
| Google Scholar 链接 | `href="https://scholar.google.com/citations?user=25p7qyQAAAAJ&hl=en"` |
| LinkedIn 链接       | 找到 `title="[待补充] LinkedIn 链接"` 的 `<a>` 标签，替换 `href="#"`  |

---

### 2. About / 个人简介 — `index.html` 第 ~230 行

- **英文简介**：修改 `class="bio-text"` 段落内的英文文本
- **中文简介**：修改第二个 `class="bio-text"` 段落内的中文文本
- **联系地址**：修改页脚信息中的 `📍 LSK4051...` 一行

---

### 3. Highlights 图片轮播 — `index.html` 第 ~285 行

1. 在目录中放入图片，建议命名：`highlight_1.jpg`、`highlight_2.jpg` 等
2. 找到 `<!-- HIGHLIGHTS CAROUSEL` 和 `END HIGHLIGHTS CAROUSEL -->` 注释，删除这两行注释标记使代码生效
3. 替换 `<img src="highlight_1.jpg">` 等为实际文件名
4. 替换 `<div class="slide-caption">` 内的说明文字
5. 每增加一张图片，在 `<div class="carousel-dots">` 内复制一行 `<div class="dot" ...>` 并更新序号

---

### 4. Funding / 科研经费 — `index.html` 第 ~320 行

在 Funding 卡片的 `<div class="card-desc">` 中，按格式添加：

```html
• 项目名称（资助机构）<br />
```

目前已预填 NSFC 优青和 RGC；其他项目请自行补充。

---

### 5. Teaching / 教学课程 — `index.html` 第 ~340 行

找到 Teaching 卡片，将 `[待补充]` 替换为实际课程，参考格式：

```html
<div class="card-title">Spring 2026</div>
<div class="card-desc">课程编号：课程名称</div>
<a href="课程大纲链接" class="card-link">View Syllabus →</a>
```

---

### 6. Selected Research / 论文列表 — `index.html` 第 ~370 行

找到 `<!-- 论文模板` 注释，取消注释并复制模板，填写实际数据：

```html
<div class="paper-item" data-aos="fade-up">
  <div class="paper-meta">期刊名 年份</div>
  <div class="paper-title">论文标题</div>
  <div class="paper-authors">作者列表</div>
  <div class="paper-links">
    <a href="论文链接">Paper</a>
    <a href="SSRN链接">SSRN</a>
  </div>
</div>
```

---

### 7. Latest News / 最新动态 — `index.html` 第 ~410 行

找到 `<!-- 新闻模板` 注释，取消注释并复制模板：

```html
<div class="news-item" data-aos="fade-up">
  <div class="news-date">Jun 2025</div>
  <div class="news-content">
    新闻内容，可加 <strong>加粗</strong> 和 <a href="#">链接</a>。
  </div>
</div>
```

---

### 8. Opportunities / 招聘信息 — `index.html` 第 ~440 行

三张招聘卡片分别对应 Postdoc、PhD、RA，可修改：

- `<div class="card-desc">` 内的要求描述
- `<a href="mailto:...">` 中的邮箱地址

---

### 9. Team / 团队成员 — `index.html` 第 ~490 行

找到 `<!-- TEAM` 和 `END TEAM -->` 注释，删除注释标记并填写成员：

```html
<div class="team-card">
  <div class="team-name">学生姓名</div>
  <div class="team-role">所在院校 / 身份</div>
</div>
```

---

### 10. 导航栏链接 — `index.html` 第 ~165 行

```html
<nav class="dynamic-island">
  <a href="#about">About</a>
  <a href="#research">Research</a>
  <a href="#news">News</a>
  <a href="#opportunities">Join Us</a>
  <a href="#team">Team</a>
</nav>
```

可修改链接文字或跳转锚点（对应各 section 的 `id` 属性）。

---

### 11. 页脚 — `index.html` 最后 ~20 行

```html
<footer>
  &copy; 2025 Jia Liu. All rights reserved.<br />
  LSK4051, HKUST, Clear Water Bay, Hong Kong
</footer>
```

---

### 12. 主题颜色 — `index.html` 第 ~10 行 `:root`

```css
:root {
  --bg-color: #f5f5f7; /* 页面背景色 */
  --text-primary: #1d1d1f; /* 主文字颜色 */
  --text-secondary: #86868b; /* 次文字颜色 */
  --accent: #0066cc; /* 链接/强调色 */
}
```

---

## [待补充] 内容汇总

以下内容在原始网站中不存在，需要手动补充：

| 内容                    | 位置                 | 优先级    |
| ----------------------- | -------------------- | --------- |
| 个人头像 `profile.jpg`  | 目录根目录           | ⭐⭐⭐ 高 |
| Google Scholar 主页链接 | Hero 区域            | ⭐⭐⭐ 高 |
| 论文列表                | Selected Research 区 | ⭐⭐⭐ 高 |
| 最新动态                | Latest News 区       | ⭐⭐ 中   |
| 教学课程                | Teaching 卡片        | ⭐⭐ 中   |
| Highlights 照片         | Highlights 轮播      | ⭐⭐ 中   |
| 团队成员                | Team 区              | ⭐⭐ 中   |
| 具体基金项目列表        | Funding 卡片         | ⭐ 低     |
| LinkedIn 链接           | Hero 区域            | ⭐ 低     |

---

## 部署到 GitHub Pages

```bash
# 1. 在 GitHub 创建新仓库（例如 jialiu-website）

# 2. 在本目录初始化并推送
cd jialiu-website
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/你的用户名/jialiu-website.git
git push -u origin main

# 3. 在 GitHub 仓库页面：Settings → Pages → Source 选 main 分支 → Save
# 4. 几分钟后即可通过 https://你的用户名.github.io/jialiu-website 访问
```

若使用自定义域名（如 `jialiu.example.com`），在仓库根目录创建 `CNAME` 文件，内容为域名即可。

---

## 技术说明

- **纯静态网页**，无需任何后端或构建工具，直接用浏览器打开 `index.html` 即可预览
- 动画库：[AOS (Animate On Scroll)](https://github.com/michalsnik/aos) via CDN
- 字体：系统默认 sans-serif（与 Apple 设计风格一致）
- 完全响应式，支持移动端
