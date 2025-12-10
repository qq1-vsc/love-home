# VV & 圈圈的幸福小屋 (Web 3D 版)

这是一个基于 Web 3D (Three.js) 的情侣互动网页应用，无需后端服务器，直接在浏览器运行。

## 🚀 快速开始

1. **打开项目**:
   - 推荐使用 VS Code 安装 "Live Server" 插件。
   - 右键点击 `index.html` -> "Open with Live Server"。
   - 或者直接双击 `index.html` 打开 (部分浏览器可能会限制模块加载，推荐使用本地服务器)。

2. **首次配置**:
   - 打开网页后，点击右上角的 **"⚙️ 设置"** 按钮。
   - **Gemini API Key**: 输入你的 Google Gemini API Key (用于 AI 对话)。
   - **Firebase Config**: 输入你的 Firebase 项目配置 JSON (用于数据同步)。
   - **在一起的日期**: 选择你们的纪念日。
   - 点击 "保存并重启"。

## 🛠️ 技术栈

- **核心**: HTML5 单文件应用
- **3D 引擎**: Three.js (CDN 引入)
- **AI 对话**: Google Gemini API
- **数据同步**: Firebase Firestore
- **样式**: 原生 CSS (粉色温馨主题)

## 📂 文件结构

- `index.html`: 包含所有代码 (HTML, CSS, JS) 的完整文件。

## ✨ 功能列表

1. **3D 场景切换**:
   - 🛏️ **卧室**: 温馨的大床，VV 和 圈圈的小人，还有宠物猫“麻薯”。点击人物可以聊天。
   - 🍳 **厨房**: 冰箱、蛋糕。点击冰箱会有特效。
   - 🎬 **电影房**: 暗色调的观影空间。

2. **互动功能**:
   - **AI 聊天**: 点击场景中的人物 (VV 或 圈圈)，可以进行对话。AI 会根据当前房间和角色设定不同的语气。
   - **想你了**: 点击顶部的 "💕 想你了" 按钮，次数会通过 Firebase 实时同步给对方。
   - **纪念日**: 顶部显示在一起的天数。

## 📝 Firebase 配置指南

如果你还没有 Firebase 项目：
1. 访问 [Firebase Console](https://console.firebase.google.com/) 创建新项目。
2. 创建 **Firestore Database** (选择 "Test mode" 以便快速测试)。
3. 在项目设置中添加一个 "Web App"，复制生成的 `firebaseConfig` 对象。
4. 格式如下：
   ```json
   {
     "apiKey": "AIzaSy...",
     "authDomain": "...",
     "projectId": "...",
     "storageBucket": "...",
     "messagingSenderId": "...",
     "appId": "..."
   }
   ```
