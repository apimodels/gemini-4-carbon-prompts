# Long agentic coding sessions: Carbon vs Opus 5.5 vs Fable 5.2

Gemini 4 Carbon case 209 of 223 · Apps, Real Codebases and Tooling · [简体中文](#中文)

By Bito · [original post](https://bito.ai/blog/gemini-4-carbon-vs-claude-opus-5-5-fable-5-2-coding/) · 2026-11-11 · [see it in the apimodels.app gallery](https://apimodels.app/gemini-4-carbon-prompts/code)

- **What it is:** Long agentic coding sessions on production services, with the Claude models in Claude Code at medium effort, Carbon through Google AI Studio at default thinking, and a judge model with a fixed answer key. Carbon scored lowest overall and took longest, but cost the least per session.
- **Where:** blog
- **Tool:** Google AI Studio
- **Numbers the author reported:** overall: Opus 85.0%, Fable 83.1%, Carbon 79.5% · one-shot: Carbon 89.1% (Fable 89.4%) · cost per long session: Carbon $2.75, Opus $5.42, Fable $8.13 · time: 32 vs 17 vs 15 min · 20-turn session: Opus 89.4% ($43.37, 112 min) vs Carbon 79.4% ($21, 173 min)
- **Compared with:** Opus 5.5, Fable 5.2. Keep Claude Opus 5.5 as the default for long agentic coding.
- **Prompt:** not published here. We do not reconstruct unpublished prompts.
- **Note:** Company blog; the byline is unclear.

To run Carbon yourself: [how to use Gemini 4 Carbon](https://apimodels.app/how-to-use-gemini-4-carbon) covers where it works, the settings that matter and what it costs.

## 中文

**生产服务长会话编码评测**

作者:Bito · [原文](https://bito.ai/blog/gemini-4-carbon-vs-claude-opus-5-5-fable-5-2-coding/) · 2026-11-11 · [在 apimodels.app 案例库查看](https://apimodels.app/zh/gemini-4-carbon-prompts/code)

- **作品:** 在生产服务上跑长时间的智能体编码会话：Claude 模型在 Claude Code 里用 medium 档，Carbon 走 Google AI Studio 默认思考档，由评审模型按固定答案打分。Carbon 总分最低、耗时最长，但每个会话花费最少。
- **发布在:** 博客
- **工具:** Google AI Studio
- **作者公布的数字:** overall: Opus 85.0%, Fable 83.1%, Carbon 79.5% · one-shot: Carbon 89.1% (Fable 89.4%) · cost per long session: Carbon $2.75, Opus $5.42, Fable $8.13 · time: 32 vs 17 vs 15 min · 20-turn session: Opus 89.4% ($43.37, 112 min) vs Carbon 79.4% ($21, 173 min)
- **对比对象:** Opus 5.5、Fable 5.2。长时间智能体编码仍以 Claude Opus 5.5 为默认选择。
- **提示词:** 这里没有公开。我们不替作者补写没公开的提示词。
- **备注:** 公司博客，作者署名不明确。

自己用 Carbon:[Gemini 4 Carbon 怎么用](https://apimodels.app/zh/how-to-use-gemini-4-carbon)讲了哪里能用、哪些参数要改、要花多少钱。

---

← [Six merged production fixes replayed 20 times: Carbon vs Argon](208-six-merged-production-fixes-replayed-20-times-carbon-vs.md) · [All 223 cases](../../README.md) · [Strands SDK integration tests run against gemini-4-carbon](210-strands-sdk-integration-tests-run-against-gemini-4-carbon.md) →

Collected by [apimodels.app](https://apimodels.app), the API platform that maintains this repository. The work belongs to its creator; our write-up is [CC BY 4.0](../../LICENSE). Call Gemini 4 Carbon through apimodels.app: [model page](https://apimodels.app/models/gemini-4-carbon).
