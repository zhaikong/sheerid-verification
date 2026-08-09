

# SheerID 学生身份验证服务

🎓 一个基于 Cloudflare Workers 的 SheerID 学生身份验证服务，提供完整的前端界面和后端 API。

## 🌟 功能特点

- ✅ 美观的用户界面，响应式设计
- ✅ 支持多所大学的学生身份验证
- ✅ 学生证图片上传和预览
- ✅ hCaptcha 人机验证
- ✅ 实时验证日志显示
- ✅ 完整的错误处理

## 🚀 在线使用

访问：[https://energygod29.github.io/sheerid-verification/](https://energygod29.github.io/sheerid-verification/)

## 🏗️ 技术架构

- **前端**: HTML + CSS + JavaScript (部署在 GitHub Pages)
- **后端**: Cloudflare Workers (处理 SheerID API 调用)
- **验证**: hCaptcha 人机验证
- **存储**: AWS S3 (学生证图片临时存储)

## 📋 支持的学校

- Massachusetts Institute of Technology (Cambridge, MA)
- Logan University (Chesterfield, MO)

## 🛠️ 本地开发

1. 克隆仓库：
```bash
git clone https://github.com/energygod29/sheerid-verification.git
cd sheerid-verification
```

2. 安装 Wrangler CLI：
```bash
npm install -g wrangler
```

3. 登录 Cloudflare：
```bash
wrangler login
```

4. 部署 Worker：
```bash
wrangler deploy
```

5. 在浏览器中打开 `index.html` 进行测试

## 📝 使用说明

1. 填写个人信息（姓名、邮箱、生日）
2. 选择你的学校
3. 上传学生证照片（最大 1MB）
4. 完成人机验证
5. 点击"开始验证"按钮
6. 等待验证结果

## 🔧 配置说明

Worker 配置文件位于 `wrangler.toml`，主要配置项：

- `PROGRAM_ID`: SheerID 程序 ID
- `SHEERID_BASE_URL`: SheerID API 基础 URL
- `MAX_FILE_SIZE`: 最大文件上传大小限制

**注意**：部署前请在 `index.html` 中搜索 `data-sitekey`，将默认占位符 `10000000-ffff-ffff-ffff-000000000001` 替换为您在 hCaptcha 官网申请的站点密钥。

## 📄 许可证

MIT License

## 🤝 贡献

欢迎提交 Issue 和 Pull Request！

## 📞 联系方式

如有问题，请通过 GitHub Issues 联系。
