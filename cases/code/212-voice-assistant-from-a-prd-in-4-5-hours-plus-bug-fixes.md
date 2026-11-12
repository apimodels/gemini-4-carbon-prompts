# Voice assistant from a PRD in 4.5 hours, plus bug fixes

Gemini 4 Carbon case 212 of 223 · Apps, Real Codebases and Tooling · [简体中文](#中文)

By codeSTACKr · [original YouTube page](https://www.youtube.com/watch?v=4onc5T6VHSM) · 2026-11-10 · [see it in the apimodels.app gallery](https://apimodels.app/gemini-4-carbon-prompts/code)

- **What it is:** From a PRD, Carbon spent about 4.5 hours building a "Jarvis" voice assistant that clicks, types and fills forms on LiveKit Inference, testing it without a mic by generating speech and fixing the vision model's click offset itself. Carbon, Argon and Opus then fixed two real LiveKit Agents bugs and security-reviewed the homepage voice agent.
- **Where:** YouTube
- **Numbers the author reported:** about 4.5 h build with no questions asked · security review real issues: Carbon 6, Argon 6, Opus 5, none invented
- **Compared with:** Argon, Opus 5.5. Opus was faster on both bug fixes; Carbon's top security finding was a framework bug the others missed, though it overrated severity.
- **Prompt:** not published here. We do not reconstruct unpublished prompts.
- **Note:** Made with LiveKit. A judge LLM checked the security findings; the framework bug Carbon found was reported and fixed.

To run Carbon yourself: [how to use Gemini 4 Carbon](https://apimodels.app/how-to-use-gemini-4-carbon) covers where it works, the settings that matter and what it costs.

## 中文

**4.5 小时按 PRD 做语音助手**

作者:codeSTACKr · [原页面(YouTube)](https://www.youtube.com/watch?v=4onc5T6VHSM) · 2026-11-10 · [在 apimodels.app 案例库查看](https://apimodels.app/zh/gemini-4-carbon-prompts/code)

- **作品:** Carbon 按一份 PRD 用约 4.5 小时做出能点击、打字、填表的「Jarvis」语音助手（跑在 LiveKit Inference 上），没有麦克风就自己生成语音来测，还自行修好了视觉模型的点击偏移。之后 Carbon、Argon 和 Opus 各自修复两个真实的 LiveKit Agents bug，并对官网首页的语音代理做安全审查。
- **发布在:** YouTube
- **作者公布的数字:** about 4.5 h build with no questions asked · security review real issues: Carbon 6, Argon 6, Opus 5, none invented
- **对比对象:** Argon、Opus 5.5。两个 bug 都是 Opus 修得更快；Carbon 安全审查的头号发现是其他模型都漏掉的框架 bug，但它高估了严重程度。
- **提示词:** 这里没有公开。我们不替作者补写没公开的提示词。
- **备注:** 与 LiveKit 合作制作。安全审查结果由评审 LLM 核对，Carbon 找到的框架 bug 已上报并修复。

自己用 Carbon:[Gemini 4 Carbon 怎么用](https://apimodels.app/zh/how-to-use-gemini-4-carbon)讲了哪里能用、哪些参数要改、要花多少钱。

---

← [MCP connector for Carbon design reviews from inside Codex](211-mcp-connector-for-carbon-design-reviews-from-inside-codex.md) · [All 223 cases](../../README.md) · [Agent teams find new exact solutions for fusion equations](../research/213-agent-teams-find-new-exact-solutions-for-fusion-equations.md) →

Collected by [apimodels.app](https://apimodels.app), the API platform that maintains this repository. The work belongs to its creator; our write-up is [CC BY 4.0](../../LICENSE). Call Gemini 4 Carbon through apimodels.app: [model page](https://apimodels.app/models/gemini-4-carbon).
