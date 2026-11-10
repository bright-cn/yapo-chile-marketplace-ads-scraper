# Yapo 智利分类广告抓取工具

[![Bright Data](https://img.shields.io/badge/Powered%20by-Bright%20Data-FF9A00?style=flat-square)](https://www.bright.cn/) [![爬虫工具 API](https://img.shields.io/badge/Scraper%20API-Available-FF9A00?style=flat-square)](https://www.bright.cn/products/web-scraper/yapo) [![数据集](https://img.shields.io/badge/Dataset-Available-0066CC?style=flat-square)](https://www.bright.cn/products/datasets/yapo) [![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat-square&logo=python&logoColor=white)](https://python.org) [![许可证：MIT](https://img.shields.io/badge/License-MIT-22C55E?style=flat-square)](LICENSE)

[![推广](https://github.com/bright-cn/Awesome-Web-Scraping/raw/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner%20CN.png)](https://www.bright.cn/products/web-scraper/yapo)

> **由 [Bright Data](https://www.bright.cn/) 提供支持的 Yapo Chile 市场广告数据。**

此代码库提供两种大规模访问 Yapo Chile 市场广告数据的方法：

- **[方法 1：Bright Data Yapo Chile 市场广告爬虫工具 API](#方法-1bright-data-yapo-chile-市场广告爬虫工具-api)**（推荐）- 完全托管的企业级爬虫 API，可自动处理代理、CAPTCHA 和扩展。
- **[方法 2：Bright Data Yapo Chile 市场广告数据集](#方法-2bright-data-yapo-chile-市场广告数据集)** - 可直接下载的预采集 Yapo Chile 市场广告数据集，无需进行网页爬虫。

## 目录

- [为什么使用 Bright Data 抓取 Yapo Chile 市场广告？](#为什么使用-bright-data-抓取-yapo-chile-市场广告)
- [方法 1：Bright Data Yapo Chile 市场广告爬虫工具 API](#方法-1bright-data-yapo-chile-市场广告爬虫工具-api)
  - [快速入门](#yapo-chile-市场广告爬虫工具-api-快速入门)
  - [1. Yapo Chile 市场广告平台商品列表](#1-yapo-chile-市场广告平台商品列表)
- [方法 2：Bright Data Yapo Chile 市场广告数据集](#方法-2bright-data-yapo-chile-市场广告数据集)
- [数据采集方法](#数据采集方法)

## 为什么使用 Bright Data 抓取 Yapo Chile 市场广告？

抓取 Yapo Chile 市场广告面临多项挑战：

- 速率限制：Yapo Chile 市场广告平台会监控请求频率，并可能封禁超出限制的 IP。
- CAPTCHA 检测：自动访问可能触发 CAPTCHA 验证。
- 身份验证障碍：部分数据需要登录才能访问，而且平台会检测自动化尝试。
- 动态内容加载：使用 JavaScript 渲染的内容很难通过简单的 HTTP 请求抓取。
- IP 封禁：从同一 IP 重复发送请求可能导致封禁。

Bright Data 的 Yapo Chile 市场广告爬虫工具 API 通过以下功能解决这些问题：

- ✅ **内置动态代理**：自动绕过基于 IP 的速率限制
- ✅ **验证码破解**：无需任何额外设置即可应对机器人检测
- ✅ **结构化数据输出**：获取可直接用于分析的整洁 JSON
- ✅ **无需基础设施**：云端托管，可支持任意规模的抓取
- ✅ **99.9% 正常运行时间 SLA**：为业务关键型工作流提供可靠的数据采集

## 方法 1：Bright Data Yapo Chile 市场广告爬虫工具 API

[Bright Data Yapo Chile 市场广告爬虫工具 API](https://www.bright.cn/products/web-scraper/yapo) 是一种完全托管的解决方案，无需进行任何基础设施设置。

### Yapo Chile 市场广告爬虫工具 API 快速入门

1. **注册**[免费 Bright Data 账户](https://www.bright.cn/)
2. **前往**[Yapo Chile 市场广告爬虫工具 API](https://www.bright.cn/products/web-scraper/yapo)
3. 从控制面板**获取 API 令牌**
4. **安装** `requests` 库：`pip install requests`
5. **运行** `yapo-chile-marketplace-ads_scraper_api_codes/` 中的任意脚本

### 1. Yapo Chile 市场广告平台商品列表

从 Yapo Chile 市场广告平台采集商品列表。

#### 输入参数

| 字段 | 类型 | 必填 | 说明 |
|-------|------|----------|-------------|
| `url` | 字符串 | 是 | 要抓取的 Yapo Chile 市场广告条目的 URL |
| `limit` | 整数 | 否 | 返回结果的最大数量 |
| `include_errors` | 布尔值 | 否 | 在响应中包含错误详情 |
| `notify` | URL | 否 | 数据采集完成时用于接收通知的 Webhook URL |
| `format` | 枚举 | 否 | 输出格式：`JSON`、`NDJSON`、`JSON Lines`、`CSV` |

#### 响应示例

```json
{
  "db_source": "1774452388078",
  "description": "Espectacular departamento en exclusivo edificio de La DehesaEn un entorno tranquilo y residencial, con excelente conecti...",
  "root_category_name": "Inmuebles",
  "seller_name": "Maria *** S*****t",
  "title": "Departamentos en Regi\u00f3n Metropolitana | Exclusivo departamento con ascensor privado y vista al valle      \n\n    ..."
}
```

👉 查看[完整 Python 代码](yapo-chile-marketplace-ads_scraper_api_codes/yapo_chile_marketplace_ads_scraper.py)

## 方法 2：Bright Data Yapo Chile 市场广告数据集

如果你需要无需编写任何抓取代码即可直接使用的数据，[Bright Data Yapo Chile 市场广告数据集](https://www.bright.cn/products/datasets/yapo)提供预先采集、定期更新且可立即下载的数据。

**为什么使用数据集而不是 API？**

- 📦 **即时访问**：无需设置、无需代码，也无需等待采集
- 🔄 **定期更新**：按照固定计划持续刷新最新数据
- 📊 **多种格式**：可下载为 JSON、JSONL 或 CSV
- 🌍 **超大规模**：涵盖 Yapo Chile 市场广告所有主要类别的数百万条记录
- ✅ **完全合规**：数据来源符合道德规范，并通过法律合规审查

👉 **[探索 Yapo Chile 市场广告数据集](https://www.bright.cn/products/datasets/yapo)**

## 数据采集方法

| 功能 | Bright Data 爬虫工具 API | Bright Data 数据集 |
|---------|------------------------|---------------------|
| 所需设置 | 仅需 API 令牌 | 无需设置 |
| 实时数据 | ✅ 是 | ❌ 预先采集 |
| 自定义查询 | ✅ 完全控制 | ❌ 固定结构 |
| 包含代理 | ✅ 内置动态代理 | N/A |
| CAPTCHA 破解 | ✅ 自动 | N/A |
| 规模 | 无限制 | 无限制 |
| 结构化输出 | ✅ JSON / NDJSON / JSON Lines / CSV | ✅ JSON / JSONL / CSV |
| 支持 | 企业级全天候支持 | 企业级全天候支持 |

---

🔗 **了解更多**：[https://www.bright.cn/products/web-scraper/yapo](https://www.bright.cn/products/web-scraper/yapo)
