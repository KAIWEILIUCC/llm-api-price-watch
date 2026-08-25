<div align="center">

[简体中文](README.md) | [English](README_EN.md)

# LLM API Price Watch

本仓库用于记录主流大模型 API 在不同供应商处的价格和调用限额。

[![Data](https://img.shields.io/badge/data-official%20sources-22c55e?style=flat-square)](#数据口径)
[![Updated](https://img.shields.io/badge/updated-2026--08--25-6366f1?style=flat-square)](#更新状态)
[![Currency](https://img.shields.io/badge/currency-USD%20%7C%20CNY-f59e0b?style=flat-square)](#完整模型目录与价格)
[![PRs](https://img.shields.io/badge/PRs-welcome-ec4899?style=flat-square)](#参与更新)

数据按模型家族整理，包括供应商、模型 ID、输入价格、缓存价格、输出价格和 API Quota，并附有官方来源。

[完整模型目录](#完整模型目录与价格) · [Quota 说明](#quota-说明) · [数据口径](#数据口径) · [参与更新](#参与更新)

</div>

> [!IMPORTANT]
> 价格均为公开刊例价，不包含税费、充值手续费、企业折扣或临时活动。不同地区、上下文长度和服务等级可能采用不同价格；下单前请点击表中的官方来源复核。

## 更新状态

| 项目 | 状态 |
| --- | --- |
| 最近核验 | **2026-08-25** |
| 当前收录 | **26 个模型家族 · 141 个型号 · 259 条供应商记录** |
| 计价基准 | 每 1M Tokens，顺序统一为 **输入 / 缓存命中 / 输出** |
| 汇率处理 | 保留供应商原始币种，不做实时换算 |
| `—` | 供应商未公开、该项不适用，或需在账户控制台查看 |
| Quota | `RPM` 请求/分钟 · `RPS` 请求/秒 · `TPM` Token/分钟 · `TPD` Token/天 · `CC` 并发连接 |

## 完整模型目录与价格

目录按照“模型家族 → 具体型号 → API 供应商”组织。同一个型号的官方 API 和已核验的第三方 API 放在同一张表中；供应商使用的模型 ID、快照版本或 `Pro` 路由保留在“模型 ID”列。

价格沿用供应商原始币种。文本模型默认按每 1M Tokens 计价，顺序为“输入 / 缓存命中 / 输出”；图片、语音、视频和 3D 模型会在价格中注明实际单位。`—` 表示不适用或供应商未公开。

> [!NOTE]
> “已核验的第三方”指能够从公开官网确认模型仍可调用，并能确认价格或 Quota 的平台；无法公开核验的转售商不计入。OpenRouter 展示当前 Models API 返回的最低路由价，实际请求可能因上游路由而变化。

<a id="family-openai-gpt"></a>

<details>
<summary><strong>OpenAI GPT</strong> · 3 个型号 · 9 条供应商记录</summary>

#### gpt-5.6-sol

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [OpenAI](https://openai.com/) | `gpt-5.6-sol` | $4.00 / $0.40 / $20.00 | Tier 1: 500 RPM / 500K TPM | 在售 | [价格与限流](https://developers.openai.com/api/docs/models/gpt-5.6-sol) |
| [Azure OpenAI](https://azure.microsoft.com/products/ai-services/openai-service) | `gpt-5.6-sol` | —（公开 Token meter 暂不可核验） | 需按订阅申请 Quota | 已确认可用 | [模型可用性](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/reasoning) |
| [OpenRouter](https://openrouter.ai/) | `openai/gpt-5.6-sol` | $2 / $0.2 / $10 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/openai/gpt-5.6-sol) · [限流](https://openrouter.ai/docs/faq) |

#### gpt-5.6-terra

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [OpenAI](https://openai.com/) | `gpt-5.6-terra` | $2.00 / $0.20 / $12.00 | 随 Usage Tier 动态变化 | 在售 | [价格与限流](https://developers.openai.com/api/docs/models/gpt-5.6-terra) |
| [Azure OpenAI](https://azure.microsoft.com/products/ai-services/openai-service) | `gpt-5.6-terra` | —（公开 Token meter 暂不可核验） | 需按订阅申请 Quota | 已确认可用 | [模型可用性](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/reasoning) |
| [OpenRouter](https://openrouter.ai/) | `openai/gpt-5.6-terra` | $2 / $0.2 / $12 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/openai/gpt-5.6-terra) · [限流](https://openrouter.ai/docs/faq) |

#### gpt-5.6-luna

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [OpenAI](https://openai.com/) | `gpt-5.6-luna` | $0.20 / $0.02 / $1.20 | Tier 1: 500 RPM / 500K TPM | 在售 | [价格与限流](https://developers.openai.com/api/docs/models/gpt-5.6-luna) |
| [Azure OpenAI](https://azure.microsoft.com/products/ai-services/openai-service) | `gpt-5.6-luna` | —（公开 Token meter 暂不可核验） | 需按订阅申请 Quota | 已确认可用 | [模型可用性](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/reasoning) |
| [OpenRouter](https://openrouter.ai/) | `openai/gpt-5.6-luna` | $0.2 / $0.02 / $1.2 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/openai/gpt-5.6-luna) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-claude"></a>

<details>
<summary><strong>Claude</strong> · 4 个型号 · 19 条供应商记录</summary>

#### claude-fable-5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-fable-5` | $10.00 / $1.00 / $50.00 | 按 Start / Build / Scale 分级 | 在售 | [模型与价格](https://platform.claude.com/docs/en/models/overview) · [限流](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-fable-5` | $10.00 / $1.00 / $50.00 | 按区域与账户动态变化 | 在售 | [模型卡](https://docs.aws.amazon.com/bedrock/latest/userguide/model-card-anthropic-claude-fable-5.html) · [价格](https://aws.amazon.com/bedrock/pricing/) |
| [Google Cloud](https://cloud.google.com/) | `claude-fable-5` | $10.00 / $1.00 / $50.00（Global） | 按项目与区域动态变化 | 在售 | [价格](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-fable-5` | $10.00 / $1.00 / $50.00 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/anthropic/claude-fable-5) · [限流](https://openrouter.ai/docs/faq) |

#### claude-opus-5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-opus-5` | $5.00 / $0.50 / $25.00 | 按 Start / Build / Scale 分级 | 在售 | [价格](https://platform.claude.com/docs/en/about-claude/pricing) · [限流](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-opus-5` | $5.00 / $0.50 / $25.00 | 按区域与账户动态变化 | 在售 | [发布与可用性](https://aws.amazon.com/blogs/machine-learning/introducing-claude-opus-5-on-aws-anthropics-most-capable-opus-model/) · [价格](https://aws.amazon.com/bedrock/pricing/) |
| [Google Cloud](https://cloud.google.com/) | `claude-opus-5` | $5.50 / $0.55 / $27.50 | 按项目与区域动态变化 | 在售 | [价格](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [Microsoft Foundry](https://azure.microsoft.com/products/ai-foundry) | `claude-opus-5` | —（Marketplace / 部署类型 / 区域计价） | 按部署类型与订阅动态变化 | 已确认可用 | [模型可用性](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-opus-5` | $5 / $0.5 / $25 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/anthropic/claude-opus-5) · [限流](https://openrouter.ai/docs/faq) |

#### claude-sonnet-5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-sonnet-5` | $2.00 / $0.20 / $10.00 | 独立模型限流桶 | 在售 | [价格](https://platform.claude.com/docs/en/about-claude/pricing) · [限流](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-sonnet-5` | $2.00 / — / $10.00（推广价至 2026-08-31；其后 $3 / $15） | 按区域与账户动态变化 | 在售 | [价格](https://aws.amazon.com/bedrock/pricing/) · [模型卡](https://docs.aws.amazon.com/bedrock/latest/userguide/model-card-anthropic-claude-sonnet-5.html) |
| [Google Cloud](https://cloud.google.com/) | `claude-sonnet-5` | $2.20 / $0.22 / $11.00（推广价至 2026-08-31） | 按项目与区域动态变化 | 在售 | [价格](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [Microsoft Foundry](https://azure.microsoft.com/products/ai-foundry) | `claude-sonnet-5` | —（Marketplace / 部署类型 / 区域计价） | 按部署类型与订阅动态变化 | 已确认可用 | [模型可用性](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-sonnet-5` | $2 / $0.2 / $10 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/anthropic/claude-sonnet-5) · [限流](https://openrouter.ai/docs/faq) |

#### claude-haiku-4-5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-haiku-4-5` | $1.00 / $0.10 / $5.00 | 按账户等级动态变化 | 在售 | [价格](https://platform.claude.com/docs/en/about-claude/pricing) · [限流](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-haiku-4-5-20251001-v1:0` | $1.00 / $0.10 / $5.00（Global） | 按区域与账户动态变化 | 在售 | [价格](https://aws.amazon.com/bedrock/pricing/) · [模型 ID](https://docs.aws.amazon.com/bedrock/latest/userguide/claude-messages-extended-thinking.html) |
| [Google Cloud](https://cloud.google.com/) | `claude-haiku-4-5` | $1.10 / $0.11 / $5.50 | 按项目与区域动态变化 | 在售 | [价格](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [Microsoft Foundry](https://azure.microsoft.com/products/ai-foundry) | `claude-haiku-4-5` | —（Marketplace / 部署类型 / 区域计价） | 按部署类型与订阅动态变化 | 已确认可用 | [模型可用性](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-haiku-4.5` | $1 / $0.1 / $5 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/anthropic/claude-haiku-4.5) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-gemini"></a>

<details>
<summary><strong>Gemini</strong> · 3 个型号 · 9 条供应商记录</summary>

#### gemini-3.7-flash

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Google AI](https://ai.google.dev/) | `gemini-3.7-flash` | $0.75 / $0.075 / $3.75 | 按项目 Tier，在 AI Studio 查看 | 在售 | [价格](https://ai.google.dev/gemini-api/docs/pricing) · [限流](https://ai.google.dev/gemini-api/docs/rate-limits) |
| [Google Cloud](https://cloud.google.com/) | `gemini-3.7-flash` | $0.75 / $0.075 / $3.75（Global 推广价至 2026-12-31） | 按项目与区域动态变化 | 在售 | [价格](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `google/gemini-3.7-flash` | $0.375 / $0.0375 / $1.875 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/google/gemini-3.7-flash) · [限流](https://openrouter.ai/docs/faq) |

#### gemini-3.5-flash

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Google AI](https://ai.google.dev/) | `gemini-3.5-flash` | $1.50 / $0.15 / $9.00 | 按项目 Tier 动态变化 | 在售 | [价格](https://ai.google.dev/gemini-api/docs/pricing) |
| [Google Cloud](https://cloud.google.com/) | `gemini-3.5-flash` | $1.50 / $0.15 / $9.00（Global） | 按项目与区域动态变化 | 在售 | [价格](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `google/gemini-3.5-flash` | $1.5 / $0.15 / $9 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/google/gemini-3.5-flash) · [限流](https://openrouter.ai/docs/faq) |

#### gemini-3.5-flash-lite

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Google AI](https://ai.google.dev/) | `gemini-3.5-flash-lite` | $0.30 / $0.03 / $2.50 | 按项目 Tier 动态变化 | 在售 | [价格](https://ai.google.dev/gemini-api/docs/pricing) |
| [Google Cloud](https://cloud.google.com/) | `gemini-3.5-flash-lite` | $0.30 / $0.03 / $2.50（Global） | 按项目与区域动态变化 | 在售 | [价格](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `google/gemini-3.5-flash-lite` | $0.3 / $0.03 / $2.5 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/google/gemini-3.5-flash-lite) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-grok"></a>

<details>
<summary><strong>Grok</strong> · 1 个型号 · 2 条供应商记录</summary>

#### grok-4.3

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [xAI](https://x.ai/) | `grok-4.3` | $1.25 / $0.20 / $2.50 | Tier 0: 37 RPS / 10M TPM | 在售 | [价格](https://docs.x.ai/developers/models/grok-4.3) · [限流](https://docs.x.ai/developers/rate-limits) |
| [OpenRouter](https://openrouter.ai/) | `x-ai/grok-4.3` | $1.25 / $0.2 / $2.5 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/x-ai/grok-4.3) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-deepseek"></a>

<details>
<summary><strong>DeepSeek</strong> · 8 个型号 · 28 条供应商记录</summary>

#### DeepSeek V4 Flash

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [DeepSeek](https://www.deepseek.com/) | `deepseek-v4-flash` | $0.14 / $0.0028 / $0.28 | 2,500 CC / account | 在售 | [价格](https://api-docs.deepseek.com/quick_start/pricing) · [限流](https://api-docs.deepseek.com/quick_start/rate_limit/) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `deepseek-v4-flash-ga-260731` | ¥3 / ¥0.1 / ¥9 | 500 RPM / 1M TPM | 正式版 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `deepseek-v4-flash-260425` | ¥1 / ¥0.2 / ¥2 | 15K RPM / 1.5M TPM | 8 月 28 日调价 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V4-Flash` | ¥1 / ¥0.02 / ¥2 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `deepseek-ai/DeepSeek-V4-Flash-0731` | $0.14 / $0.03 / $0.28 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/deepseek-v4-flash-0731` | $0.22 / $0.007 / $0.66 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/deepseek-v4-flash-0731) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v4-flash` | $0.088606 / $0.017721 / $0.177212 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/deepseek/deepseek-v4-flash) · [限流](https://openrouter.ai/docs/faq) |

#### DeepSeek V4 Pro

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [DeepSeek](https://www.deepseek.com/) | `deepseek-v4-pro` | $0.435 / $0.003625 / $0.87 | 500 CC / account | 在售 | [价格](https://api-docs.deepseek.com/quick_start/pricing) · [限流](https://api-docs.deepseek.com/quick_start/rate_limit/) |
| [Together AI](https://www.together.ai/) | `deepseek-ai/DeepSeek-V4-Pro` | $1.74 / $0.20 / $3.48 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [Together AI](https://www.together.ai/) | `deepseek-ai/DeepSeek-V4-Pro-0813` | $1.32 / $0.13 / $3.96 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `deepseek-v4-pro-ga-260813` | ¥9 / ¥0.3 / ¥27 | 500 RPM / 1M TPM | 正式版 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `deepseek-v4-pro-260425` | ¥12 / ¥1 / ¥24 | 15K RPM / 1.5M TPM | 8 月 28 日调价 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V4-Pro` | ¥12 / ¥1 / ¥24 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/deepseek-v4-pro` | $1.74 / $0.145 / $3.48 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/deepseek-v4-pro) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v4-pro` | $0.790308 / $0.065859 / $1.580616 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/deepseek/deepseek-v4-pro) · [限流](https://openrouter.ai/docs/faq) |

#### DeepSeek-OCR

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-OCR` | 免费 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### DeepSeek-R1-0528-Qwen3-8B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-R1-0528-Qwen3-8B` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### DeepSeek-V3.2

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V3.2` | ¥4 / ¥0.4 / ¥6 | 1,000 RPM / 100,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-V3.2` | ¥4 / ¥0.4 / ¥6 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v3.2` | $0.26 / $0.13 / $0.38 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/deepseek/deepseek-v3.2) · [限流](https://openrouter.ai/docs/faq) |

#### DeepSeek-V3

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-V3` | ¥2 / ¥0.2 / ¥8 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V3` | ¥2 / ¥0.2 / ¥8 | 1,000 RPM / 100,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### DeepSeek-V3.1-Terminus

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-V3.1-Terminus` | ¥4 / ¥0.4 / ¥12 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V3.1-Terminus` | ¥4 / ¥0.4 / ¥12 | 1,000 RPM / 100,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v3.1-terminus` | $0.27 / $0.135 / $1 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/deepseek/deepseek-v3.1-terminus) · [限流](https://openrouter.ai/docs/faq) |

#### DeepSeek-R1

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-R1` | ¥4 / ¥0.4 / ¥16 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-R1` | ¥4 / ¥0.4 / ¥16 | 1,000 RPM / 100,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-r1` | $0.7 / — / $2.5 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/deepseek/deepseek-r1) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-bytedance-seed-doubao"></a>

<details>
<summary><strong>ByteDance Seed / Doubao</strong> · 33 个型号 · 41 条供应商记录</summary>

#### doubao-seed-evolving

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-evolving` | ¥6 / ¥1.2 / ¥30 | 500 RPM / 1M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-1-pro

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-1-pro-260628` | ¥6 / ¥1.2 / ¥30 | 500 RPM / 1M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-1-turbo

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-1-turbo-260628` | ¥3 / ¥0.6 / ¥15 | 500 RPM / 1M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-pro

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-pro-260215` | ≤32K ¥3.2/¥0.64/¥16；32–128K ¥4.8/¥0.96/¥24；128–256K ¥9.6/¥1.92/¥48 | 30K RPM / 5M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-code-preview

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-code-preview-260215` | ≤32K ¥3.2/¥0.64/¥16；32–128K ¥4.8/¥0.96/¥24；128–256K ¥9.6/¥1.92/¥48 | 30K RPM / 5M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-lite

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-lite-260428` | ≤32K ¥0.6/¥0.12/¥3.6；32–128K ¥0.9/¥0.18/¥5.4；128–256K ¥1.8/¥0.36/¥10.8 | 30K RPM / 5M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-lite-260215` | ≤32K ¥0.6/¥0.12/¥3.6；32–128K ¥0.9/¥0.18/¥5.4；128–256K ¥1.8/¥0.36/¥10.8 | 30K RPM / 5M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-mini

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-mini-260428` | ≤32K ¥0.2/¥0.04/¥2；32–128K ¥0.4/¥0.08/¥4；128–256K ¥0.8/¥0.16/¥8 | 30K RPM / 5M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-mini-260215` | ≤32K ¥0.2/¥0.04/¥2；32–128K ¥0.4/¥0.08/¥4；128–256K ¥0.8/¥0.16/¥8 | 30K RPM / 5M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-character

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-character-260628` | ≤32K ¥0.8/¥0.16/¥2；32–128K ¥1.2/¥0.16/¥6 | 30K RPM / 5M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-character-251128` | ≤32K ¥0.8/¥0.16/¥2；32–128K ¥1.2/¥0.16/¥6 | 30K RPM / 5M TPM | 往期 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-8

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-1-8-251228` | ¥0.8–2.4 / ¥0.16 / ¥2–24 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-code-preview

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-code-preview-251028` | ¥1.2–2.8 / ¥0.24 / ¥8–16 | 5K RPM / 1.2M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-6

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-251015` | ¥0.8–2.4 / ¥0.16 / ¥2–24 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-250615` | ¥0.8–2.4 / ¥0.16 / ¥2–24 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-6-flash

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-flash-250828` | ¥0.15–0.6 / ¥0.03 / ¥1.5–6 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-flash-250615` | ¥0.15–0.6 / ¥0.03 / ¥1.5–6 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-6-vision

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-vision-250815` | ¥0.8–2.4 / ¥0.16 / ¥8–24 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-translation

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed-translation-250915` | ¥1.2 / — / ¥3.6 | 5K RPM / 500K TPM | 往期 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-pro-32k

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-1-5-pro-32k-250115` | ¥0.8 / ¥0.16 / ¥2 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-pro-32k-character

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-1-5-pro-32k-character-250715` | ¥0.8 / ¥0.16 / ¥2 | 15K RPM / 10M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-lite-32k

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-1-5-lite-32k-250115` | ¥0.3 / ¥0.06 / ¥0.6 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-vision-pro-32k

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-1-5-vision-pro-32k-250115` | ¥3 / — / ¥9 | 30K RPM / 5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedance-2-5-260628` | ¥42–77 / M Tokens | 企业 600 RPM / 10 CC；个人 180 RPM / 3 CC | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedance-2-0-260128` | ¥16–51 / M Tokens | 企业 600 RPM / 10 CC；个人 180 RPM / 3 CC | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-0-fast

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedance-2-0-fast-260128` | ¥22–37 / M Tokens（活动折扣另计） | 企业 600 RPM / 10 CC；个人 180 RPM / 3 CC | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-0-mini

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedance-2-0-mini-260615` | ¥14–23 / M Tokens（活动折扣另计） | 企业 600 RPM / 10 CC；个人 180 RPM / 3 CC | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-1-5-pro

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedance-1-5-pro-251215` | 有声 ¥16 / 无声 ¥8 / M Tokens | 600 RPM / 10 CC | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-1-0-pro

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedance-1-0-pro-250528` | ¥15 / M Tokens | 600 RPM / 10 CC | 往期 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-1-0-pro-fast

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedance-1-0-pro-fast-251015` | ¥4.2 / M Tokens | 600 RPM / 10 CC | 往期 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-5-0-pro

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedream-5-0-pro-260628` | 输入首张免费，其后 ¥0.02/张；输出 ¥0.15–0.60/张 | 500 IPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-5-0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedream-5-0-260128` | ¥0.22 / 张 | 500 IPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-5-0-lite

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedream-5-0-lite-260128` | ¥0.22 / 张 | 500 IPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [Together AI](https://www.together.ai/) | `ByteDance/Seedream-5.0-lite` | $0.035 / MP | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |

#### doubao-seedream-4-5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedream-4-5-251128` | ¥0.25 / 张 | 500 IPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-4-0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seedream-4-0-250828` | ¥0.20 / 张 | 500 IPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [Together AI](https://www.together.ai/) | `ByteDance-Seed/Seedream-4.0` | $0.03 / MP | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |

#### doubao-seed3d-2-0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-seed3d-2-0-260328` | ¥2.40 / 次 | 300 RPM / 5 CC | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-embedding-vision

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-embedding-vision-251215` | 文本 ¥0.70 / 图片 ¥1.80 / M Tokens | 15K RPM / 1.2M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `doubao-embedding-vision-250615` | 文本 ¥0.70 / 图片 ¥1.80 / M Tokens | 15K RPM / 1.2M TPM | 往期 | [官方](https://www.volcengine.com/docs/82379/1544106) |

#### Seed-OSS-36B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `ByteDance-Seed/Seed-OSS-36B-Instruct` | ¥1.5 / — / ¥4 | 1,000 RPM / 20,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-qwen"></a>

<details>
<summary><strong>Qwen</strong> · 41 个型号 · 67 条供应商记录</summary>

#### Qwen 3.8 Max

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [阿里云百炼](https://www.aliyun.com/product/bailian) | `qwen3.8-max` | ¥12.00 / ¥1.50¹ / ¥36.00 | 北京: 30K RPM / 5M TPM | 在售 | [价格](https://help.aliyun.com/zh/model-studio/qwen3-8-max) · [限流](https://help.aliyun.com/zh/model-studio/rate-limit) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/qwen3p8-max` | $2.00 / $0.25 / $6.00 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/qwen3p8-max) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.8-max` | $2 / $0.25 / $6 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.8-max) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen 3.7 Max

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen3.7-Max` | $1.25 / — / $3.75 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.7-max` | $1.475 / $0.295 / $4.425 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.7-max) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3.5-4B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.5-4B` | 免费 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-8B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-8B` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-8b` | $0.117 / — / $0.455 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-8b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen2.5-7B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen2.5-7B-Instruct` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `Pro/Qwen/Qwen2.5-7B-Instruct` | ¥0.35 / — / ¥0.35 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen2.5-7B-Instruct-Turbo` | $0.30 / — / $0.30 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen-2.5-7b-instruct` | $0.1 / — / $0.2 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen-2.5-7b-instruct) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen2.5-14B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen2.5-14B-Instruct` | ¥0.7 / — / ¥0.7 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen2.5-32B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen2.5-32B-Instruct` | ¥1.26 / — / ¥1.26 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3.5-397B-A17B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.5-397B-A17B` | 输入 [0, 128K): ¥1.2 / — / ¥7.2<br>输入 [128K, +∞): ¥3 / — / ¥18 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-397b-a17b` | $0.5 / $0.3 / $3.6 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.5-397b-a17b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-8B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-8B-Instruct` | ¥0.5 / — / ¥2 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-8b-instruct` | $0.117 / — / $0.455 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-vl-8b-instruct) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-14B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-14B` | ¥0.5 / — / ¥2 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-14b` | $0.12 / — / $0.24 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-14b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-30B-A3B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-30B-A3B-Instruct` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-30b-a3b-instruct` | $0.13 / — / $0.52 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-vl-30b-a3b-instruct) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-30B-A3B-Thinking

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-30B-A3B-Thinking` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-30b-a3b-thinking` | $0.2 / — / $2.4 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-vl-30b-a3b-thinking) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-Omni-30B-A3B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Omni-30B-A3B-Instruct` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Omni-30B-A3B-Thinking

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Omni-30B-A3B-Thinking` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Omni-30B-A3B-Captioner

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Omni-30B-A3B-Captioner` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Coder-30B-A3B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Coder-30B-A3B-Instruct` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-coder-30b-a3b-instruct` | $0.07 / — / $0.28 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-coder-30b-a3b-instruct) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-30B-A3B-Instruct-2507

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-30B-A3B-Instruct-2507` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-30b-a3b-instruct-2507` | $0.04815 / — / $0.19305 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-30b-a3b-instruct-2507) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-32B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-32B-Instruct` | ¥1 / — / ¥4 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-32b-instruct` | $0.104 / — / $0.416 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-vl-32b-instruct) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-32B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-32B` | ¥1 / — / ¥4 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-32b` | $0.08 / — / $0.28 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-32b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen2.5-72B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen2.5-72B-Instruct` | ¥4.13 / — / ¥4.13 | 1,000 RPM / 20,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen-2.5-72b-instruct` | $0.36 / — / $0.4 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen-2.5-72b-instruct) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen2.5-72B-Instruct-128K

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen2.5-72B-Instruct-128K` | ¥4.13 / — / ¥4.13 | 1,000 RPM / 20,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-VL-8B-Thinking

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-8B-Thinking` | ¥0.5 / — / ¥5 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-8b-thinking` | $0.18 / — / $2.1 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3-vl-8b-thinking) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-32B-Thinking

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-32B-Thinking` | ¥1 / — / ¥10 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3.5-9B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.5-9B` | 输入 [0, 128K): ¥0.5 / — / ¥4<br>输入 [128K, +∞): ¥1.5 / — / ¥12 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen3.5-9B` | $0.17 / — / $0.25 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-9b` | $0.1 / — / $0.15 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.5-9b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3.6-35B-A3B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.6-35B-A3B` | ¥1.8 / — / ¥10.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.6-35b-a3b` | $0.14 / $0.05 / $1 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.6-35b-a3b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3.5-35B-A3B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.5-35B-A3B` | 输入 [0, 128K): ¥0.4 / — / ¥3.2<br>输入 [128K, +∞): ¥1.6 / — / ¥12.8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-35b-a3b` | $0.25 / $0.25 / $1.25 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.5-35b-a3b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3.6-27B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.6-27B` | ¥3 / — / ¥18 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.6-27b` | $0.32 / — / $3.2 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.6-27b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3.5-27B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.5-27B` | 输入 [0, 128K): ¥0.6 / — / ¥4.8<br>输入 [128K, +∞): ¥1.8 / — / ¥14.4 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-27b` | $0.195 / — / $1.56 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.5-27b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3.5-122B-A10B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3.5-122B-A10B` | 输入 [0, 128K): ¥0.8 / — / ¥6.4<br>输入 [128K, +∞): ¥2 / — / ¥16 | 1,000 RPM / 20,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-122b-a10b` | $0.26 / — / $2.08 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/qwen/qwen3.5-122b-a10b) · [限流](https://openrouter.ai/docs/faq) |

#### Qwen3-Embedding-0.6B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Embedding-0.6B` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Reranker-0.6B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Reranker-0.6B` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Embedding-4B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Embedding-4B` | ¥0.14 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Reranker-4B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Reranker-4B` | ¥0.14 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Embedding-8B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Embedding-8B` | ¥0.28 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-Reranker-8B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-Reranker-8B` | ¥0.28 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-VL-Reranker-8B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-Reranker-8B` | 文本 ¥0.7 / 图片 ¥1.8 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-VL-Embedding-8B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-VL-Embedding-8B` | 文本 ¥0.7 / 图片 ¥1.8 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen-Image

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen-Image` | ¥0.3 / 张 | 动态限流 | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen-Image` | $0.0058 / MP | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |

#### Qwen-Image-Edit

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen-Image-Edit` | ¥0.3 / 张 | 动态限流 | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen-Image-Edit-2509

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen-Image-Edit-2509` | ¥0.3 / 张 | 动态限流 | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Qwen3-ASR-1.7B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Qwen/Qwen3-ASR-1.7B` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-glm"></a>

<details>
<summary><strong>GLM</strong> · 8 个型号 · 19 条供应商记录</summary>

#### GLM 5.2

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [智谱开放平台](https://bigmodel.cn/) | `glm-5.2` | ¥8.00 / ¥2.00 / ¥28.00 | 按用户权益与模型动态并发 | 在售 | [价格](https://bigmodel.cn/pricing) · [限流](https://docs.bigmodel.cn/cn/api/rate-limit) |
| [Mistral AI](https://mistral.ai/) | GLM 5.2 | $1.40 / $0.14 / $4.40 | 按订阅与模型，在控制台查看 | 在售 | [价格](https://docs.mistral.ai/inference/pricing) · [限流](https://docs.mistral.ai/resources/known-limitations) |
| [腾讯云 TokenHub](https://cloud.tencent.com/product/tokenhub) | GLM 5.2 | ¥10.254 / ¥1.9044 / ¥32.2282 | 按账户与模型动态变化 | 在售 | [价格](https://cloud.tencent.cn/document/product/1823/130055) |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `glm-5-2-260617` | ¥8 / ¥2 / ¥28 | 500 RPM / 1M TPM | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [硅基流动](https://siliconflow.cn/) | `zai-org/GLM-5.2` | ¥8 / ¥2 / ¥28 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `zai-org/GLM-5.2` | $1.40 / $0.26 / $4.40 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/glm-5p2` | $1.40 / $0.14 / $4.40 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/glm-5p2) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-5.2` | $1.19 / $0.221 / $3.74 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/z-ai/glm-5.2) · [限流](https://openrouter.ai/docs/faq) |

#### GLM 4.7

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `glm-4-7-251222` | ¥2–4 / ¥0.4–0.8 / ¥8–16 | 15K RPM / 1.5M TPM | 即将下线 | [官方](https://www.volcengine.com/docs/82379/1544106) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-4.7` | $0.4 / $0.08 / $1.75 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/z-ai/glm-4.7) · [限流](https://openrouter.ai/docs/faq) |

#### GLM-Z1-9B-0414

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `THUDM/GLM-Z1-9B-0414` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### GLM-4-9B-0414

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `THUDM/GLM-4-9B-0414` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### GLM-4-32B-0414

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `THUDM/GLM-4-32B-0414` | ¥1.89 / — / ¥1.89 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### GLM-4.5V

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `zai-org/GLM-4.5V` | ¥1 / — / ¥6 | 1,000 RPM / 20,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-4.5v` | $0.6 / $0.11 / $1.8 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/z-ai/glm-4.5v) · [限流](https://openrouter.ai/docs/faq) |

#### GLM-4.5-Air

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `zai-org/GLM-4.5-Air` | ¥1 / — / ¥6 | 1,000 RPM / 20,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-4.5-air` | $0.13 / $0.025 / $0.85 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/z-ai/glm-4.5-air) · [限流](https://openrouter.ai/docs/faq) |

#### GLM-5.1

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Pro/zai-org/GLM-5.1` | 输入 [0, 32K): ¥6 / ¥1.3 / ¥24<br>输入 [32K, +∞): ¥8 / ¥2 / ¥28 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-5.1` | $1.26 / $0.234 / $3.96 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/z-ai/glm-5.1) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-kimi"></a>

<details>
<summary><strong>Kimi</strong> · 3 个型号 · 13 条供应商记录</summary>

#### Kimi K3

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Kimi 开放平台](https://platform.kimi.com/) | `kimi-k3` | ¥20.00 / ¥2.00 / ¥100.00 | 按累计充值 Tier | 在售 | [价格](https://platform.kimi.com/) · [限流](https://platform.kimi.com/docs/pricing/limits) |
| [Together AI](https://www.together.ai/) | `moonshotai/Kimi-K3` | $3.00 / $0.30 / $15.00 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/kimi-k3` | $3.00 / $0.30 / $15.00 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/kimi-k3) |
| [OpenRouter](https://openrouter.ai/) | `moonshotai/kimi-k3` | $3 / $0.3 / $15 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/moonshotai/kimi-k3) · [限流](https://openrouter.ai/docs/faq) |

#### Kimi K2.7 Code

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Kimi 开放平台](https://platform.kimi.com/) | `kimi-k2.7-code` | ¥6.50 / ¥1.30 / ¥27.00 | Tier 0: 1 CC / 3 RPM / 500K TPM / 1.5M TPD | 在售 | [价格](https://platform.kimi.com/) · [限流](https://platform.kimi.com/docs/pricing/limits) |
| [硅基流动](https://siliconflow.cn/) | `moonshotai/Kimi-K2.7-Code` | ¥6.5 / ¥1.3 / ¥27 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `moonshotai/Kimi-K2.7-Code` | $0.95 / $0.19 / $4.00 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/kimi-k2p7-code` | $0.95 / $0.19 / $4.00 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/kimi-k2p7-code) |
| [OpenRouter](https://openrouter.ai/) | `moonshotai/kimi-k2.7-code` | $0.67 / $0.19 / $3.4 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/moonshotai/kimi-k2.7-code) · [限流](https://openrouter.ai/docs/faq) |

#### Kimi K2.6

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Kimi 开放平台](https://platform.kimi.com/) | `kimi-k2.6` | ¥6.50 / ¥1.10 / ¥27.00 | Tier 1 起取消 TPD 上限 | 在售 | [价格](https://platform.kimi.com/) · [限流](https://platform.kimi.com/docs/pricing/limits) |
| [硅基流动](https://siliconflow.cn/) | `Pro/moonshotai/Kimi-K2.6` | ¥6.5 / ¥1.1 / ¥27 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/kimi-k2p6` | $0.95 / $0.16 / $4.00 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/kimi-k2p6) |
| [OpenRouter](https://openrouter.ai/) | `moonshotai/kimi-k2.6` | $0.95 / $0.16 / $4 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/moonshotai/kimi-k2.6) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-minimax"></a>

<details>
<summary><strong>MiniMax</strong> · 5 个型号 · 11 条供应商记录</summary>

#### MiniMax M3

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Together AI](https://www.together.ai/) | `MiniMaxAI/MiniMax-M3` | $0.30 / $0.06 / $1.20 | Serverless 动态限流 | 在售 | [模型目录](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/minimax-m3` | $0.30 / $0.06 / $1.20 | Serverless 动态限流 | 在售 | [价格目录](https://docs.fireworks.ai/serverless/pricing) |

#### MiniMax M2.7

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.7` | ¥2.10 / ¥0.42 / ¥8.40 | 高峰期动态限流 | 在售 | [价格](https://platform.minimaxi.com/docs/guides/pricing-paygo) · [限流说明](https://platform.minimaxi.com/docs/token-plan/faq) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/minimax-m2p7` | $0.30 / $0.06 / $1.20 | Serverless 动态限流 | 在售 | [模型与价格](https://app.fireworks.ai/models/fireworks/minimax-m2p7) |
| [OpenRouter](https://openrouter.ai/) | `minimax/minimax-m2.7` | $0.3 / $0.06 / $1.2 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/minimax/minimax-m2.7) · [限流](https://openrouter.ai/docs/faq) |

#### MiniMax-M2.7-highspeed

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.7-highspeed` | ¥4.20 / ¥0.42 / ¥16.80 | 与订阅等级相关 | 在售 | [价格](https://platform.minimaxi.com/docs/guides/pricing-paygo) |

#### MiniMax-M2.5-highspeed

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.5-highspeed` | ¥4.20 / ¥0.21 / ¥16.80 | 与订阅等级相关 | 在售 | [价格](https://platform.minimaxi.com/docs/guides/pricing-paygo) |

#### MiniMax-M2.5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.5` | ¥2.10 / ¥0.21 / ¥8.40 | 按账户等级动态变化 | 在售 | [价格](https://platform.minimaxi.com/docs/guides/pricing-paygo) |
| [硅基流动](https://siliconflow.cn/) | `MiniMaxAI/MiniMax-M2.5` | ¥2.1 / ¥0.21 / ¥8.4 | 1,000 RPM / 100,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `Pro/MiniMaxAI/MiniMax-M2.5` | ¥2.1 / ¥0.21 / ¥8.4 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `minimax/minimax-m2.5` | $0.27 / $0.027 / $1.08 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/minimax/minimax-m2.5) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-mistral"></a>

<details>
<summary><strong>Mistral</strong> · 3 个型号 · 4 条供应商记录</summary>

#### mistral-large-2512

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Mistral AI](https://mistral.ai/) | `mistral-large-2512` | $0.50 / $0.05 / $1.50 | 按订阅与模型，在控制台查看 | 在售 | [价格](https://docs.mistral.ai/inference/pricing) · [限流](https://docs.mistral.ai/resources/known-limitations) |
| [OpenRouter](https://openrouter.ai/) | `mistralai/mistral-large-2512` | $0.5 / $0.05 / $1.5 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/mistralai/mistral-large-2512) · [限流](https://openrouter.ai/docs/faq) |

#### mistral-medium-latest

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Mistral AI](https://mistral.ai/) | `mistral-medium-latest` | $1.50 / $0.15 / $7.50 | RPS 与 TPM 独立限制 | 在售 | [价格](https://docs.mistral.ai/inference/pricing) |

#### mistral-small-latest

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [Mistral AI](https://mistral.ai/) | `mistral-small-latest` | $0.15 / $0.015 / $0.60 | Batch 不占实时限流 | 在售 | [价格](https://docs.mistral.ai/inference/pricing) · [限制](https://docs.mistral.ai/resources/known-limitations) |

</details>

<a id="family-ernie-paddleocr"></a>

<details>
<summary><strong>ERNIE / PaddleOCR</strong> · 4 个型号 · 5 条供应商记录</summary>

#### ERNIE 5.1

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [百度智能云千帆](https://cloud.baidu.com/product-s/qianfan_home) | `ERNIE-5.1` ≤32K input | ¥4.00 / — / ¥18.00 | 按账户与服务实例 | 在售 | [价格](https://cloud.baidu.com/doc/qianfan/s/wmh4sv6ya) |
| [百度智能云千帆](https://cloud.baidu.com/product-s/qianfan_home) | `ERNIE-5.1` 32K–128K input | ¥6.00 / — / ¥22.00 | 按账户与服务实例 | 在售 | [价格](https://cloud.baidu.com/doc/qianfan/s/wmh4sv6ya) |

#### ERNIE 4.5 Turbo 128K Preview

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [百度智能云千帆](https://cloud.baidu.com/product-s/qianfan_home) | `ERNIE-4.5-Turbo-128K-Preview` | ¥0.80 / ¥0.20 / ¥3.20 | 按账户与服务实例 | 在售 | [价格](https://cloud.baidu.com/doc/qianfan/s/wmh4sv6ya) |

#### PaddleOCR-VL-1.5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `PaddlePaddle/PaddleOCR-VL-1.5` | 免费 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### ERNIE-Image-Turbo

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `baidu/ERNIE-Image-Turbo` | ¥0.11 / 张 | 动态限流 | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-hunyuan"></a>

<details>
<summary><strong>Hunyuan</strong> · 2 个型号 · 3 条供应商记录</summary>

#### Hunyuan-MT-7B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `tencent/Hunyuan-MT-7B` | 免费 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Hunyuan-A13B-Instruct

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `tencent/Hunyuan-A13B-Instruct` | 09:00–18:00: ¥1 / — / ¥4<br>其他时段: ¥0.8 / — / ¥3.2 | 1,000 RPM / 20,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `tencent/hunyuan-a13b-instruct` | $0.14 / — / $0.57 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/tencent/hunyuan-a13b-instruct) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-bge"></a>

<details>
<summary><strong>BGE</strong> · 4 个型号 · 6 条供应商记录</summary>

#### bge-m3

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `BAAI/bge-m3` | 免费 | 2,000 RPM / 500,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `Pro/BAAI/bge-m3` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### bge-reranker-v2-m3

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `BAAI/bge-reranker-v2-m3` | 免费 | 2,000 RPM / 500,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [硅基流动](https://siliconflow.cn/) | `Pro/BAAI/bge-reranker-v2-m3` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### bge-large-zh-v1.5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `BAAI/bge-large-zh-v1.5` | 免费 | 2,000 RPM / 500,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### bge-large-en-v1.5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `BAAI/bge-large-en-v1.5` | 免费 | 2,000 RPM / 500,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-longcat"></a>

<details>
<summary><strong>LongCat</strong> · 1 个型号 · 2 条供应商记录</summary>

#### LongCat-2.0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `meituan-longcat/LongCat-2.0` | ¥5 / ¥0.1 / ¥20 | 500 RPM / 2,000,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `meituan/longcat-2.0` | $0.3 / $0.006 / $1.2 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/meituan/longcat-2.0) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-ling"></a>

<details>
<summary><strong>Ling</strong> · 2 个型号 · 2 条供应商记录</summary>

#### Ling-mini-2.0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `inclusionAI/Ling-mini-2.0` | ¥0.5 / — / ¥2 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Ling-flash-2.0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `inclusionAI/Ling-flash-2.0` | ¥1 / — / ¥4 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-step"></a>

<details>
<summary><strong>Step</strong> · 1 个型号 · 3 条供应商记录</summary>

#### Step-3.5-Flash

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `stepfun-ai/Step-3.5-Flash` | ¥0.7 / — / ¥2.1 | 1,000 RPM / 10,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [阶跃星辰](https://platform.stepfun.com/) | `step-3.5-flash` | ¥0.70 / ¥0.14 / ¥2.10 | 按账户等级动态变化 | 在售 | [价格与限速](https://platform.stepfun.com/docs/zh/guides/pricing/details) |
| [OpenRouter](https://openrouter.ai/) | `stepfun/step-3.5-flash` | $0.1 / — / $0.3 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/stepfun/step-3.5-flash) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-nex"></a>

<details>
<summary><strong>Nex</strong> · 1 个型号 · 2 条供应商记录</summary>

#### Nex-N2-Pro

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `nex-agi/Nex-N2-Pro` | ¥1.75 / ¥0.175 / ¥7 | 1,000 RPM / 80,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `nex-agi/nex-n2-pro` | $0.25 / $0.025 / $1 | 按账户余额与上游路由动态变化 | 在售 | [模型与价格](https://openrouter.ai/nex-agi/nex-n2-pro) · [限流](https://openrouter.ai/docs/faq) |

</details>

<a id="family-xingchen"></a>

<details>
<summary><strong>XingChen</strong> · 4 个型号 · 4 条供应商记录</summary>

#### XingChenASR-V3.2-Ultra

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `XingChenAGI/XingChenASR-V3.2-Ultra` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### XingChenASR-Diarize-V3.0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `XingChenAGI/XingChenASR-Diarize-V3.0` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### XingChenGSR-V1.0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `XingChenAGI/XingChenGSR-V1.0` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### XingChenASR-V3.2

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `XingChenAGI/XingChenASR-V3.2` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-funaudiollm"></a>

<details>
<summary><strong>FunAudioLLM</strong> · 2 个型号 · 2 条供应商记录</summary>

#### SenseVoiceSmall

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `FunAudioLLM/SenseVoiceSmall` | 免费 | 1,000 RPM / 50,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

#### CosyVoice2-0.5B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `FunAudioLLM/CosyVoice2-0.5B` | ¥0.05 / 千字符 UTF-8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-moss"></a>

<details>
<summary><strong>MOSS</strong> · 1 个型号 · 1 条供应商记录</summary>

#### MOSS-TTSD-v0.5

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `fnlp/MOSS-TTSD-v0.5` | ¥0.05 / 千字符 UTF-8 | 1,000 RPM / 40,000 TPM | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-wan"></a>

<details>
<summary><strong>Wan</strong> · 2 个型号 · 2 条供应商记录</summary>

#### Wan2.2-T2V-A14B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Wan-AI/Wan2.2-T2V-A14B` | ¥2 / 个 | 5 IPM / 200 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Wan2.2-I2V-A14B

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Wan-AI/Wan2.2-I2V-A14B` | ¥2 / 个 | 5 IPM / 200 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-kolors"></a>

<details>
<summary><strong>Kolors</strong> · 1 个型号 · 1 条供应商记录</summary>

#### Kolors

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Kwai-Kolors/Kolors` | 免费 | 2 IPM / 400 IPD | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-z-image"></a>

<details>
<summary><strong>Z-Image</strong> · 2 个型号 · 2 条供应商记录</summary>

#### Z-Image-Turbo

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Tongyi-MAI/Z-Image-Turbo` | ¥0.1 / 张 | 动态限流 | 在售 | [官方](https://siliconflow.cn/pricing) |

#### Z-Image

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [硅基流动](https://siliconflow.cn/) | `Tongyi-MAI/Z-Image` | ¥0.3 / 张 | 动态限流 | 在售 | [官方](https://siliconflow.cn/pricing) |

</details>

<a id="family-hyper3d"></a>

<details>
<summary><strong>Hyper3D</strong> · 1 个型号 · 1 条供应商记录</summary>

#### hyper3d-gen2

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `hyper3d-gen2-260112` | ¥1.80 / 次 | 60 RPM / 3 CC | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

</details>

<a id="family-hitem3d"></a>

<details>
<summary><strong>Hitem3D</strong> · 1 个型号 · 1 条供应商记录</summary>

#### hitem3d-2-0

| API 供应商 | 模型 ID | 价格 | Quota | 状态 | 来源 |
| --- | --- | --- | --- | --- | --- |
| [火山引擎方舟](https://www.volcengine.com/product/ark) | `hitem3d-2-0-251223` | ¥5.80–13.05 / 次 | 600 RPM / 30 CC | 在售 | [官方](https://www.volcengine.com/docs/82379/1544106) |

</details>

## Quota 说明

API 的 `quota` 通常不是一个固定数字：它可能同时受模型、组织、账户等级、累计消费、地区和短时突发流量影响。

- 表中有明确数值时，展示的是官方公开的默认层级或注明地区的限制，并不代表企业客户上限。
- “动态限流”表示供应商只在登录后的控制台展示实际额度，或会随集群负载调整。
- 缓存 Token 是否计入 TPM，各供应商规则不同。例如 Claude 多数模型只计算未缓存输入，而 xAI 会把缓存 Token 计入 TPM。

## 数据口径

本页只收录满足以下条件的报价：

1. 模型当前可通过 API 调用；已下线或历史快照仅在状态明确标为“往期”时保留；
2. 价格能从供应商或托管平台官方页面核验；
3. 计费单位和适用条件可以明确确认；
4. Preview、区域价、限时价和长上下文溢价均显式标注；
5. 同一开放权重模型在不同平台上的报价分别记录，不把“模型开发商”误作唯一供应商。


## 参与更新

价格变化非常快，欢迎提交 Issue 或 PR。更新一条报价时，请同时提供：

- 模型 ID 与供应商；
- 原始币种及计费单位；
- 输入、缓存、输出价格；
- 地区、上下文阶梯、Batch 或高速服务等级；
- Quota 及其适用账户层级；
- 官方来源 URL 与核验日期。

---

<div align="center">

数据仅供技术选型与成本估算，不构成采购或财务建议。

本表格由 AI 辅助整理。

</div>
