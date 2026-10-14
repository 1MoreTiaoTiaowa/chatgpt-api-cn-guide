# 常见问题 | FAQ

## ChatGPT API 国内怎么充值？

注册 [Midalo](https://model.midalo.ai/) 后，在「钱包」页使用支付宝或微信充值即可，人民币结算，无需外币卡和海外账户。

## 有免费额度吗？

有新用户注册后，联系客服 QQ **480419379** 发送你的用户 ID，即可免费领取 **$1 体验额度**。

## Claude Code 能用吗？

可以。本站支持 Anthropic 原生协议（`/v1/messages`），按 [客户端接入教程](clients.md) 中的 Claude Code 一节配置两个环境变量即可使用。提供多种 Claude 线路分组（含满血 MAX20 号池），可按需选择。

## 支持哪些模型？

Claude 全系、GPT 全系（含 gpt-image-2 生图）、Gemini 全系、DeepSeek、GLM、Kimi、Grok，以及 Seedance、MiniMax 视频生成模型。完整列表见 [模型列表与价格](models.md) 或站内 [实时价格页](https://model.midalo.ai/pricing)。

## API 调用失败 / 报错怎么办？

按以下顺序排查：

1. **检查 base_url**：应为 `https://model.midalo.ai/v1`，不要多写或少写路径（Claude Code 除外，它用根地址）
2. **检查令牌分组**：你的 Key 绑定的分组需要包含所调用的模型
3. **检查余额**：在「钱包」页确认额度充足
4. **查看日志**：站内「日志」页有每次请求的详细错误信息
5. 仍无法解决请联系客服 QQ：**480419379**

## 不同分组有什么区别？

同一模型在不同分组下走不同线路，价格和稳定性不同。例如 Claude 有满血号池、独享 20x、Kiro Pro、Kiro 低价线路；GPT 有 Pool、Pro、Team-Plus 分组。创建令牌时选择分组，价格最低的线路可省 50% 以上。详见 [模型列表与价格](models.md)。

## DeepSeek 峰谷计价是怎么回事？

deepseek-v4.1-flash 按时段自动半价：工作日 18:00–次日 9:00、12:00–14:00，以及周末全天（北京时间）均为 5 折，无需任何操作，系统自动按时段结算。

## 视频生成模型怎么计费？

Seedance 按秒计费（单价 × 视频秒数，请求中 `seconds` 必填）；MiniMax H3 和 seedance-2.5-fixed 按次计费，每条固定价与秒数无关。成片请在 24 小时内下载。详见 [模型列表与价格](models.md)。

## 中转站安全吗？我的数据会被保存吗？

本站仅做请求转发，不存储对话内容。但作为通用安全建议，请不要在任何第三方 API 服务中发送账号密码、私钥等敏感凭据信息。

## 企业采购 / 官方渠道需求？

提供企业官方 Key 线路（AWS / Azure / OpenAI / Anthropic 等企业蒸馏渠道），有对公需求请联系客服 QQ：**480419379**。
