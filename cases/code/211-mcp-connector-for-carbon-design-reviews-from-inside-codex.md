# MCP connector for Carbon design reviews from inside Codex

Gemini 4 Carbon case 211 of 223 · Apps, Real Codebases and Tooling · [简体中文](#中文)

By wpv-chan · [original GitHub page](https://github.com/wpv-chan/codex-antigravity-acp) · 2026-11-11 · [see it in the apimodels.app gallery](https://apimodels.app/gemini-4-carbon-prompts/code)

- **What it is:** An MCP connector that lets Codex ask Gemini 4 Carbon High for design reviews via Codex -> stdio MCP -> `agy acp` -> Antigravity, checking each session is `gemini-4-carbon` at `thought_level=high` before asking. Tested on Windows with Antigravity CLI 1.5.5.
- **Where:** GitHub
- **Tool:** Codex -> stdio MCP -> `agy acp` -> Antigravity
- **Numbers the author reported:** Antigravity CLI 1.5.5
- **Prompt:** not published here. We do not reconstruct unpublished prompts.
- **Note:** The author warns that using a personal Antigravity subscription this way may break Antigravity's terms.

To run Carbon yourself: [how to use Gemini 4 Carbon](https://apimodels.app/how-to-use-gemini-4-carbon) covers where it works, the settings that matter and what it costs.

## 中文

**在 Codex 里调用 Carbon 做设计评审**

作者:wpv-chan · [原页面(GitHub)](https://github.com/wpv-chan/codex-antigravity-acp) · 2026-11-11 · [在 apimodels.app 案例库查看](https://apimodels.app/zh/gemini-4-carbon-prompts/code)

- **作品:** 一个让 Codex 向 Gemini 4 Carbon High 请求设计评审的 MCP 连接器，链路为 Codex -> stdio MCP -> `agy acp` -> Antigravity，每次提问前先确认会话是 `thought_level=high` 的 `gemini-4-carbon`。在 Windows 上用 Antigravity CLI 1.5.5 测试过。
- **发布在:** GitHub
- **工具:** Codex -> stdio MCP -> `agy acp` -> Antigravity
- **作者公布的数字:** Antigravity CLI 1.5.5
- **提示词:** 这里没有公开。我们不替作者补写没公开的提示词。
- **备注:** 作者提醒，这样使用个人 Antigravity 订阅可能违反 Antigravity 的服务条款。

自己用 Carbon:[Gemini 4 Carbon 怎么用](https://apimodels.app/zh/how-to-use-gemini-4-carbon)讲了哪里能用、哪些参数要改、要花多少钱。

---

← [Strands SDK integration tests run against gemini-4-carbon](210-strands-sdk-integration-tests-run-against-gemini-4-carbon.md) · [All 223 cases](../../README.md) · [Voice assistant from a PRD in 4.5 hours, plus bug fixes](212-voice-assistant-from-a-prd-in-4-5-hours-plus-bug-fixes.md) →

Collected by [apimodels.app](https://apimodels.app), the API platform that maintains this repository. The work belongs to its creator; our write-up is [CC BY 4.0](../../LICENSE). Call Gemini 4 Carbon through apimodels.app: [model page](https://apimodels.app/models/gemini-4-carbon).
