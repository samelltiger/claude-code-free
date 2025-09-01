# Claude Code Free - 低成本 AI 助手配置方案

一套 Shell 脚本集合，通过智能混合免费和付费服务，帮助您以显著降低的成本使用 Claude Code 和其他 AI 模型。

[70%成本降幅！不装软件混搭Claude Code，我的年省2500元秘籍](content.md)

## ✨ 特性

- **成本降低**: 相比标准 Claude Code 订阅，成本降低高达 70%
- **多模型支持**: 无缝切换 Claude Code、DeepSeek、Kimi 等多种 AI 模型
- **自动配置**: 简单设置不同模型提供商的 shell 函数
- **故障转移策略**: 基于任务复杂度和服务可用性的智能路由
- **零依赖**: 纯 Shell 脚本，无需额外安装

## 🚀 快速开始

### 前提条件

- 已安装 Node.js 和 npm
- 全局安装 Claude Code CLI:
  ```bash
  npm install -g @anthropic-ai/claude-code
  ```

### 安装步骤

1. **克隆本仓库**:
   ```bash
   git clone https://github.com/samelltiger/claude-code-free
   cd claude-code-free
   ```

2. **配置 API 密钥**:
   编辑 `claude_functions` 文件，将占位符 API 密钥替换为您的实际密钥：
   ```bash
   # 使用 vim 编辑配置文件
   vim claude_functions
   
   # 或使用您喜欢的编辑器
   code claude_functions
   ```

3. **安装配置**:
   ```bash
   # 复制到主目录
   cp claude_functions ~/.claude_functions
   
   # 添加到 shell 配置
   echo '# 加载 Claude 函数' >> ~/.bashrc  # 或 ~/.zshrc
   echo 'if [ -f ~/.claude_functions ]; then' >> ~/.bashrc
   echo '    source ~/.claude_functions' >> ~/.bashrc
   echo 'fi' >> ~/.bashrc
   
   # 重新加载 shell 配置
   source ~/.bashrc  # 或 source ~/.zshrc
   ```

## 📋 可用命令

| 命令 | 描述 | 需要配置 |
|------|------|----------|
| `claude_free` | 免费 Claude Code 服务 | `FREE_API_KEY` |
| `claude_kimi` | Moonshot Kimi 模型 | `KIMI_API_KEY` |
| `claude_taobao` | 淘宝 Claude 接口 | `TAOBAO_API_KEY` |
| `claude_deepseek` | DeepSeek 模型 | `DEEPSEEK_API_KEY` |
| `claude_aicode` | AI Code Mirror 服务 | `AICODE_MIRROR_API_KEY` |
| `claude_start` | 使用当前配置 | 预先配置的设置 |
| `claude_status` | 显示当前配置 | - |
| `claude_clear` | 清除配置 | - |

## 🔧 配置说明

### API 密钥来源

- **免费服务**: [anyrouter.top](https://anyrouter.top)
- **Kimi**: [moonshot.cn](https://www.moonshot.cn/)
- **DeepSeek**: [deepseek.com](https://www.deepseek.com/)
- **AI Code Mirror**: [aicodemirror.com](https://www.aicodemirror.com/register?invitecode=YWJB6R)

### 使用策略

本方案实现了智能的成本节约策略：

1. **复杂任务** (>100 行或多轮迭代): 使用付费 Claude Code 服务
2. **简单任务** (函数重命名、测试生成、错误解释): 使用免费/廉价模型如 DeepSeek 或 Kimi
3. **故障转移**: 如果 Claude 服务不可用，自动切换到替代模型

## 💰 成本分析

- **传统方案**: ~299-699 元/月 的 Claude Code 订阅
- **本方案**: ~299 元/3 个月 (5000 次请求) + 免费模型使用
- **节省**: 年成本降低高达 70%

## 🛠️ 故障排除

### 常见问题

1. **"命令未找到"**: 确保已加载配置文件
2. **API 错误**: 验证 API 密钥是否正确且服务可用
3. **连接问题**: 检查网络连接和服务状态

### 模型兼容性

某些模型可能不支持所有 Claude Code 功能（如工具调用）。脚本会优雅地处理这些问题，提供适当的回退方案。

## 🤝 贡献

欢迎贡献！请随时提交 Pull Request。

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE)。

## ⚠️ 免责声明

本项目提供使用各种 AI 服务的配置脚本。用户需自行负责：
- 从服务提供商获取正确的 API 密钥
- 遵守每个平台的服务条款
- 管理自己的使用成本和限制

## 📞 支持

如有问题或需要支持：
- 提交 [Issue](https://github.com/samelltiger/claude-code-free/issues)
- 通过微信联系: `ithulianwang` (备注 "claude")
- 公众号：
![](images/微信公众号.jpg)

## Claude code价格全场最低
![](./images/claude-code-month-price.png)

---

**注意**: 本项目与 Anthropic、DeepSeek、Moonshot 或其他提到的服务提供商无关。