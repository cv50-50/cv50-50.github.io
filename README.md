# EdgeFNAI 聊天助手

一个现代化的AI聊天助手前端应用，支持EdgeFNAI API，采用黑白极简风格设计。

## 功能特性

- 🎨 **现代化的黑白风格界面**
- 🔌 **支持EdgeFNAI API**
- 💬 **流畅的对话体验**，支持打字机效果
- 📱 **响应式设计**，支持移动端和桌面端
- 🔄 **API密钥文件上传**和手动输入
- 💾 **对话历史管理**
- 📝 **代码块高亮显示**

## 快速开始

### 方法一：直接使用

1. 将HTML代码保存为 `index.html`
2. 用浏览器打开该文件
3. 按照界面指引配置API密钥
4. 开始聊天

### 方法二：部署到静态网站

#### GitHub Pages

1. 创建新仓库
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

## API配置

### EdgeFNAI API

- **模型**: `DeepSeek-R1-0528-Qwen3-8B`
- **端点**: `https://api.edgefn.net/v1/chat/completions`
- **认证方式**: `Bearer Token`

## 使用说明

### 1. API密钥设置

- 支持文件上传（`.txt`格式）
- 支持手动输入
- 密钥验证确保配置正确

### 2. 开始聊天

- 输入消息并发送
- 支持实时对话
- 自动滚动到最新消息

### 3. 对话管理

- 清空对话历史
- 返回设置界面重新配置

## 技术特点

- **纯前端实现**，无需后端服务器
- 使用`Fetch API`与EdgeFNAI服务通信
- **响应式设计**，适配各种屏幕尺寸
- 优雅的动画和交互效果
- **代码块语法高亮**支持

## 浏览器兼容性

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 注意事项

- 本应用为**纯前端应用**，API密钥仅用于与EdgeFNAI服务通信
- 对话历史存储在浏览器内存中，刷新页面会清空历史
- 请妥善保管您的API密钥

## 许可证

[MIT License](LICENSE)


MIT License（中英文对照版）

Copyright (c) 2025 EdgeFNAI Chat Contributors  
版权所有 (c) 2025 EdgeFNAI 聊天助手贡献者

Permission is hereby granted, free of charge, to any person obtaining a copy  
of this software and associated documentation files (the "Software"), to deal  
in the Software without restriction, including without limitation the rights  
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell  
copies of the Software, and to permit persons to whom the Software is  
furnished to do so, subject to the following conditions:  

特此免费授予任何获得本软件及相关文档文件（“软件”）副本的人，不受限制地处理  
本软件，包括但不限于使用、复制、修改、合并、出版、分发、再许可和/或销售  
软件的副本，并允许向其提供软件的人这样做，但须满足以下条件：

The above copyright notice and this permission notice shall be included in all  
copies or substantial portions of the Software.  

上述版权声明和本许可声明应包含在软件的所有副本或实质部分中。

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR  
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,  
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE  
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER  
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,  
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE  
SOFTWARE.  

本软件按“原样”提供，不提供任何明示或暗示的保证，包括但不限于  
适销性、特定用途适用性和非侵权的保证。在任何情况下，作者或版权持有人  
均不对任何索赔、损害或其他责任承担责任，无论是在合同诉讼、侵权诉讼或其他诉讼中，  
因本软件或本软件的使用或其他交易而产生、与之相关或与之相关。
