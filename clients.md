# 客户端接入教程 | Client Setup Guides

凡是支持自定义 API 地址的工具，都可以接入 Midalo。以下是常用工具的配置方法。

## Claude Code

本站支持 Anthropic 原生协议，Claude Code 可直接接入：

```bash
export ANTHROPIC_BASE_URL="https://model.midalo.ai"
export ANTHROPIC_AUTH_TOKEN="sk-你的密钥"
claude
```

Windows（PowerShell）：

```powershell
$env:ANTHROPIC_BASE_URL="https://model.midalo.ai"
$env:ANTHROPIC_AUTH_TOKEN="sk-你的密钥"
claude
```

> 建议在创建令牌时选择 Claude 专用分组（CCMAX 满血号池 / Kiro Pro），体验更稳定。

## Cursor

1. 打开 Settings → Models
2. 找到 OpenAI API Key 部分，启用 Override OpenAI Base URL
3. 填入：
   - Base URL：`https://model.midalo.ai/v1`
   - API Key：`sk-你的密钥`
4. 添加要使用的模型名（如 `gpt-5.6`、`claude-sonnet-5`）

## Cherry Studio

1. 设置 → 模型服务 → 添加服务（选择 OpenAI 兼容类型）
2. 填入：
   - API 地址：`https://model.midalo.ai/v1`
   - API Key：`sk-你的密钥`
3. 点击「管理」拉取全部模型列表，勾选需要的模型

## NextChat（ChatGPT-Next-Web）

部署或设置中填入：

- 接口地址（BASE_URL）：`https://model.midalo.ai`
- API Key：`sk-你的密钥`

## Codex CLI

```bash
export OPENAI_BASE_URL="https://model.midalo.ai/v1"
export OPENAI_API_KEY="sk-你的密钥"
codex --model "gpt-5.6"
```

## 沉浸式翻译 / 浏览器插件

在插件设置中选择「自定义 OpenAI 接口」：

- API 地址：`https://model.midalo.ai/v1`
- API Key：`sk-你的密钥`
- 模型：建议用轻量模型如 `gemini-3.1-flash-lite` 或 `claude-haiku-4-5`，翻译速度快且便宜

## LangChain / LlamaIndex 等开发框架

```python
from langchain_openai import ChatOpenAI

llm = ChatOpenAI(
    base_url="https://model.midalo.ai/v1",
    api_key="sk-你的密钥",
    model="claude-sonnet-5",
)
```

任何接受 `base_url` + `api_key` 的框架均可用同样方式接入。

## 其他工具

如果你的工具不在上面的列表里，只要它支持自定义 OpenAI 兼容端点，统一规则是：

```
Base URL:  https://model.midalo.ai/v1
API Key:   sk-你的密钥
Model:     模型列表页中的任意模型名
```

配置有问题？联系客服 QQ：**480419379**，QQ群**389039568**
