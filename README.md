# 🔒 快点SSL证书SSL证书申请工具 | QuickSSL Certificate Tool

一个现代化的网页版ACME客户端，用于免费申请SSL/TLS证书。支持Let's Encrypt、ZeroSSL、Google Trust Services等多个证书颁发机构。

A modern web-based ACME client for free SSL/TLS certificate applications. Supports multiple Certificate Authorities including Let's Encrypt, ZeroSSL, and Google Trust Services.

## ✨ 特性 | Features

### 🚀 简单易用 | Easy to Use
- 🌐 **纯网页应用** - 无需下载安装，在浏览器中直接使用
- 🎯 **一键操作** - 简化的用户界面，几步即可完成证书申请
- 📱 **响应式设计** - 完美适配桌面和移动设备
- 🔄 **自动填充** - 支持拖拽LOG文件自动恢复配置

### 🛡️ 安全可靠 | Secure & Safe
- 🔓 **开源透明** - 完全开源，代码可审查
- 🚫 **无需注册** - 不需要创建账户或登录
- 🔐 **数据安全** - 私钥仅在本地生成，不会发送到第三方
- 📋 **单文件应用** - 可下载到本地离线使用

### 🌐 功能强大 | Powerful Features
- 🎯 **多域名支持** - 支持单域名、多域名和通配符证书
- 🏢 **多CA支持** - Let's Encrypt、ZeroSSL、Google Trust Services
- 🔑 **多种密钥** - 支持RSA和ECC/ECDSA密钥类型
- ✅ **多种验证** - DNS验证和HTTP文件验证

## 🎨 界面预览 | Interface Preview

### 现代化设计
- 🎨 基于Bootstrap 5的现代化界面
- 🌈 渐变背景和毛玻璃效果
- 📊 可视化步骤指示器
- 🎭 平滑动画和交互效果

### 响应式布局
- 💻 桌面端：宽屏卡片式布局
- 📱 移动端：自适应堆叠布局
- 🖱️ 悬停效果和视觉反馈

## 🚀 快速开始 | Quick Start

### 在线使用 | Online Usage
1. 直接在浏览器中打开 `index.html`
2. 选择证书颁发机构（推荐Let's Encrypt）
3. 配置域名和密钥
4. 完成域名验证
5. 下载证书文件

### 本地使用 | Local Usage
```bash
# 克隆仓库
git clone https://github.com/muzihuaner/ACME-HTML-Web-Browser-Client.git

# 进入目录
cd ACME-HTML-Web-Browser-Client

# 在浏览器中打开
open index.html
```

## 📋 使用步骤 | Usage Steps

### 步骤1️⃣：选择证书颁发机构
- **Let's Encrypt** - 最受欢迎，无需额外配置
- **ZeroSSL** - 需要EAB凭据
- **Google Trust Services** - 需要EAB凭据
- **自定义** - 手动输入ACME服务URL

### 步骤2️⃣：证书配置
- 📝 **域名配置** - 输入要申请证书的域名
- 🔑 **证书私钥** - 选择RSA或ECC密钥类型
- 👤 **账户私钥** - ACME账户标识
- 📧 **联系邮箱** - 接收通知邮件

### 步骤3️⃣：域名验证
- 🌐 **DNS验证** - 添加TXT记录（推荐）
- 📁 **HTTP验证** - 上传验证文件

### 步骤4️⃣：下载证书
- 📜 **证书文件** - PEM格式证书链
- 🔐 **私钥文件** - 证书对应的私钥
- 📋 **记录文件** - 完整配置记录

## 🔧 技术规格 | Technical Specifications

### 支持的证书类型
- **RSA证书** - 2048位、3072位、4096位
- **ECC证书** - P-256、P-384、P-521曲线

### 支持的验证方式
- **DNS-01** - DNS TXT记录验证
- **HTTP-01** - HTTP文件验证

### 浏览器兼容性
- ✅ Chrome 60+
- ✅ Firefox 55+
- ✅ Safari 12+
- ✅ Edge 79+

## ⚠️ 重要提醒 | Important Notes

### 证书有效期
- 📅 **免费证书有效期90天**
- 🔄 **需要手动续期**
- 📧 **到期前会收到邮件提醒**

### 安全建议
- 🔐 **妥善保管私钥文件**
- 💾 **备份LOG记录文件**
- 🔄 **定期更新证书**

## 🛠️ 开发信息 | Development

### 技术栈
- **前端框架** - Bootstrap 5
- **图标库** - Bootstrap Icons
- **加密库** - Web Crypto API
- **语言** - HTML5 + CSS3 + JavaScript

### 项目结构
```
ACME-HTML-Web-Browser-Client/
├── index.html  # 主应用文件
├── README.md                          # 项目说明
└── LICENSE                           # 开源协议
```

## 📄 开源协议 | License

本项目采用 [GPL-3.0](LICENSE) 开源协议。

## 🤝 贡献 | Contributing

欢迎提交Issue和Pull Request来改进这个项目！

## 🔧 部署说明 | Deployment

### 静态网站托管
```bash
# 上传到任何静态网站托管服务
# GitHub Pages, Netlify, Vercel, 阿里云OSS等

# 示例：使用Python简单HTTP服务器
python -m http.server 8000
# 然后访问 http://localhost:8000
```

### Nginx配置示例
```nginx
server {
    listen 80;
    server_name your-domain.com;
    root /path/to/ACME-HTML-Web-Browser-Client;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}
```

## ❓ 常见问题 | FAQ

### Q: 为什么图标不显示？
A: 可能是Bootstrap Icons CDN加载失败，工具已内置备用图标方案，会自动切换到Emoji图标。

### Q: 支持哪些域名类型？
A: 支持单域名、多域名、通配符域名，例如：
- `example.com`
- `example.com, www.example.com`
- `*.example.com, example.com`

### Q: 证书申请失败怎么办？
A: 请检查：
1. 域名DNS解析是否正确
2. 验证文件是否可访问
3. 网络连接是否正常
4. EAB凭据是否正确（ZeroSSL/Google）

### Q: 可以离线使用吗？
A: 可以，下载HTML文件到本地即可离线使用，但需要网络连接到ACME服务器申请证书。

### Q: 如何自动续期？
A: 本工具为手动工具，如需自动续期请使用 `acme.sh` 或 `certbot` 等命令行工具。

## 🔄 更新日志 | Changelog

### v1.0.1
- ✨ 全新Bootstrap 5界面设计
- 🎨 现代化渐变背景和毛玻璃效果
- 📱 完全响应式设计
- 🔧 图标备用方案
- 📊 可视化步骤指示器
- ⚡ 性能优化和动画效果

## 📞 支持 | Support

- 🐛 **问题反馈** - [GitHub Issues](https://github.com/muzihuaner/ACME-HTML-Web-Browser-Client/issues)
- 📧 **邮件** - 通过GitHub联系

## ⭐ 致谢 | Acknowledgments

感谢以下项目和服务：
- [Let's Encrypt](https://letsencrypt.org/) - 免费SSL证书服务
- [Bootstrap](https://getbootstrap.com/) - 前端框架
- [ACME协议](https://tools.ietf.org/html/rfc8555) - 自动化证书管理
- [Bootstrap Icons](https://icons.getbootstrap.com/) - 图标库

---

**如果这个项目对您有帮助，请给个⭐Star支持一下！**

**If this project helps you, please give it a ⭐Star!**
