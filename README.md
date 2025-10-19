# AI聊天助手 - 智能对话平台

一个现代化的AI聊天助手前端应用，支持多种AI API提供商，采用豆包黑白风格设计。

## 功能特性

- 🎨 现代化的豆包黑白风格界面
- 🔌 支持多种AI API提供商（白山云、OpenAI、自定义API）
- 💬 流畅的对话体验，支持打字机效果
- 💾 本地存储配置，无需重复输入API密钥
- 📱 响应式设计，支持移动端和桌面端
- 🔄 实时连接测试，确保配置正确
- 📤 对话导出功能

## 支持的API提供商

### 1. 白山云AI
- 国内AI服务提供商
- 访问速度快，中文优化
- 注册地址：http://ai.baishan.com/account/index

### 2. OpenAI
- 国际领先的AI服务
- 功能强大，支持多种模型
- 注册地址：https://platform.openai.com

### 3. 自定义API
- 支持任何兼容OpenAI格式的API
- 可自定义请求头和模型参数

## 快速开始

### 方法一：直接使用
1. 将上面的HTML代码保存为 `index.html`
2. 用浏览器打开该文件
3. 按照界面指引配置API密钥
4. 开始聊天

### 方法二：部署到静态网站

#### GitHub Pages
1. Fork本仓库或创建新仓库
2. 将HTML文件上传到仓库
3. 在仓库设置中启用GitHub Pages
4. 访问生成的URL即可使用

#### Vercel部署
1. 安装Vercel CLI: `npm i -g vercel`
2. 在项目目录运行: `vercel`
3. 按照提示完成部署

#### Netlify部署
1. 将项目文件拖拽到Netlify部署区域
2. 或连接Git仓库自动部署

### 方法三：Docker部署

创建 `Dockerfile`:
```dockerfile
FROM nginx:alpine
COPY . /usr/share/nginx/html
EXPOSE 80