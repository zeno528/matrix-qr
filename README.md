# SubQR Hub

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-success?style=flat-square&logo=github)](https://ekko7778.github.io/qrcode-generator/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

订阅链接二维码生成器，支持 Clash / v2rayN / Surge / Shadowrocket / Quantumult 等代理订阅链接。

## 功能特性

- **多链接支持** - 支持批量输入，每行一个链接，一键生成多个二维码
- **超长链接** - 使用 `qrcode-generator` 库，支持超长订阅链接
- **一键粘贴** - 从剪贴板快速粘贴链接
- **快捷键** - `Ctrl + Enter` 快速生成二维码
- **下载功能** - 单独下载每个二维码为 PNG 图片
- **灯罩预览** - 点击二维码可放大查看
- **深色主题** - 现代玻璃拟态设计风格
- **响应式布局** - 完美适配移动端

## 使用方法

1. 打开 [SubQR Hub](https://ekko7778.github.io/qrcode-generator/)
2. 粘贴订阅链接到输入框
3. 点击「生成二维码」按钮
4. 点击二维码可放大预览
5. 点击下载按钮保存二维码图片

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

Made with by [Ekko](https://github.com/Ekko7778)
