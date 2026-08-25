<div align="center">

[简体中文](README.md) | [English](README_EN.md)

# LLM API Price Watch

This repository tracks API pricing and usage limits for mainstream large language models across providers.

[![Data](https://img.shields.io/badge/data-official%20sources-22c55e?style=flat-square)](#methodology)
[![Updated](https://img.shields.io/badge/updated-2026--08--25-6366f1?style=flat-square)](#update-status)
[![Currency](https://img.shields.io/badge/currency-USD%20%7C%20CNY-f59e0b?style=flat-square)](#full-model-catalog-and-pricing)
[![PRs](https://img.shields.io/badge/PRs-welcome-ec4899?style=flat-square)](#contributing)

Data is organized by model family and includes providers, model IDs, input, cached-input and output pricing, API quotas, and official sources.

[Full model catalog](#full-model-catalog-and-pricing) · [Quota notes](#quota-notes) · [Methodology](#methodology) · [Contributing](#contributing)

</div>

> [!IMPORTANT]
> Prices are public list prices and exclude taxes, payment fees, enterprise discounts, and temporary promotions. Pricing may vary by region, context length, and service tier; verify the official source before purchase.

## Update status

| Item | Status |
| --- | --- |
| Last verified | **2026-08-25** |
| Coverage | **26 model families · 141 models · 259 provider records** |
| Pricing basis | Per 1M tokens, ordered as **input / cached input / output** |
| Currency handling | Provider currencies retained; no live conversion |
| `—` | Not disclosed, not applicable, or available only in the account console |
| Quota | `RPM` requests/min · `RPS` requests/sec · `TPM` tokens/min · `TPD` tokens/day · `CC` concurrent connections |

## Full model catalog and pricing

The catalog is organized as model family → exact model → API provider. Official and verified third-party APIs for the same model appear in one table. Provider-specific model IDs, snapshots, and `Pro` routes are retained in the Model ID column.

Prices retain each provider’s original currency. Text models are priced per 1M tokens in the order input / cached input / output. Image, audio, video, and 3D models state their actual billing units. `—` means not applicable or not publicly disclosed.

> [!NOTE]
> “Verified third party” means a platform whose public website confirms that the model remains callable and whose pricing or quota can be verified. Unverifiable resellers are excluded. OpenRouter shows the lowest route price returned by its current Models API; actual charges may vary by upstream route.

<a id="family-openai-gpt"></a>

<details>
<summary><strong>OpenAI GPT</strong> · 3 models · 9 provider records</summary>

#### gpt-5.6-sol

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [OpenAI](https://openai.com/) | `gpt-5.6-sol` | $4.00 / $0.40 / $20.00 | Tier 1: 500 RPM / 500K TPM | Available | [Pricing & rate limits](https://developers.openai.com/api/docs/models/gpt-5.6-sol) |
| [Azure OpenAI](https://azure.microsoft.com/products/ai-services/openai-service) | `gpt-5.6-sol` | — (public token meter not yet verifiable) | Quota request required per subscription | Availability confirmed | [Model availability](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/reasoning) |
| [OpenRouter](https://openrouter.ai/) | `openai/gpt-5.6-sol` | $2 / $0.2 / $10 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/openai/gpt-5.6-sol) · [Rate limits](https://openrouter.ai/docs/faq) |

#### gpt-5.6-terra

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [OpenAI](https://openai.com/) | `gpt-5.6-terra` | $2.00 / $0.20 / $12.00 | Varies by usage tier | Available | [Pricing & rate limits](https://developers.openai.com/api/docs/models/gpt-5.6-terra) |
| [Azure OpenAI](https://azure.microsoft.com/products/ai-services/openai-service) | `gpt-5.6-terra` | — (public token meter not yet verifiable) | Quota request required per subscription | Availability confirmed | [Model availability](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/reasoning) |
| [OpenRouter](https://openrouter.ai/) | `openai/gpt-5.6-terra` | $2 / $0.2 / $12 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/openai/gpt-5.6-terra) · [Rate limits](https://openrouter.ai/docs/faq) |

#### gpt-5.6-luna

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [OpenAI](https://openai.com/) | `gpt-5.6-luna` | $0.20 / $0.02 / $1.20 | Tier 1: 500 RPM / 500K TPM | Available | [Pricing & rate limits](https://developers.openai.com/api/docs/models/gpt-5.6-luna) |
| [Azure OpenAI](https://azure.microsoft.com/products/ai-services/openai-service) | `gpt-5.6-luna` | — (public token meter not yet verifiable) | Quota request required per subscription | Availability confirmed | [Model availability](https://learn.microsoft.com/en-us/azure/foundry/openai/how-to/reasoning) |
| [OpenRouter](https://openrouter.ai/) | `openai/gpt-5.6-luna` | $0.2 / $0.02 / $1.2 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/openai/gpt-5.6-luna) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-claude"></a>

<details>
<summary><strong>Claude</strong> · 4 models · 19 provider records</summary>

#### claude-fable-5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-fable-5` | $10.00 / $1.00 / $50.00 | Tiered by Start / Build / Scale | Available | [Model & pricing](https://platform.claude.com/docs/en/models/overview) · [Rate limits](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-fable-5` | $10.00 / $1.00 / $50.00 | Varies by region and account | Available | [Model card](https://docs.aws.amazon.com/bedrock/latest/userguide/model-card-anthropic-claude-fable-5.html) · [Pricing](https://aws.amazon.com/bedrock/pricing/) |
| [Google Cloud](https://cloud.google.com/) | `claude-fable-5` | $10.00 / $1.00 / $50.00 (Global) | Varies by project and region | Available | [Pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-fable-5` | $10.00 / $1.00 / $50.00 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/anthropic/claude-fable-5) · [Rate limits](https://openrouter.ai/docs/faq) |

#### claude-opus-5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-opus-5` | $5.00 / $0.50 / $25.00 | Tiered by Start / Build / Scale | Available | [Pricing](https://platform.claude.com/docs/en/about-claude/pricing) · [Rate limits](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-opus-5` | $5.00 / $0.50 / $25.00 | Varies by region and account | Available | [Release & availability](https://aws.amazon.com/blogs/machine-learning/introducing-claude-opus-5-on-aws-anthropics-most-capable-opus-model/) · [Pricing](https://aws.amazon.com/bedrock/pricing/) |
| [Google Cloud](https://cloud.google.com/) | `claude-opus-5` | $5.50 / $0.55 / $27.50 | Varies by project and region | Available | [Pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [Microsoft Foundry](https://azure.microsoft.com/products/ai-foundry) | `claude-opus-5` | — (priced by Marketplace, deployment type, and region) | Varies by deployment type and subscription | Availability confirmed | [Model availability](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-opus-5` | $5 / $0.5 / $25 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/anthropic/claude-opus-5) · [Rate limits](https://openrouter.ai/docs/faq) |

#### claude-sonnet-5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-sonnet-5` | $2.00 / $0.20 / $10.00 | Separate per-model rate-limit pool | Available | [Pricing](https://platform.claude.com/docs/en/about-claude/pricing) · [Rate limits](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-sonnet-5` | $2.00 / — / $10.00 (promotional price through 2026-08-31; then $3 / $15) | Varies by region and account | Available | [Pricing](https://aws.amazon.com/bedrock/pricing/) · [Model card](https://docs.aws.amazon.com/bedrock/latest/userguide/model-card-anthropic-claude-sonnet-5.html) |
| [Google Cloud](https://cloud.google.com/) | `claude-sonnet-5` | $2.20 / $0.22 / $11.00 (promotional price through 2026-08-31) | Varies by project and region | Available | [Pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [Microsoft Foundry](https://azure.microsoft.com/products/ai-foundry) | `claude-sonnet-5` | — (priced by Marketplace, deployment type, and region) | Varies by deployment type and subscription | Availability confirmed | [Model availability](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-sonnet-5` | $2 / $0.2 / $10 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/anthropic/claude-sonnet-5) · [Rate limits](https://openrouter.ai/docs/faq) |

#### claude-haiku-4-5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Anthropic](https://www.anthropic.com/) | `claude-haiku-4-5` | $1.00 / $0.10 / $5.00 | Varies by account tier | Available | [Pricing](https://platform.claude.com/docs/en/about-claude/pricing) · [Rate limits](https://platform.claude.com/docs/en/api/rate-limits) |
| [Amazon Bedrock](https://aws.amazon.com/bedrock/) | `anthropic.claude-haiku-4-5-20251001-v1:0` | $1.00 / $0.10 / $5.00 (Global) | Varies by region and account | Available | [Pricing](https://aws.amazon.com/bedrock/pricing/) · [Model ID](https://docs.aws.amazon.com/bedrock/latest/userguide/claude-messages-extended-thinking.html) |
| [Google Cloud](https://cloud.google.com/) | `claude-haiku-4-5` | $1.10 / $0.11 / $5.50 | Varies by project and region | Available | [Pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [Microsoft Foundry](https://azure.microsoft.com/products/ai-foundry) | `claude-haiku-4-5` | — (priced by Marketplace, deployment type, and region) | Varies by deployment type and subscription | Availability confirmed | [Model availability](https://learn.microsoft.com/en-us/azure/foundry/foundry-models/concepts/claude-models) |
| [OpenRouter](https://openrouter.ai/) | `anthropic/claude-haiku-4.5` | $1 / $0.1 / $5 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/anthropic/claude-haiku-4.5) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-gemini"></a>

<details>
<summary><strong>Gemini</strong> · 3 models · 9 provider records</summary>

#### gemini-3.7-flash

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Google AI](https://ai.google.dev/) | `gemini-3.7-flash` | $0.75 / $0.075 / $3.75 | Varies by project tier; see AI Studio | Available | [Pricing](https://ai.google.dev/gemini-api/docs/pricing) · [Rate limits](https://ai.google.dev/gemini-api/docs/rate-limits) |
| [Google Cloud](https://cloud.google.com/) | `gemini-3.7-flash` | $0.75 / $0.075 / $3.75 (Global promotional price through 2026-12-31) | Varies by project and region | Available | [Pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `google/gemini-3.7-flash` | $0.375 / $0.0375 / $1.875 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/google/gemini-3.7-flash) · [Rate limits](https://openrouter.ai/docs/faq) |

#### gemini-3.5-flash

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Google AI](https://ai.google.dev/) | `gemini-3.5-flash` | $1.50 / $0.15 / $9.00 | Varies by project tier | Available | [Pricing](https://ai.google.dev/gemini-api/docs/pricing) |
| [Google Cloud](https://cloud.google.com/) | `gemini-3.5-flash` | $1.50 / $0.15 / $9.00 (Global) | Varies by project and region | Available | [Pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `google/gemini-3.5-flash` | $1.5 / $0.15 / $9 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/google/gemini-3.5-flash) · [Rate limits](https://openrouter.ai/docs/faq) |

#### gemini-3.5-flash-lite

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Google AI](https://ai.google.dev/) | `gemini-3.5-flash-lite` | $0.30 / $0.03 / $2.50 | Varies by project tier | Available | [Pricing](https://ai.google.dev/gemini-api/docs/pricing) |
| [Google Cloud](https://cloud.google.com/) | `gemini-3.5-flash-lite` | $0.30 / $0.03 / $2.50 (Global) | Varies by project and region | Available | [Pricing](https://cloud.google.com/gemini-enterprise-agent-platform/generative-ai/pricing) |
| [OpenRouter](https://openrouter.ai/) | `google/gemini-3.5-flash-lite` | $0.3 / $0.03 / $2.5 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/google/gemini-3.5-flash-lite) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-grok"></a>

<details>
<summary><strong>Grok</strong> · 1 models · 2 provider records</summary>

#### grok-4.3

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [xAI](https://x.ai/) | `grok-4.3` | $1.25 / $0.20 / $2.50 | Tier 0: 37 RPS / 10M TPM | Available | [Pricing](https://docs.x.ai/developers/models/grok-4.3) · [Rate limits](https://docs.x.ai/developers/rate-limits) |
| [OpenRouter](https://openrouter.ai/) | `x-ai/grok-4.3` | $1.25 / $0.2 / $2.5 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/x-ai/grok-4.3) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-deepseek"></a>

<details>
<summary><strong>DeepSeek</strong> · 8 models · 28 provider records</summary>

#### DeepSeek V4 Flash

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [DeepSeek](https://www.deepseek.com/) | `deepseek-v4-flash` | $0.14 / $0.0028 / $0.28 | 2,500 CC / account | Available | [Pricing](https://api-docs.deepseek.com/quick_start/pricing) · [Rate limits](https://api-docs.deepseek.com/quick_start/rate_limit/) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `deepseek-v4-flash-ga-260731` | ¥3 / ¥0.1 / ¥9 | 500 RPM / 1M TPM | GA | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `deepseek-v4-flash-260425` | ¥1 / ¥0.2 / ¥2 | 15K RPM / 1.5M TPM | Price changes Aug 28 | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V4-Flash` | ¥1 / ¥0.02 / ¥2 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `deepseek-ai/DeepSeek-V4-Flash-0731` | $0.14 / $0.03 / $0.28 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/deepseek-v4-flash-0731` | $0.22 / $0.007 / $0.66 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/deepseek-v4-flash-0731) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v4-flash` | $0.088606 / $0.017721 / $0.177212 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/deepseek/deepseek-v4-flash) · [Rate limits](https://openrouter.ai/docs/faq) |

#### DeepSeek V4 Pro

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [DeepSeek](https://www.deepseek.com/) | `deepseek-v4-pro` | $0.435 / $0.003625 / $0.87 | 500 CC / account | Available | [Pricing](https://api-docs.deepseek.com/quick_start/pricing) · [Rate limits](https://api-docs.deepseek.com/quick_start/rate_limit/) |
| [Together AI](https://www.together.ai/) | `deepseek-ai/DeepSeek-V4-Pro` | $1.74 / $0.20 / $3.48 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [Together AI](https://www.together.ai/) | `deepseek-ai/DeepSeek-V4-Pro-0813` | $1.32 / $0.13 / $3.96 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `deepseek-v4-pro-ga-260813` | ¥9 / ¥0.3 / ¥27 | 500 RPM / 1M TPM | GA | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `deepseek-v4-pro-260425` | ¥12 / ¥1 / ¥24 | 15K RPM / 1.5M TPM | Price changes Aug 28 | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V4-Pro` | ¥12 / ¥1 / ¥24 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/deepseek-v4-pro` | $1.74 / $0.145 / $3.48 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/deepseek-v4-pro) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v4-pro` | $0.790308 / $0.065859 / $1.580616 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/deepseek/deepseek-v4-pro) · [Rate limits](https://openrouter.ai/docs/faq) |

#### DeepSeek-OCR

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-OCR` | Free | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### DeepSeek-R1-0528-Qwen3-8B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-R1-0528-Qwen3-8B` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### DeepSeek-V3.2

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V3.2` | ¥4 / ¥0.4 / ¥6 | 1,000 RPM / 100,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-V3.2` | ¥4 / ¥0.4 / ¥6 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v3.2` | $0.26 / $0.13 / $0.38 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/deepseek/deepseek-v3.2) · [Rate limits](https://openrouter.ai/docs/faq) |

#### DeepSeek-V3

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-V3` | ¥2 / ¥0.2 / ¥8 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V3` | ¥2 / ¥0.2 / ¥8 | 1,000 RPM / 100,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### DeepSeek-V3.1-Terminus

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-V3.1-Terminus` | ¥4 / ¥0.4 / ¥12 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-V3.1-Terminus` | ¥4 / ¥0.4 / ¥12 | 1,000 RPM / 100,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-v3.1-terminus` | $0.27 / $0.135 / $1 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/deepseek/deepseek-v3.1-terminus) · [Rate limits](https://openrouter.ai/docs/faq) |

#### DeepSeek-R1

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/deepseek-ai/DeepSeek-R1` | ¥4 / ¥0.4 / ¥16 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `deepseek-ai/DeepSeek-R1` | ¥4 / ¥0.4 / ¥16 | 1,000 RPM / 100,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `deepseek/deepseek-r1` | $0.7 / — / $2.5 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/deepseek/deepseek-r1) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-bytedance-seed-doubao"></a>

<details>
<summary><strong>ByteDance Seed / Doubao</strong> · 33 models · 41 provider records</summary>

#### doubao-seed-evolving

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-evolving` | ¥6 / ¥1.2 / ¥30 | 500 RPM / 1M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-1-pro

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-1-pro-260628` | ¥6 / ¥1.2 / ¥30 | 500 RPM / 1M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-1-turbo

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-1-turbo-260628` | ¥3 / ¥0.6 / ¥15 | 500 RPM / 1M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-pro

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-pro-260215` | ≤32K ¥3.2/¥0.64/¥16；32–128K ¥4.8/¥0.96/¥24；128–256K ¥9.6/¥1.92/¥48 | 30K RPM / 5M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-code-preview

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-code-preview-260215` | ≤32K ¥3.2/¥0.64/¥16；32–128K ¥4.8/¥0.96/¥24；128–256K ¥9.6/¥1.92/¥48 | 30K RPM / 5M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-lite

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-lite-260428` | ≤32K ¥0.6/¥0.12/¥3.6；32–128K ¥0.9/¥0.18/¥5.4；128–256K ¥1.8/¥0.36/¥10.8 | 30K RPM / 5M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-lite-260215` | ≤32K ¥0.6/¥0.12/¥3.6；32–128K ¥0.9/¥0.18/¥5.4；128–256K ¥1.8/¥0.36/¥10.8 | 30K RPM / 5M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-2-0-mini

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-mini-260428` | ≤32K ¥0.2/¥0.04/¥2；32–128K ¥0.4/¥0.08/¥4；128–256K ¥0.8/¥0.16/¥8 | 30K RPM / 5M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-2-0-mini-260215` | ≤32K ¥0.2/¥0.04/¥2；32–128K ¥0.4/¥0.08/¥4；128–256K ¥0.8/¥0.16/¥8 | 30K RPM / 5M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-character

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-character-260628` | ≤32K ¥0.8/¥0.16/¥2；32–128K ¥1.2/¥0.16/¥6 | 30K RPM / 5M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-character-251128` | ≤32K ¥0.8/¥0.16/¥2；32–128K ¥1.2/¥0.16/¥6 | 30K RPM / 5M TPM | Historical | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-8

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-1-8-251228` | ¥0.8–2.4 / ¥0.16 / ¥2–24 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-code-preview

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-code-preview-251028` | ¥1.2–2.8 / ¥0.24 / ¥8–16 | 5K RPM / 1.2M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-6

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-251015` | ¥0.8–2.4 / ¥0.16 / ¥2–24 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-250615` | ¥0.8–2.4 / ¥0.16 / ¥2–24 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-6-flash

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-flash-250828` | ¥0.15–0.6 / ¥0.03 / ¥1.5–6 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-flash-250615` | ¥0.15–0.6 / ¥0.03 / ¥1.5–6 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-1-6-vision

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-1-6-vision-250815` | ¥0.8–2.4 / ¥0.16 / ¥8–24 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seed-translation

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed-translation-250915` | ¥1.2 / — / ¥3.6 | 5K RPM / 500K TPM | Historical | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-pro-32k

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-1-5-pro-32k-250115` | ¥0.8 / ¥0.16 / ¥2 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-pro-32k-character

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-1-5-pro-32k-character-250715` | ¥0.8 / ¥0.16 / ¥2 | 15K RPM / 10M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-lite-32k

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-1-5-lite-32k-250115` | ¥0.3 / ¥0.06 / ¥0.6 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-1-5-vision-pro-32k

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-1-5-vision-pro-32k-250115` | ¥3 / — / ¥9 | 30K RPM / 5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedance-2-5-260628` | ¥42–77 / M Tokens | Enterprise: 600 RPM / 10 CC; Individual: 180 RPM / 3 CC | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedance-2-0-260128` | ¥16–51 / M Tokens | Enterprise: 600 RPM / 10 CC; Individual: 180 RPM / 3 CC | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-0-fast

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedance-2-0-fast-260128` | ¥22–37 / M Tokens (promotional discounts excluded) | Enterprise: 600 RPM / 10 CC; Individual: 180 RPM / 3 CC | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-2-0-mini

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedance-2-0-mini-260615` | ¥14–23 / M Tokens (promotional discounts excluded) | Enterprise: 600 RPM / 10 CC; Individual: 180 RPM / 3 CC | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-1-5-pro

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedance-1-5-pro-251215` | With audio ¥16 / Without audio ¥8 / M Tokens | 600 RPM / 10 CC | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-1-0-pro

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedance-1-0-pro-250528` | ¥15 / M Tokens | 600 RPM / 10 CC | Historical | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedance-1-0-pro-fast

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedance-1-0-pro-fast-251015` | ¥4.2 / M Tokens | 600 RPM / 10 CC | Historical | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-5-0-pro

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedream-5-0-pro-260628` | First input image free, then ¥0.02/image；Output ¥0.15–0.60/image | 500 IPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-5-0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedream-5-0-260128` | ¥0.22 / image | 500 IPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-5-0-lite

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedream-5-0-lite-260128` | ¥0.22 / image | 500 IPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Together AI](https://www.together.ai/) | `ByteDance/Seedream-5.0-lite` | $0.035 / MP | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |

#### doubao-seedream-4-5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedream-4-5-251128` | ¥0.25 / image | 500 IPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-seedream-4-0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seedream-4-0-250828` | ¥0.20 / image | 500 IPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Together AI](https://www.together.ai/) | `ByteDance-Seed/Seedream-4.0` | $0.03 / MP | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |

#### doubao-seed3d-2-0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-seed3d-2-0-260328` | ¥2.40 / request | 300 RPM / 5 CC | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### doubao-embedding-vision

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-embedding-vision-251215` | Text ¥0.70 / Image ¥1.80 / M Tokens | 15K RPM / 1.2M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `doubao-embedding-vision-250615` | Text ¥0.70 / Image ¥1.80 / M Tokens | 15K RPM / 1.2M TPM | Historical | [Official](https://www.volcengine.com/docs/82379/1544106) |

#### Seed-OSS-36B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `ByteDance-Seed/Seed-OSS-36B-Instruct` | ¥1.5 / — / ¥4 | 1,000 RPM / 20,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-qwen"></a>

<details>
<summary><strong>Qwen</strong> · 41 models · 67 provider records</summary>

#### Qwen 3.8 Max

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Alibaba Cloud Model Studio](https://www.aliyun.com/product/bailian) | `qwen3.8-max` | ¥12.00 / ¥1.50¹ / ¥36.00 | Beijing: 30K RPM / 5M TPM | Available | [Pricing](https://help.aliyun.com/zh/model-studio/qwen3-8-max) · [Rate limits](https://help.aliyun.com/zh/model-studio/rate-limit) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/qwen3p8-max` | $2.00 / $0.25 / $6.00 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/qwen3p8-max) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.8-max` | $2 / $0.25 / $6 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.8-max) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen 3.7 Max

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen3.7-Max` | $1.25 / — / $3.75 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.7-max` | $1.475 / $0.295 / $4.425 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.7-max) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3.5-4B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.5-4B` | Free | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-8B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-8B` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-8b` | $0.117 / — / $0.455 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-8b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen2.5-7B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen2.5-7B-Instruct` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/Qwen/Qwen2.5-7B-Instruct` | ¥0.35 / — / ¥0.35 | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen2.5-7B-Instruct-Turbo` | $0.30 / — / $0.30 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen-2.5-7b-instruct` | $0.1 / — / $0.2 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen-2.5-7b-instruct) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen2.5-14B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen2.5-14B-Instruct` | ¥0.7 / — / ¥0.7 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen2.5-32B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen2.5-32B-Instruct` | ¥1.26 / — / ¥1.26 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3.5-397B-A17B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.5-397B-A17B` | Input [0, 128K): ¥1.2 / — / ¥7.2<br>Input [128K, +∞): ¥3 / — / ¥18 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-397b-a17b` | $0.5 / $0.3 / $3.6 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.5-397b-a17b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-8B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-8B-Instruct` | ¥0.5 / — / ¥2 | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-8b-instruct` | $0.117 / — / $0.455 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-vl-8b-instruct) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-14B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-14B` | ¥0.5 / — / ¥2 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-14b` | $0.12 / — / $0.24 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-14b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-30B-A3B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-30B-A3B-Instruct` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-30b-a3b-instruct` | $0.13 / — / $0.52 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-vl-30b-a3b-instruct) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-30B-A3B-Thinking

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-30B-A3B-Thinking` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-30b-a3b-thinking` | $0.2 / — / $2.4 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-vl-30b-a3b-thinking) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-Omni-30B-A3B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Omni-30B-A3B-Instruct` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Omni-30B-A3B-Thinking

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Omni-30B-A3B-Thinking` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Omni-30B-A3B-Captioner

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Omni-30B-A3B-Captioner` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Coder-30B-A3B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Coder-30B-A3B-Instruct` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-coder-30b-a3b-instruct` | $0.07 / — / $0.28 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-coder-30b-a3b-instruct) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-30B-A3B-Instruct-2507

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-30B-A3B-Instruct-2507` | ¥0.7 / — / ¥2.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-30b-a3b-instruct-2507` | $0.04815 / — / $0.19305 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-30b-a3b-instruct-2507) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-32B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-32B-Instruct` | ¥1 / — / ¥4 | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-32b-instruct` | $0.104 / — / $0.416 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-vl-32b-instruct) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-32B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-32B` | ¥1 / — / ¥4 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-32b` | $0.08 / — / $0.28 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-32b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen2.5-72B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen2.5-72B-Instruct` | ¥4.13 / — / ¥4.13 | 1,000 RPM / 20,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen-2.5-72b-instruct` | $0.36 / — / $0.4 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen-2.5-72b-instruct) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen2.5-72B-Instruct-128K

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen2.5-72B-Instruct-128K` | ¥4.13 / — / ¥4.13 | 1,000 RPM / 20,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-VL-8B-Thinking

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-8B-Thinking` | ¥0.5 / — / ¥5 | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3-vl-8b-thinking` | $0.18 / — / $2.1 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3-vl-8b-thinking) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-VL-32B-Thinking

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-32B-Thinking` | ¥1 / — / ¥10 | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3.5-9B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.5-9B` | Input [0, 128K): ¥0.5 / — / ¥4<br>Input [128K, +∞): ¥1.5 / — / ¥12 | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen3.5-9B` | $0.17 / — / $0.25 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-9b` | $0.1 / — / $0.15 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.5-9b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3.6-35B-A3B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.6-35B-A3B` | ¥1.8 / — / ¥10.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.6-35b-a3b` | $0.14 / $0.05 / $1 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.6-35b-a3b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3.5-35B-A3B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.5-35B-A3B` | Input [0, 128K): ¥0.4 / — / ¥3.2<br>Input [128K, +∞): ¥1.6 / — / ¥12.8 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-35b-a3b` | $0.25 / $0.25 / $1.25 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.5-35b-a3b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3.6-27B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.6-27B` | ¥3 / — / ¥18 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.6-27b` | $0.32 / — / $3.2 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.6-27b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3.5-27B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.5-27B` | Input [0, 128K): ¥0.6 / — / ¥4.8<br>Input [128K, +∞): ¥1.8 / — / ¥14.4 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-27b` | $0.195 / — / $1.56 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.5-27b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3.5-122B-A10B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3.5-122B-A10B` | Input [0, 128K): ¥0.8 / — / ¥6.4<br>Input [128K, +∞): ¥2 / — / ¥16 | 1,000 RPM / 20,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `qwen/qwen3.5-122b-a10b` | $0.26 / — / $2.08 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/qwen/qwen3.5-122b-a10b) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Qwen3-Embedding-0.6B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Embedding-0.6B` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Reranker-0.6B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Reranker-0.6B` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Embedding-4B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Embedding-4B` | ¥0.14 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Reranker-4B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Reranker-4B` | ¥0.14 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Embedding-8B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Embedding-8B` | ¥0.28 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-Reranker-8B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-Reranker-8B` | ¥0.28 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-VL-Reranker-8B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-Reranker-8B` | Text ¥0.7 / Image ¥1.8 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-VL-Embedding-8B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-VL-Embedding-8B` | Text ¥0.7 / Image ¥1.8 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen-Image

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen-Image` | ¥0.3 / image | Dynamic limits | Available | [Official](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `Qwen/Qwen-Image` | $0.0058 / MP | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |

#### Qwen-Image-Edit

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen-Image-Edit` | ¥0.3 / image | Dynamic limits | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen-Image-Edit-2509

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen-Image-Edit-2509` | ¥0.3 / image | Dynamic limits | Available | [Official](https://siliconflow.cn/pricing) |

#### Qwen3-ASR-1.7B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Qwen/Qwen3-ASR-1.7B` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-glm"></a>

<details>
<summary><strong>GLM</strong> · 8 models · 19 provider records</summary>

#### GLM 5.2

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Zhipu AI Open Platform](https://bigmodel.cn/) | `glm-5.2` | ¥8.00 / ¥2.00 / ¥28.00 | Dynamic concurrency by account entitlement and model | Available | [Pricing](https://bigmodel.cn/pricing) · [Rate limits](https://docs.bigmodel.cn/cn/api/rate-limit) |
| [Mistral AI](https://mistral.ai/) | GLM 5.2 | $1.40 / $0.14 / $4.40 | See console; varies by subscription and model | Available | [Pricing](https://docs.mistral.ai/inference/pricing) · [Rate limits](https://docs.mistral.ai/resources/known-limitations) |
| [Tencent Cloud TokenHub](https://cloud.tencent.com/product/tokenhub) | GLM 5.2 | ¥10.254 / ¥1.9044 / ¥32.2282 | Varies by account and model | Available | [Pricing](https://cloud.tencent.cn/document/product/1823/130055) |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `glm-5-2-260617` | ¥8 / ¥2 / ¥28 | 500 RPM / 1M TPM | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [SiliconFlow](https://siliconflow.cn/) | `zai-org/GLM-5.2` | ¥8 / ¥2 / ¥28 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `zai-org/GLM-5.2` | $1.40 / $0.26 / $4.40 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/glm-5p2` | $1.40 / $0.14 / $4.40 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/glm-5p2) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-5.2` | $1.19 / $0.221 / $3.74 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/z-ai/glm-5.2) · [Rate limits](https://openrouter.ai/docs/faq) |

#### GLM 4.7

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `glm-4-7-251222` | ¥2–4 / ¥0.4–0.8 / ¥8–16 | 15K RPM / 1.5M TPM | Retiring soon | [Official](https://www.volcengine.com/docs/82379/1544106) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-4.7` | $0.4 / $0.08 / $1.75 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/z-ai/glm-4.7) · [Rate limits](https://openrouter.ai/docs/faq) |

#### GLM-Z1-9B-0414

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `THUDM/GLM-Z1-9B-0414` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### GLM-4-9B-0414

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `THUDM/GLM-4-9B-0414` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### GLM-4-32B-0414

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `THUDM/GLM-4-32B-0414` | ¥1.89 / — / ¥1.89 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### GLM-4.5V

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `zai-org/GLM-4.5V` | ¥1 / — / ¥6 | 1,000 RPM / 20,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-4.5v` | $0.6 / $0.11 / $1.8 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/z-ai/glm-4.5v) · [Rate limits](https://openrouter.ai/docs/faq) |

#### GLM-4.5-Air

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `zai-org/GLM-4.5-Air` | ¥1 / — / ¥6 | 1,000 RPM / 20,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-4.5-air` | $0.13 / $0.025 / $0.85 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/z-ai/glm-4.5-air) · [Rate limits](https://openrouter.ai/docs/faq) |

#### GLM-5.1

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/zai-org/GLM-5.1` | Input [0, 32K): ¥6 / ¥1.3 / ¥24<br>Input [32K, +∞): ¥8 / ¥2 / ¥28 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `z-ai/glm-5.1` | $1.26 / $0.234 / $3.96 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/z-ai/glm-5.1) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-kimi"></a>

<details>
<summary><strong>Kimi</strong> · 3 models · 13 provider records</summary>

#### Kimi K3

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Kimi Open Platform](https://platform.kimi.com/) | `kimi-k3` | ¥20.00 / ¥2.00 / ¥100.00 | Based on cumulative top-up tier | Available | [Pricing](https://platform.kimi.com/) · [Rate limits](https://platform.kimi.com/docs/pricing/limits) |
| [Together AI](https://www.together.ai/) | `moonshotai/Kimi-K3` | $3.00 / $0.30 / $15.00 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/kimi-k3` | $3.00 / $0.30 / $15.00 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/kimi-k3) |
| [OpenRouter](https://openrouter.ai/) | `moonshotai/kimi-k3` | $3 / $0.3 / $15 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/moonshotai/kimi-k3) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Kimi K2.7 Code

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Kimi Open Platform](https://platform.kimi.com/) | `kimi-k2.7-code` | ¥6.50 / ¥1.30 / ¥27.00 | Tier 0: 1 CC / 3 RPM / 500K TPM / 1.5M TPD | Available | [Pricing](https://platform.kimi.com/) · [Rate limits](https://platform.kimi.com/docs/pricing/limits) |
| [SiliconFlow](https://siliconflow.cn/) | `moonshotai/Kimi-K2.7-Code` | ¥6.5 / ¥1.3 / ¥27 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [Together AI](https://www.together.ai/) | `moonshotai/Kimi-K2.7-Code` | $0.95 / $0.19 / $4.00 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/kimi-k2p7-code` | $0.95 / $0.19 / $4.00 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/kimi-k2p7-code) |
| [OpenRouter](https://openrouter.ai/) | `moonshotai/kimi-k2.7-code` | $0.67 / $0.19 / $3.4 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/moonshotai/kimi-k2.7-code) · [Rate limits](https://openrouter.ai/docs/faq) |

#### Kimi K2.6

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Kimi Open Platform](https://platform.kimi.com/) | `kimi-k2.6` | ¥6.50 / ¥1.10 / ¥27.00 | No TPD cap from Tier 1 | Available | [Pricing](https://platform.kimi.com/) · [Rate limits](https://platform.kimi.com/docs/pricing/limits) |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/moonshotai/Kimi-K2.6` | ¥6.5 / ¥1.1 / ¥27 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/kimi-k2p6` | $0.95 / $0.16 / $4.00 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/kimi-k2p6) |
| [OpenRouter](https://openrouter.ai/) | `moonshotai/kimi-k2.6` | $0.95 / $0.16 / $4 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/moonshotai/kimi-k2.6) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-minimax"></a>

<details>
<summary><strong>MiniMax</strong> · 5 models · 11 provider records</summary>

#### MiniMax M3

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Together AI](https://www.together.ai/) | `MiniMaxAI/MiniMax-M3` | $0.30 / $0.06 / $1.20 | Dynamic serverless limits | Available | [Model catalog](https://docs.together.ai/docs/serverless/models) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/minimax-m3` | $0.30 / $0.06 / $1.20 | Dynamic serverless limits | Available | [Pricing catalog](https://docs.fireworks.ai/serverless/pricing) |

#### MiniMax M2.7

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.7` | ¥2.10 / ¥0.42 / ¥8.40 | Dynamic peak-hour limits | Available | [Pricing](https://platform.minimaxi.com/docs/guides/pricing-paygo) · [Rate-limit notes](https://platform.minimaxi.com/docs/token-plan/faq) |
| [Fireworks AI](https://fireworks.ai/) | `accounts/fireworks/models/minimax-m2p7` | $0.30 / $0.06 / $1.20 | Dynamic serverless limits | Available | [Model & pricing](https://app.fireworks.ai/models/fireworks/minimax-m2p7) |
| [OpenRouter](https://openrouter.ai/) | `minimax/minimax-m2.7` | $0.3 / $0.06 / $1.2 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/minimax/minimax-m2.7) · [Rate limits](https://openrouter.ai/docs/faq) |

#### MiniMax-M2.7-highspeed

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.7-highspeed` | ¥4.20 / ¥0.42 / ¥16.80 | Depends on subscription tier | Available | [Pricing](https://platform.minimaxi.com/docs/guides/pricing-paygo) |

#### MiniMax-M2.5-highspeed

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.5-highspeed` | ¥4.20 / ¥0.21 / ¥16.80 | Depends on subscription tier | Available | [Pricing](https://platform.minimaxi.com/docs/guides/pricing-paygo) |

#### MiniMax-M2.5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [MiniMax](https://www.minimaxi.com/) | `MiniMax-M2.5` | ¥2.10 / ¥0.21 / ¥8.40 | Varies by account tier | Available | [Pricing](https://platform.minimaxi.com/docs/guides/pricing-paygo) |
| [SiliconFlow](https://siliconflow.cn/) | `MiniMaxAI/MiniMax-M2.5` | ¥2.1 / ¥0.21 / ¥8.4 | 1,000 RPM / 100,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/MiniMaxAI/MiniMax-M2.5` | ¥2.1 / ¥0.21 / ¥8.4 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `minimax/minimax-m2.5` | $0.27 / $0.027 / $1.08 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/minimax/minimax-m2.5) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-mistral"></a>

<details>
<summary><strong>Mistral</strong> · 3 models · 4 provider records</summary>

#### mistral-large-2512

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Mistral AI](https://mistral.ai/) | `mistral-large-2512` | $0.50 / $0.05 / $1.50 | See console; varies by subscription and model | Available | [Pricing](https://docs.mistral.ai/inference/pricing) · [Rate limits](https://docs.mistral.ai/resources/known-limitations) |
| [OpenRouter](https://openrouter.ai/) | `mistralai/mistral-large-2512` | $0.5 / $0.05 / $1.5 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/mistralai/mistral-large-2512) · [Rate limits](https://openrouter.ai/docs/faq) |

#### mistral-medium-latest

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Mistral AI](https://mistral.ai/) | `mistral-medium-latest` | $1.50 / $0.15 / $7.50 | Separate RPS and TPM limits | Available | [Pricing](https://docs.mistral.ai/inference/pricing) |

#### mistral-small-latest

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Mistral AI](https://mistral.ai/) | `mistral-small-latest` | $0.15 / $0.015 / $0.60 | Batch does not consume realtime quota | Available | [Pricing](https://docs.mistral.ai/inference/pricing) · [Limits](https://docs.mistral.ai/resources/known-limitations) |

</details>

<a id="family-ernie-paddleocr"></a>

<details>
<summary><strong>ERNIE / PaddleOCR</strong> · 4 models · 5 provider records</summary>

#### ERNIE 5.1

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Baidu AI Cloud Qianfan](https://cloud.baidu.com/product-s/qianfan_home) | `ERNIE-5.1` ≤32K input | ¥4.00 / — / ¥18.00 | Varies by account and service instance | Available | [Pricing](https://cloud.baidu.com/doc/qianfan/s/wmh4sv6ya) |
| [Baidu AI Cloud Qianfan](https://cloud.baidu.com/product-s/qianfan_home) | `ERNIE-5.1` 32K–128K input | ¥6.00 / — / ¥22.00 | Varies by account and service instance | Available | [Pricing](https://cloud.baidu.com/doc/qianfan/s/wmh4sv6ya) |

#### ERNIE 4.5 Turbo 128K Preview

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Baidu AI Cloud Qianfan](https://cloud.baidu.com/product-s/qianfan_home) | `ERNIE-4.5-Turbo-128K-Preview` | ¥0.80 / ¥0.20 / ¥3.20 | Varies by account and service instance | Available | [Pricing](https://cloud.baidu.com/doc/qianfan/s/wmh4sv6ya) |

#### PaddleOCR-VL-1.5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `PaddlePaddle/PaddleOCR-VL-1.5` | Free | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### ERNIE-Image-Turbo

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `baidu/ERNIE-Image-Turbo` | ¥0.11 / image | Dynamic limits | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-hunyuan"></a>

<details>
<summary><strong>Hunyuan</strong> · 2 models · 3 provider records</summary>

#### Hunyuan-MT-7B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `tencent/Hunyuan-MT-7B` | Free | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Hunyuan-A13B-Instruct

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `tencent/Hunyuan-A13B-Instruct` | 09:00–18:00: ¥1 / — / ¥4<br>Other hours: ¥0.8 / — / ¥3.2 | 1,000 RPM / 20,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `tencent/hunyuan-a13b-instruct` | $0.14 / — / $0.57 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/tencent/hunyuan-a13b-instruct) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-bge"></a>

<details>
<summary><strong>BGE</strong> · 4 models · 6 provider records</summary>

#### bge-m3

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `BAAI/bge-m3` | Free | 2,000 RPM / 500,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/BAAI/bge-m3` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### bge-reranker-v2-m3

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `BAAI/bge-reranker-v2-m3` | Free | 2,000 RPM / 500,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [SiliconFlow](https://siliconflow.cn/) | `Pro/BAAI/bge-reranker-v2-m3` | ¥0.07 / M Tokens | 2,000 RPM / 1,000,000 TPM / 1 IPM / 1,440 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### bge-large-zh-v1.5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `BAAI/bge-large-zh-v1.5` | Free | 2,000 RPM / 500,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### bge-large-en-v1.5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `BAAI/bge-large-en-v1.5` | Free | 2,000 RPM / 500,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-longcat"></a>

<details>
<summary><strong>LongCat</strong> · 1 models · 2 provider records</summary>

#### LongCat-2.0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `meituan-longcat/LongCat-2.0` | ¥5 / ¥0.1 / ¥20 | 500 RPM / 2,000,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `meituan/longcat-2.0` | $0.3 / $0.006 / $1.2 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/meituan/longcat-2.0) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-ling"></a>

<details>
<summary><strong>Ling</strong> · 2 models · 2 provider records</summary>

#### Ling-mini-2.0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `inclusionAI/Ling-mini-2.0` | ¥0.5 / — / ¥2 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### Ling-flash-2.0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `inclusionAI/Ling-flash-2.0` | ¥1 / — / ¥4 | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-step"></a>

<details>
<summary><strong>Step</strong> · 1 models · 3 provider records</summary>

#### Step-3.5-Flash

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `stepfun-ai/Step-3.5-Flash` | ¥0.7 / — / ¥2.1 | 1,000 RPM / 10,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [StepFun](https://platform.stepfun.com/) | `step-3.5-flash` | ¥0.70 / ¥0.14 / ¥2.10 | Varies by account tier | Available | [Pricing & rate limits](https://platform.stepfun.com/docs/zh/guides/pricing/details) |
| [OpenRouter](https://openrouter.ai/) | `stepfun/step-3.5-flash` | $0.1 / — / $0.3 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/stepfun/step-3.5-flash) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-nex"></a>

<details>
<summary><strong>Nex</strong> · 1 models · 2 provider records</summary>

#### Nex-N2-Pro

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `nex-agi/Nex-N2-Pro` | ¥1.75 / ¥0.175 / ¥7 | 1,000 RPM / 80,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |
| [OpenRouter](https://openrouter.ai/) | `nex-agi/nex-n2-pro` | $0.25 / $0.025 / $1 | Varies by balance and upstream routing | Available | [Model & pricing](https://openrouter.ai/nex-agi/nex-n2-pro) · [Rate limits](https://openrouter.ai/docs/faq) |

</details>

<a id="family-xingchen"></a>

<details>
<summary><strong>XingChen</strong> · 4 models · 4 provider records</summary>

#### XingChenASR-V3.2-Ultra

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `XingChenAGI/XingChenASR-V3.2-Ultra` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### XingChenASR-Diarize-V3.0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `XingChenAGI/XingChenASR-Diarize-V3.0` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### XingChenGSR-V1.0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `XingChenAGI/XingChenGSR-V1.0` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### XingChenASR-V3.2

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `XingChenAGI/XingChenASR-V3.2` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-funaudiollm"></a>

<details>
<summary><strong>FunAudioLLM</strong> · 2 models · 2 provider records</summary>

#### SenseVoiceSmall

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `FunAudioLLM/SenseVoiceSmall` | Free | 1,000 RPM / 50,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

#### CosyVoice2-0.5B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `FunAudioLLM/CosyVoice2-0.5B` | ¥0.05 / 1K UTF-8 characters | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-moss"></a>

<details>
<summary><strong>MOSS</strong> · 1 models · 1 provider records</summary>

#### MOSS-TTSD-v0.5

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `fnlp/MOSS-TTSD-v0.5` | ¥0.05 / 1K UTF-8 characters | 1,000 RPM / 40,000 TPM | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-wan"></a>

<details>
<summary><strong>Wan</strong> · 2 models · 2 provider records</summary>

#### Wan2.2-T2V-A14B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Wan-AI/Wan2.2-T2V-A14B` | ¥2 / generation | 5 IPM / 200 IPD | Available | [Official](https://siliconflow.cn/pricing) |

#### Wan2.2-I2V-A14B

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Wan-AI/Wan2.2-I2V-A14B` | ¥2 / generation | 5 IPM / 200 IPD | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-kolors"></a>

<details>
<summary><strong>Kolors</strong> · 1 models · 1 provider records</summary>

#### Kolors

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Kwai-Kolors/Kolors` | Free | 2 IPM / 400 IPD | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-z-image"></a>

<details>
<summary><strong>Z-Image</strong> · 2 models · 2 provider records</summary>

#### Z-Image-Turbo

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Tongyi-MAI/Z-Image-Turbo` | ¥0.1 / image | Dynamic limits | Available | [Official](https://siliconflow.cn/pricing) |

#### Z-Image

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [SiliconFlow](https://siliconflow.cn/) | `Tongyi-MAI/Z-Image` | ¥0.3 / image | Dynamic limits | Available | [Official](https://siliconflow.cn/pricing) |

</details>

<a id="family-hyper3d"></a>

<details>
<summary><strong>Hyper3D</strong> · 1 models · 1 provider records</summary>

#### hyper3d-gen2

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `hyper3d-gen2-260112` | ¥1.80 / request | 60 RPM / 3 CC | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

</details>

<a id="family-hitem3d"></a>

<details>
<summary><strong>Hitem3D</strong> · 1 models · 1 provider records</summary>

#### hitem3d-2-0

| API provider | Model ID | Price | Quota | Status | Source |
| --- | --- | --- | --- | --- | --- |
| [Volcengine Ark](https://www.volcengine.com/product/ark) | `hitem3d-2-0-251223` | ¥5.80–13.05 / request | 600 RPM / 30 CC | Available | [Official](https://www.volcengine.com/docs/82379/1544106) |

</details>

## Quota notes

An API `quota` is rarely a single fixed number. It may depend on the model, organization, account tier, cumulative spend, region, and burst traffic.

- Explicit values are public defaults or region-specific limits and do not represent enterprise maximums.
- “Dynamic limits” means the provider only shows the actual quota in the signed-in console or adjusts it with cluster load.
- Whether cached tokens count toward TPM varies by provider. Most Claude models count only uncached input, while xAI includes cached tokens in TPM.

## Methodology

This page includes prices that meet the following criteria:

1. The model is currently callable through an API; retired models or snapshots are retained only when explicitly marked Historical.
2. Pricing can be verified on an official provider or hosting-platform page.
3. Billing units and applicable conditions are clearly identifiable.
4. Preview status, regional prices, promotional prices, and long-context premiums are explicitly labeled.
5. Prices for the same open-weight model are recorded separately by platform; the model developer is not treated as the only provider.


## Contributing

Prices change quickly. Issues and pull requests are welcome. When updating a price, include:

- Model ID and provider;
- Original currency and billing unit;
- Input, cached-input, and output prices;
- Region, context tier, Batch or high-speed service tier;
- Quota and applicable account tier;
- Official source URL and verification date.

---

<div align="center">

Data is provided for technical evaluation and cost estimation only; it is not purchasing or financial advice.

This table was compiled with AI assistance.

</div>
