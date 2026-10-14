# 模型列表与价格 | Models & Pricing

> 以下为主要模型概览，完整实时列表与倍率请访问站内价格页：
> **https://model.midalo.ai/pricing**（JSON 接口：`/api/pricing`）

## Claude 全系

| 模型 | 定位 |
|---|---|
| claude-opus-5-5 / claude-opus-5 | Opus 旗舰，复杂推理与编码 |
| claude-opus-4-5 / 4-6 / 4-7 / 4-8 | Opus 4.x 系列 |
| claude-sonnet-5-5 / claude-sonnet-5 | Sonnet 主力，性价比之选 |
| claude-sonnet-4-5 / 4-6 | Sonnet 4.x 系列 |
| claude-haiku-4-5 | 轻量快速，高并发场景 |
| claude-fable-5 / 5-1 / 5.1 | Fable 系列 |

**Claude 线路分组**（创建令牌时可选）：

| 分组 | 特点 |
|---|---|
| CCMAX 满血号池 | 逆向满配满血 MAX20，带防封提示词注入 |
| CCMAX 独享 20x | 逆向满配满血 MAX20，无注入 |
| Kiro Pro | Kiro Pro 线路，均衡 |
| Kiro 逆向 | 价格最低，效果不做保证 |

## GPT 全系（含生图）

gpt-6 / gpt-6-sol / gpt-6-astra / gpt-6-luna / gpt-6.1-sol / gpt-5.6 / gpt-5.6-sol / gpt-5.6-terra / gpt-5.6-luna / gpt-5.5 / gpt-5.4 / gpt-5.4-mini 等全系模型。

线路分组：GPT-Pool（Pro/Plus 混合）、GPT-Pro（纯 Pro 号池）、GPT-Team-Plus（价格最低）。

**生图模型 gpt-image-2**（按张计费，与画质无关）：

| 尺寸 | 价格 |
|---|---|
| 方图（1024×1024 / 1:1 / auto） | $0.2 / 张 |
| 横图、竖图及其他比例 | $0.25 / 张 |

## Gemini 全系

gemini-3.8-flash / 3.7-flash / 3.6-flash / 3.5-flash / 3.1-pro-preview / 3.1-flash-lite / 3-pro-preview / 3-flash-preview / gemini-4-argon / 2.5-flash 等。

- 双通道：Antigravity 通道（支持上下文缓存）、CLI 通道（轻量快速）
- 生图：gemini-3.1-flash-image（$0.067 / 张）

## 国产模型

| 厂商 | 模型 | 说明 |
|---|---|---|
| DeepSeek | deepseek-v4.1-flash | 官方 API，**峰谷计价**（夜间/午间/周末半价） |
| 智谱 GLM | glm-5.3 / glm-5.3-flash / glm-5v-turbo | 官方直供 |
| Kimi | kimi-k2.7 / kimi-k2.8-preview / kimi-k3 / kimi-k3-1 | 含 K3 满血分组 |
| xAI | grok-4.5 | 文本 |

## 视频生成

| 模型 | 计费 | 规格 |
|---|---|---|
| seedance-2.0m | 按秒 $0.99/秒 | 720p，5–15 秒 |
| seedance-2.5 | 按秒 $1.51/秒 | 720p，5–30 秒 |
| seedance-2.5-fixed | 按次 | 720p，每条 30 秒 |
| minimax-h3-768p-fixed | 按次 | 768P，最长 15 秒 |
| minimax-h3-2k-fixed | 按次 | 2K（2560×1440），最长 15 秒 |

视频模型支持首尾帧、图片/音频/视频参考，可生成音频，成片请在 24 小时内下载。

## 计费说明

- **按量计费**：用多少扣多少，无月费、无套餐绑定
- **分组倍率**：同一模型在不同线路分组下价格不同，创建令牌时自选
- **DeepSeek 峰谷价**：工作日 18:00–次日 9:00、12:00–14:00 及周末全天半价（北京时间）
- **充值**：支付宝 / 微信，USDT
