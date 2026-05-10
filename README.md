# 汪汪队九宫格拼图

静态网页游戏，可部署到 **GitHub Pages**，无需后端。

## 在线地址长什么样

开启 Pages 后，游戏网址一般为：

```text
https://你的GitHub用户名.github.io/仓库名/
```

例如：仓库名是 `paw-patrol-puzzle`、用户名是 `zhangsan`，则为：

```text
https://zhangsan.github.io/paw-patrol-puzzle/
```

（首次部署后等待 1～3 分钟再访问；若 404，检查下面「Settings → Pages」是否已保存。）

## 部署到 GitHub Pages（推荐：本文件夹单独做一个仓库）

### 1. 在 GitHub 上新建仓库

1. 打开 [GitHub](https://github.com)，登录后点 **New repository**。
2. **Repository name** 填例如：`paw-patrol-puzzle`（可自定）。
3. 选 **Public**，不要勾选「Add a README」（本地已有文件时可不选）。
4. 点 **Create repository**。

### 2. 把本文件夹推送到 GitHub

在电脑上用 **PowerShell** 进入本目录（`paw_patrol_puzzle`），执行（把 `你的用户名` 和 `仓库名` 换成自己的）：

```powershell
cd D:\Cursor\paw_patrol_puzzle
git init
git add index.html puzzle_source.png README.md 说明.txt
git commit -m "Initial commit: puzzle game"
git branch -M main
git remote add origin https://github.com/你的用户名/仓库名.git
git push -u origin main
```

若你之后会加入背景音乐，再执行：

```powershell
git add paw_patrol_theme.mp3
git commit -m "Add BGM"
git push
```

（没有 `paw_patrol_theme.mp3` 时不必添加；有版权的音频请自行合法取得。）

### 3. 打开 GitHub Pages

1. 打开该仓库页面 → **Settings** → 左侧 **Pages**。
2. **Source** 选 **Deploy from a branch**。
3. **Branch** 选 **main**，文件夹选 **/ (root)** → **Save**。
4. 回到 **Pages** 页面，会显示站点地址（即上面的 `https://用户名.github.io/仓库名/`）。

## 仓库里需要哪些文件

| 文件 | 说明 |
|------|------|
| `index.html` | 主页面（进入页 + 拼图） |
| `puzzle_source.png` | 拼图用原图，须与 `index.html` 同目录 |
| `paw_patrol_theme.mp3` | 可选；主题曲，同目录，无则游戏静音 |

## 本地预览

双击 `index.html`，或在浏览器地址栏输入：

`file:///你的路径/paw_patrol_puzzle/index.html`
