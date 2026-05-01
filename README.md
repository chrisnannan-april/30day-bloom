# 🌸 30天蜕变 · Ruonan

A personal 30-day transformation tracker built for me, by me.
Track training, fasting, sleep, HRV, weight, body fat, and calorie deficit — all in one beautiful PWA.

---

## ✨ Features

- 🌸 **30-flower garden** — each completed day blooms a flower (6 colors rotating)
- 🔥 **Calorie deficit center stage** — auto-calculated from burn vs eat
- 🫁 **VO₂ max tracker** — visualize zones (low / mid / high), see how close you are to ≥38
- ✨ **5-item universal checklist** — works for weekdays, weekends, holidays
- 📊 **10 health metrics tracked** — weight, body fat %, VO₂ max, deep sleep, HRV, RHR, steps, burn, eat, deficit
- 🏆 **16 milestones** — streak / weight / body fat / VO₂ / deficit badges
- 📈 **Smooth trend curves** — 7 metrics with toggleable views
- ⚡ **Apple Health auto-sync** — via iOS Shortcut + URL params (one-tap fill)
- 💾 **Offline-first PWA** — saves data locally, works without internet
- 📱 **Add to Home Screen** — runs like a native iOS app

---

## 🚀 部署到 GitHub Pages(5 分钟)

### 方案 A:网页操作(无需命令行,推荐)

#### 1. 创建 GitHub 仓库
1. 打开 https://github.com/new
2. Repository name: `30day-bloom`(或你喜欢的名字)
3. Visibility: **Public**(GitHub Pages 免费版必须公开)
4. 勾选 **Add a README**
5. 点 **Create repository**

#### 2. 上传文件
1. 进入新仓库,点 **Add file** → **Upload files**
2. 把这 5 个文件拖进去:
   - `index.html` ⭐ 必须叫这个名字
   - `apple-touch-icon.png`
   - `icon-192.png`
   - `icon-512.png`
   - `icon.svg`
3. 底部 Commit message 写 `init: 30 day tracker`
4. 点 **Commit changes**

#### 3. 启用 GitHub Pages
1. 仓库顶部 **Settings** → 左边栏 **Pages**
2. Source 选 **Deploy from a branch**
3. Branch 选 **main** + folder **/ (root)** → **Save**
4. 等 1-2 分钟,刷新页面会出现 URL:
   `https://chrisnannan-april.github.io/30day-bloom/`
5. 这就是你的看板地址!保存好,Shortcut 要用到。

#### 4. iPhone 添加到主屏幕
1. iPhone Safari 打开上面那个 URL
2. 底部分享按钮 → **添加到主屏幕**
3. 名称改为「30 天」或「Bloom」
4. 添加 ✓ — 主屏幕现在有了一个看板图标(就是那朵 7 色花)

---

### 方案 B:命令行操作(快)

```bash
# 1. 进入文件夹(把 5 个文件放在这个目录)
cd ~/30day-bloom

# 2. 初始化 git
git init
git add index.html apple-touch-icon.png icon-192.png icon-512.png icon.svg
git commit -m "init: 30 day tracker"
git branch -M main

# 3. 关联远程仓库(先去 github.com 创建好空仓库)
git remote add origin https://github.com/chrisnannan-april/30day-bloom.git

# 4. 推送
git push -u origin main

# 5. 去 Settings → Pages 启用,选 main 分支 / root
```

---

## 🔄 后续更新看板

**网页方式**:
- 改完本地 `index.html` → 仓库主页 → 拖文件覆盖上传 → Commit → 1 分钟生效

**命令行方式**:
```bash
git add index.html
git commit -m "update: tweak some styles"
git push
```

---

## 📲 配套设置:iOS 快捷指令

部署完看板后,看 **`SHORTCUT-TUTORIAL.md`** 文档配置自动同步。每天 21:00 一点,9 项苹果健康数据全部进看板。

---

## 🎨 自定义

### 改颜色
打开 `index.html`,搜索 `:root {` 找到 CSS 变量,改:
```css
--coral: #FF6B47;     /* 主色,珊瑚橙 */
--sunshine: #FFD23F;  /* 阳光黄 */
--mint: #06D6A0;      /* 薄荷绿 */
--pink: #FF6B9D;      /* 樱花粉 */
```

### 改起始日期
搜索 `PLAN_START`(在 script 里):
```js
const PLAN_START = '2026-05-01'; // 改成你想要的开始日
const TOTAL_DAYS = 30;
```

### 改打卡项
搜 `CHECKLIST_TEMPLATE`,改 5 项内容,emoji,时间标签。

### 改金句
搜 `QUOTES`,在数组里加 / 改 / 删句子。

### 改里程碑
搜 `MILESTONES`,定义自己的徽章解锁条件。

---

## 🛡️ 隐私

- 所有数据仅保存在你设备的浏览器本地存储里
- GitHub Pages 不存任何数据,只托管静态 HTML
- 唯一会"上网"的瞬间是 Shortcut 把数据通过 URL 参数传给页面 — 这个 URL 不会发给任何服务器,只有 Safari 和你的看板看到
- 仓库 Public 是因为 Pages 免费版限制,但**仓库里没有任何个人数据**(只有 HTML 模板和图标)

---

## 🌸 致 30 天后的自己

> *"You're the gardener. Be patient with the bloom."*

Made with ● by Ruonan · MAY 2026
