# 快速开始 | Quick Start

30 秒发出你的第一个 API 请求。所有模型均兼容 OpenAI 接口格式，任何支持自定义 `base_url` 的工具都能直接使用。

## 第一步：获取 API Key

1. 打开 [Midalo 米搭中转站](https://model.midalo.ai/) 注册账号
2. 在「令牌」页创建一个 API Key（形如 `sk-xxx`）
3. 创建时可选择令牌分组，不同分组对应不同线路和价格

> 🎁 新用户注册后联系客服 QQ **480419379** 发送用户 ID，可免费领取 $1 额度。

## 第二步：发起请求

### Python（OpenAI SDK）

```python
from openai import OpenAI

client = OpenAI(
    base_url="https://model.midalo.ai/v1",
    api_key="sk-你的密钥",
)

response = client.chat.completions.create(
    model="claude-sonnet-5",   # 换成 gpt-5.6、gemini-3.1-pro-preview 等任意模型
    messages=[{"role": "user", "content": "你好"}],
)
print(response.choices[0].message.content)
```

### cURL

```bash
curl https://model.midalo.ai/v1/chat/completions \
  -H "Authorization: Bearer sk-你的密钥" \
  -H "Content-Type: application/json" \
  -d '{"model": "gpt-5.6", "messages": [{"role": "user", "content": "Hello"}]}'
```

### Node.js

```javascript
import OpenAI from "openai";

const client = new OpenAI({
  baseURL: "https://model.midalo.ai/v1",
  apiKey: "sk-你的密钥",
});

const res = await client.chat.completions.create({
  model: "gemini-3.1-pro-preview",
  messages: [{ role: "user", content: "Hello" }],
});
console.log(res.choices[0].message.content);
```

## 支持的协议端点

本站同时提供三种原生协议，不只是 OpenAI 格式：

| 协议 | 端点 | 适用场景 |
|---|---|---|
| OpenAI | `POST /v1/chat/completions` | 绝大多数工具和 SDK |
| Anthropic | `POST /v1/messages` | Claude Code 及 Anthropic SDK |
| Gemini | `POST /v1beta/models/{model}:generateContent` | Gemini 原生 SDK |

## 下一步

- 想看有哪些模型和具体价格 → [模型列表与价格](models.md)
- 想接入 Claude Code / Cursor 等工具 → [客户端接入教程](clients.md)
- 遇到报错 → [常见问题 FAQ](faq.md)
