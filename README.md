# Matrix QR

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-success?style=flat-square&logo=github)](https://ekko7778.github.io/matrix-qr/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

一个简洁的二维码生成工具，支持 WiFi 连接、短信发送、文本等多种场景，也可用于代理订阅链接。

## 功能特性

### 模板支持
- **文本** - 通用文本二维码，支持多行批量生成
- **WiFi** - 扫码即可连接 WiFi，支持 SSID、密码、加密方式配置
- **短信** - 扫码发送短信，预设号码和内容

### 通用功能
- **批量生成** - 文本模板支持多行输入，一键生成多个二维码
- **超长内容** - 使用 `qrcode-generator` 库，支持超长文本
- **快捷键** - `Ctrl + Enter` 快速生成二维码
- **下载功能** - 单独下载每个二维码为 PNG 图片
- **放大预览** - 点击二维码可放大查看
- **深色主题** - 现代玻璃拟态设计风格
- **响应式布局** - 完美适配移动端
- **隐私保护** - 纯前端处理，数据不上传服务器

## 使用方法

1. 打开 [Matrix QR](https://ekko7778.github.io/matrix-qr/)
2. 选择模板类型（文本 / WiFi / 短信）
3. 填写对应信息
4. 点击「生成二维码」按钮
5. 点击二维码可放大预览
6. 点击下载按钮保存二维码图片

## 技术栈

- 纯 HTML / CSS / JavaScript，无框架依赖
- 二维码库：[qrcode-generator](https://github.com/kazuhikoarase/qrcode-generator) (支持超长内容)
- 字体：Inter + JetBrains Mono
- CDN：jsDelivr

## 本地运行

无需安装，直接用浏览器打开 `index.html` 即可使用。

或者使用本地服务器：

```bash
# 使用 Python
python -m http.server 8080

# 使用 Node.js
npx serve .
```

## 许可证

[MIT License](LICENSE)

---

Made with by [Feng](https://github.com/zeno528)
