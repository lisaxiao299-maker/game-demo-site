# 🎮 游戏项目网页

一个基于 **Jekyll** + **GitHub Pages** 的游戏项目展示网站。

一键推送即可自动部署到 `https://lisaxiao299-maker.github.io/game-demo-site/`。

## 页面功能

| 页面 | 文件 | 说明 |
|------|------|------|
| 🏠 首页 | `index.md` | 游戏简介 + 截图 + 快速入口 |
| 📖 关于 | `about.md` | 故事背景、玩法、技术栈 |
| 📸 截图 | `screenshots.md` | 游戏截图和动图展示 |
| ⬇️ 下载 | `download.md` | 各平台下载链接 + 系统要求 |
| 📋 更新日志 | `changelog.md` | 版本发布历史 |

## 部署步骤

### 1. 在 GitHub 新建仓库

- 仓库名称任意（如 `my-game`）
- 不需要初始化 README（你会 push 这个）
- **记得设为 Public**（免费用户才能用 GitHub Pages）

### 2. 推送到 GitHub

```bash
# 进入项目目录
cd /mnt/data/game-demo-site

# 初始化为 Git 仓库
git init
git add .
git commit -m "🎉 初始化游戏项目网页"

# 关联远程仓库（改成你的实际仓库地址）
git remote add origin https://github.com/lisaxiao299-maker/game-demo-site.git
git push -u origin main
```

### 3. 开启 GitHub Pages

1. 打开仓库 **Settings** → **Pages**
2. Source 选 **Deploy from a branch**
3. Branch 选 **main**，目录选 **/(root)**
4. 点 **Save**

等待约 **1~2 分钟**，访问：
```
https://lisaxiao299-maker.github.io/game-demo-site/
```

### 4. 个性化修改

所有内容都在 Markdown 文件里，直接改：

- **改标题/描述** → `_config.yml`
- **改首页内容** → `index.md`
- **加截图** → 把图片放到 `screenshots/`，然后改 `screenshots.md`
- **发更新日志** → 改 `changelog.md`
- **发博客** → 在 `_posts/` 新建 `YYYY-MM-DD-标题.md`

### 5. 关联 GitHub Releases

下载页面的下载链接指向 GitHub Releases。当你在仓库发布新版本后，下载链接自动生效。

## 本地预览（可选）

如果装了 Ruby：

```bash
gem install bundler
bundle install
bundle exec jekyll serve
```

然后打开 http://localhost:4000 预览。

## 主题

使用 [jekyll-theme-hacker](https://github.com/pages-themes/hacker)，暗色调，适合游戏展示。

> 想换主题？修改 `_config.yml` 中的 `theme:` 行，支持的列表见 [GitHub Pages Supported Themes](https://pages.github.com/themes/)。
