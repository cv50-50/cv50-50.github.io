

# 微信防红链接生成器 GitHub Pages 部署指南

## 一、环境准备
### 1.1 项目结构

bash

├── index.html          # 主页面

├── style.css           # 样式表（可选）

└── assets/            # 静态资源

├── qrcode/        # 二维码图片

└── icons/         # Font Awesome 图标


### 1.2 依赖工具
- Git 命令行工具
- GitHub 账号
- 文本编辑器（推荐 VS Code）

## 二、部署步骤
### 2.1 创建 GitHub 仓库

bash

在终端执行（替换 yourusername）

mkdir wechat-safe-link

cd wechat-safe-link

git init

git add .

git commit -m "Initial commit"


### 2.2 配置 GitHub Pages
1. 进入仓库 **Settings → Pages**
2. 选择分支 `main`
3. 路径填写 `/ (root)`
4. 点击保存

### 2.3 自动部署配置（可选）
在项目根目录创建 `.github/workflows/deploy.yml`：

yaml

name: Auto Deploy

on:

push:

branches: [main]

jobs:

build:

runs-on: ubuntu-latest

steps:

- uses: actions/checkout@v2
- name: Deploy to GitHub Pagesuses: peaceiris/actions-gh-pages@v3with:github_token: ${{ secrets.GITHUB_TOKEN }}publish_dir: ./dist


## 三、核心代码解析
### 3.1 HTML 结构

html

<!-- 响应式容器 -->

<div class="container">

<div class="header">

<h1>微信防红链接生成器</h1>

</div>

<!-- 输入表单 -->

<div class="input-group">

<input type="url" id="targetUrl" placeholder=""https://example.com" (https://example.com)">

<button onclick="generate()">生成链接</button>

</div>

<!-- 结果展示 -->

<div class="result" id="result"></div>

</div>


### 3.2 关键 JavaScript

javascript

// 生成防红链接

async function generate() {

const url = document.getElementById('targetUrl').value;

const response = await fetch('api.php?url=' + encodeURIComponent(url));

const data = await response.json();

// 显示结果

const resultDiv = document.getElementById('result');

resultDiv.innerHTML = `

<p>原始链接: <a href=" {url}"> {url}</a></p>

<p>防红链接: <a href=" {data.safeUrl}"> {data.safeUrl}</a></p>

`;

}


## 四、高级配置
### 4.1 自定义域名
1. 在仓库 **Settings → Pages** 添加 CNAME 记录
2. 在 DNS 管理平台添加解析：

Type: CNAME

Name: @

Value: yourusername.github.io


### 4.2 性能优化

nginx

静态资源缓存配置

location ~* .(css|js|png|jpg|jpeg|gif|ico)$ {

expires 30d;

add_header Cache-Control "public, no-transform";

}


## 五、常见问题
### 5.1 部署失败排查
| 现象 | 解决方案 |
|------|----------|
| 404 错误 | 检查分支名称和文件路径 |
| 样式丢失 | 确认 CSS 文件路径和加载顺序 |
| API 失效 | 检查 `api.php` 文件权限 |

### 5.2 安全建议
1. 使用 HTTPS 加密传输
2. 添加验证码防止滥用
3. 限制 API 调用频率

## 六、效果预览
![界面示意图](https://via.placeholder.com/800x600.png/CCCCCC/FFFFFF?text=Preview+Image)

> 提示：可通过 [51.la](https://js.users.51.la/21969247.js) 添加访问统计

附：Markdown 写作技巧

1. 代码高亮：使用 
"html 或 "bash 指定语言
2. 表格美化：
| 功能       | 说明               |
|------------|--------------------|
| 防红处理   | 自动转换短链接     |
| 二维码生成 | 支持动态刷新       |
3. 流程图：
graph TD
  A[输入链接] --> B{验证协议}
  B -->|HTTPS| C[生成短链]
  B -->|HTTP| D[提示错误]

本指南遵循 "Markdown 最佳实践" (https://github.com/mixu/markdown-cheatsheet)，完整项目可访问 "GitHub 仓库" (https://github.com/yourusername/wechat-safe-link)