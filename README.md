# 📚 英语学习助手

单页英语学习应用：CET-4（3739 词）/ CET-6（2078 词）/ 托业 TOEIC（1200 词）完整词库，支持自定义词库导入、卡片学习、测验、英汉互译、错题本与进度统计。

## 文件结构

```
english-learning/
├── index.html      # 应用主页面（全部功能 + 内置三大词库，双击即可使用）
└── data/           # 三个词库的独立 JSON 文件（备用，页面已内嵌同份数据）
```

> `index.html` 已把 CET-4 / CET-6 / 托业三个完整词库内嵌在文件中，
> **双击即可直接使用**，无需联网、无需本地服务器。

## 本地预览

直接双击 `index.html` 即可使用（推荐 Chrome / Safari / 手机浏览器）。

## 📱 部署到手机可访问的网址（GitHub Pages）

1. 注册/登录 [GitHub](https://github.com)
2. 点击右上角 **+ → New repository**，名称如 `english-learning`，选择 **Public**，创建
3. 在仓库页面点击 **uploading an existing file**，把 `index.html` 和整个 `data` 文件夹拖进去（可先在本地把 data 文件夹压缩为 zip 上传后在线解压，或使用 Git 命令）
   推荐用 Git：
   ```bash
   git clone https://github.com/你的用户名/english-learning.git
   cd english-learning
   # 把 index.html 和 data/ 复制进来
   git add . && git commit -m "init" && git push
   ```
4. 仓库 **Settings → Pages**，Source 选择 `main` 分支 / 根目录，保存
5. 等待 1~2 分钟，用手机浏览器访问：
   **`https://你的用户名.github.io/english-learning/`**

> 替代方案：也可把整个文件夹拖到 [Netlify Drop](https://app.netlify.com/drop)（需注册）获取网址。

## 功能说明

| 模块 | 说明 |
|---|---|
| 🎴 卡片 | 翻转卡片、点读发音、搜索、按托业单元筛选、认识/不认识标记 |
| ✏️ 测验 | 看英选中 / 看中选英 / 拼写三种题型，自动计分、错题入错题本 |
| 🌐 翻译 | 英汉互译（MyMemory 免费 API，需联网），支持朗读、反向再译 |
| 📥 词库 | 导入 CSV/JSON 自定义词库，可删除；提供示例 CSV 下载 |
| 📊 统计 | 已认识数、错题本、正确率、错题专项测验、进度清空 |

- 进度与导入的词库保存在浏览器本地（localStorage），换设备不同步。
- 内置词库首次加载后缓存在浏览器（IndexedDB），之后离线可用；翻译始终需联网。

## 数据来源

- CET-4 / CET-6：有道词典词库（kajweb/dict 开源整理）
- TOEIC：《新托业词汇本领书（第 3 版）》整理稿（ToeicKeyWords 开源项目）
