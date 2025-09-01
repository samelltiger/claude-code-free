# Claude 配置命令说明

| 命令 | 配置项说明 | 备注 |
|------|------------|------|
| `claude_free`<br/>`claude_free --dangerously-skip-permissions` | 需要配置 `FREE_API_KEY` 变量 | 免费公益的 Claude code 接口网站<br/>注册网址：https://anyrouter.top |
| `claude_kimi`<br/>`claude_kimi --dangerously-skip-permissions` | 需要配置 `KIMI_API_KEY` 变量 | Moonshot Kimi 接口<br/>注册网址：https://www.moonshot.cn/ |
| `claude_taobao`<br/>`claude_taobao --dangerously-skip-permissions` | 需要配置 `TAOBAO_API_KEY` 变量 | 淘宝购买的 Claude 接口<br/>可以自己找店铺或联系微信：ithulianwang<br/>原价 299元/3个月，约5000次请求 |
| `claude_deepseek`<br/>`claude_deepseek --dangerously-skip-permissions` | 需要配置 `DEEPSEEK_API_KEY` 变量 | DeepSeek 接口<br/>注册网址：https://www.deepseek.com/<br/>使用 deepseek-chat 模型 |
| `claude_aicode`<br/>`claude_aicode --dangerously-skip-permissions` | 需要配置 `AICODE_MIRROR_API_KEY` 变量 | AI Code Mirror 接口<br/>注册网址：https://www.aicodemirror.com/register?invitecode=YWJB6R<br/>联系微信：ithulianwang 有优惠 |
| `claude_start`<br/>`claude_start --dangerously-skip-permissions` | 使用当前已设置的配置 | 需要先通过其他命令设置配置<br/>检查当前配置：`claude_status`<br/>清除配置：`claude_clear` |

## 通用命令
- `claude_status` - 显示当前 Claude 配置状态
- `claude_clear` - 清除所有 Claude 配置
- `claude_start` - 使用当前配置启动 Claude（支持参数传递）

## 使用方法
```bash
# 设置配置并启动（支持参数）
claude_free --dangerously-skip-permissions
claude_kimi --dangerously-skip-permissions

# 仅设置配置（不启动）
export ANTHROPIC_AUTH_TOKEN=你的密钥
export ANTHROPIC_BASE_URL=接口地址

# 使用当前配置启动
claude_start --dangerously-skip-permissions
```

所有命令都支持 `--dangerously-skip-permissions` 参数传递。