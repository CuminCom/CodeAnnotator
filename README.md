# 🤖 AI 通用代码注释生成器

一键为你的代码添加高质量注释，支持 20+ 编程语言，兼容多种主流大语言模型（OpenAI、DeepSeek、通义千问、智谱 GLM、Moonshot、百川、本地 Ollama 等）。纯本地运行，你的代码和 API Key 仅在你的机器上处理。

![Python](https://img.shields.io/badge/python-3.8+-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![GUI](https://img.shields.io/badge/GUI-CustomTkinter-ff69b4.svg)

---

## ✨ 功能特性

- 🖥️ **友好的图形界面** —— 基于 `CustomTkinter` 构建，暗色主题，操作直观
- 🌍 **多语言支持** —— 支持 Python、Java、JavaScript、TypeScript、C/C++、Go、Rust、PHP、Ruby、Swift、Kotlin、Shell、SQL、HTML/CSS、Vue、React JSX、Lua、Dart、Scala、Perl 等 20 余种语言
- 🧠 **智能注释生成** —— AI 会理解代码逻辑，仅在复杂业务、算法、接口调用等处添加注释，解释“为什么”和“是什么”，而非逐行翻译
- 🔐 **代码零改动** —— 绝对不改动原有功能代码，只增加注释，保证代码安全
- 🔗 **多模型兼容** —— 预设主流模型及其 API 地址，支持 OpenAI、DeepSeek、通义千问、智谱 GLM、Moonshot、百川、本地 Ollama 等，也可手动填写任意兼容 OpenAI 接口的模型
- 📂 **一键文件选择** —— 图形化浏览选择文件，自动识别编码（UTF-8 / GBK）
- 💾 **自动保存** —— 生成的注释代码会以 `原文件名_annotated.扩展名` 保存，原文件不受影响

---

## 🎮 使用指南

1. **选择编程语言** —— 在下拉框中选择你的代码语言，AI 会根据语言特性生成针对性注释。
2. **选择代码文件** —— 点击“📂 浏览”按钮，选择你要注释的源代码文件。
3. **配置 API**：
   - **API Key**：粘贴你的密钥（对于本地 Ollama，可随意填写，如 `ollama`）。
   - **模型**：从下拉框选择预设模型，**API 地址会自动填充**（支持手动修改）。
   - **API 地址**：通常无需手动填写，选择模型后自动匹配。如需使用自定义端点，可直接修改。
4. **点击“🚀 生成注释”** —— 等待 AI 处理（耗时取决于模型和网络），成功后会在原文件同目录下生成 `*_annotated.*` 文件。

---

## 📋 支持的模型与 API 地址映射

| 模型名称 | 对应 API 地址 |
|---------|--------------|
| `gpt-3.5-turbo`, `gpt-4`, `gpt-4-turbo`, `gpt-4o` | `https://api.openai.com/v1` |
| `deepseek-v4-flash`, `deepseek-v4-pro` | `https://api.deepseek.com` |
| `qwen-max` ,  `qwen-plus` ,  `qwen-turbo` | `https://dashscope.aliyuncs.com/compatible-mode/v1` |
| `glm-4`, `glm-3-turbo` | `https://open.bigmodel.cn/api/paas/v4` |
| `moonshot-v1-8k`, `moonshot-v1-32k` | `https://api.moonshot.cn/v1` |
| `Baichuan4`, `Baichuan3-Turbo` | `https://api.baichuan-ai.com/v1` |
| `llama3`, `qwen:7b`, `mistral`（本地 Ollama） | `http://localhost:11434/v1` |

> 💡 如果你使用的模型不在列表中，只需在下拉框中**手动输入模型名称**，然后手动填写对应的 API 地址即可。

---

## 📁 项目结构

```
.
├── main.py               # 主程序（GUI + 核心逻辑）
└── README.md             # 项目说明文档
```

---

## ⚠️ 注意事项

- **API 调用费用**：使用在线模型会产生相应费用，请留意各平台的计费规则。
- **文件大小**：超大文件可能超出模型的 `max_tokens` 限制，建议拆分处理。
- **网络环境**：部分 API 端点可能需要代理或特定网络环境，请确保能正常访问。
- **本地 Ollama**：需提前安装 Ollama 并下载模型，且保持服务运行。

---

## 🤝 贡献

欢迎提交 Issue 和 Pull Request。如果你希望增加新的模型预设或语言支持，请修改 `MODEL_BASE_URL_MAP` 和 `language_options` 列表。

---

## 🙏 致谢

- 本项目使用 [CustomTkinter](https://github.com/TomSchimansky/CustomTkinter) 构建现代化界面。
- 感谢 [OpenAI](https://openai.com/) 提供的 API 标准，使得兼容众多模型成为可能。
- [DeepSeek](https://deepseek.com/) 在本项目代码编写过程中提供辅助支持。

---

## 📄 License

[MIT License](LICENSE) © 2026
