<div align="center">
<img src="./docs/images/logo.png" alt="logo.png" style="zoom:30%;" />

# API CHECK

</div>

> 点击体验 : https://api-check-indol.vercel.app

## 纯前端 API 检测工具

- ✅ **支持各种 OpenAI API 中转服务的测活**

  - 兼容 oneapi、newapi 等中转 OpenAI 格式的 API，全面检测可用性。

- 🔒 **纯前端版本，数据更安全**

  - 所有操作均在前端完成，无需担心网络超时，确保数据安全。

- 📊 **详细的测活数据**

  - 显示响应时间、模型一致性等信息，测试结果一目了然。

- 💾 **无痕与密码管理器支持 (安全加固版)**

  - **移除云端与本地缓存泄漏点**：配置不再以明文形式缓存在本地或发向云端。
  - **原生密码管理器集成**：通过标准的表单 autocomplete 完美兼容主流的 1Password / iCloud Keychain 等原生密码保险箱，自动回填你的 API Key。

- 🌙 **主题和语言切换**

  - **深色/浅色模式**：根据喜好选择适合的主题，保护视力。
  - **多语言支持**：支持中文和英文，满足不同语言需求。

- 🖥️ **多种部署方式**
  - **Vercel 部署**：支持一键部署到 Vercel，方便快捷。
  - **Docker 部署**
  - **Cloudflare 部署**

## 📦开始使用

### vercel 部署

   [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/hilinc/api-check&env=PASSWORD&project-name=api-check&repository-name=api-check)，直接使用 Github 账号登录即可，记得在环境变量页填入后端密码；
2. 部署完毕后，即可开始使用；
3. （可选）部署后端服务 请参考 [详细教程](./docs/vercel.md)。
4. （可选）[绑定自定义域名](https://vercel.com/docs/concepts/projects/domains/add-a-domain)：Vercel 分配的域名 DNS 在某些区域被污染了，绑定自定义域名即可直连。

### docker 部署

1. 一键部署命令

2. ```
   docker run -d -p 13000:13000 \
     -e PASSWORD=you_password \
     -v you_path:/app/data \
     --name api-check ghcr.io/rickcert/api-check:latest
   ```

### cloudflare 部署后端

1. 参考 [详细教程](./docs/cloudflare.md)。
2. 最好绑定自定义域名。

## 📜最近更新

<img src="./docs/images/testing.png" alt="测试" style="zoom:50%;" />

### v2.1.0

🔔 **新特性与优化**

- ✨ **安全优化：彻底移除聊天功能**
  - 不再提供极易泄漏 Key 给第三方的快捷聊天入口，确保只做校验本职工作。
- 🧪 **添加实验性功能模块** from [elfmaid](https://linux.do/u/elfmaid)
  - 批量测试 gpt Refresh Tokens
  - 批量测试 claude Session Keys
  - 批量测试 gemini API Keys
- ✂️ **新增粘贴按钮 ** by [fangyuan](https://linux.do/u/fangyuan99)
- 📝 **新增自定义对话验证功能**
  - 快捷prompt测试 by [fangyuan](https://linux.do/u/fangyuan99)

🔧 **优化与修复**

- 🐳 **优化 Dockerfile** 减小镜像体积。

- 🎨 **修复布局问题** 改善界面显示

### v2.0.0

🔔 **全新特性与优化**

- 🌐 **移除传统的明文云端存储/本地存储**
  - **系统级集成**：基于浏览器的 autofill 让系统的密码管理器（如各大浏览器内置功能/macOS 钥匙串等）接管输入框。
  - **安全极客专属**：移除设置面板所有储存功能，防止任何恶意跳转链接窃取配置数据。
- ✨**支持预设参数**
  - **一键配置方便**
  - **快速绑定到 new-api**
- 💻 **支持 Vercel Docker 一键部署**
- 🌙 **新增暗黑模式**
  - **主题切换**：支持深色模式和浅色模式的切换，适应不同环境和用户偏好。
  - **自动适配**：可以根据系统设置自动切换主题，保护您的视力。
- 🌐 **国际化支持**
  - **多语言**：新增国际化支持，现已支持中文和英文。
- 📱 **移动端适配优化**
- 🛠 **其他优化和修复**

### 🧪 版本历史

<details>

### v1.5.0

- 📱 适配手机模式
- 🌙 新增暗黑主题
- 🧠 优化o1模型测试

### v1.4.0

- 🔍 新增温度验证功能
- 📊 新增函数验证功能
- 🔧 优化测试提示

### v1.3.0

- 🔍 新增官方API验证功能
- 🖥️ 支持筛选查询

### v1.2.0

- 🖥️ 添加本地一键运行功能
- 🌐 支持pages在线托管
- 📊 改进测试结果展示

### v1.0.0

- ✨ 支持多模型测试
- 💰 添加额度检查功能
- 📋 实现模型列表获取
</details>

## 📋 功能介绍

- 🧪 测试多个模型的可用性和一致性
- 💰 检查API账户使用额度
- 📋 获取并显示可用模型列表
- 📝 智能提取API信息
- 🖱️ 便捷的复制功能
- 💾 密码管理器无缝支持
- 🌙 主题和语言切换
- 🛠 高级验证功能

  - **官转验证**：验证 API 的真实性，查看系统指纹。
  - **温度验证**：验证模型的随机性和稳定性。
  - **函数调用验证**：测试模型的函数调用能力。

[删除了之前不安全的云储存相关配置及分享链接介绍]

### 🛠 **高级验证功能**

#### 🕵️ 官方API验证

1. 🔄 发送多个相同的请求
2. 📊 分析响应的一致性
3. 🔍 检查系统指纹
4. 🧮 计算相似度得分

#### 🕵️‍♀️ 温度验证

1. 🧊 设置低温度参数（0.01）
2. 🔄 发送多个相同的请求（计算某个指定序列的下一个数）
3. 🎯 根据官方api参考值，检测命中率

### 🛠生成报告

<img src="./docs/images/report.png" alt="上测试报告" style="zoom:50%;" />

## 🤝 贡献

欢迎提出建议和改进！随时提交 pull requests 或开启 issues。让我们一起让这个工具变得更棒！ 🌈

## 📜 许可证

本项目采用[Apache](https://opensource.org/license/apache-2-0)文件。

## 🙏 致谢

特别感谢以下贡献者，他们的努力使这个项目变得更好：

- [Rick](https://linux.do/u/rick)
- [Megasoft](https://linux.do/u/zhong_little)
- [fangyuan99](https://linux.do/u/fangyuan99)
- [juzeon](https://github.com/juzeon)

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=hilinc/api-check&type=Date)](https://star-history.com/#hilinc/api-check&Date)
