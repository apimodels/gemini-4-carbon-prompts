# Six merged production fixes replayed 20 times: Carbon vs Argon

Gemini 4 Carbon case 208 of 223 · Apps, Real Codebases and Tooling · [简体中文](#中文)

By paddo.dev · [original post](https://paddo.dev/blog/gemini-4-carbon) · 2026-11-11 · [see it in the apimodels.app gallery](https://apimodels.app/gemini-4-carbon-prompts/code)

- **What it is:** Six merged changes from a production monorepo were replayed on clean snapshots in the Antigravity CLI at medium effort and graded by the tests shipped with each fix. Carbon and Argon came out effectively tied, with Carbon using more output tokens.
- **Where:** blog
- **Tool:** Antigravity CLI
- **Numbers the author reported:** runs passing every test: Carbon 17/20 vs Argon 16/20 · new tests fixed: 96% vs 98% · Carbon about 30 min per fix (max 46) · output tokens 1.82M vs 1.37M · list cost $60.38 vs $57.68 · 4 parallel sessions on a $99.99 Google AI Ultra plan · Ultra quota stopped all four sessions after about 2 hours (13 runs finished, 4 died mid-fix)
- **Compared with:** Argon. Effectively a tie; in the author's words, Carbon is Argon allowed to spend more.
- **Prompt:** not published here. We do not reconstruct unpublished prompts.
- **Note:** The author is not named on the page. Earlier Argon runs used Claude Code through a third-party API.

To run Carbon yourself: [how to use Gemini 4 Carbon](https://apimodels.app/how-to-use-gemini-4-carbon) covers where it works, the settings that matter and what it costs.

## 中文

**6 个线上修复重放 20 次**

作者:paddo.dev · [原文](https://paddo.dev/blog/gemini-4-carbon) · 2026-11-11 · [在 apimodels.app 案例库查看](https://apimodels.app/zh/gemini-4-carbon-prompts/code)

- **作品:** 把生产 monorepo 里 6 个已合并的修改放到干净快照上重放，在 Antigravity CLI 里用 medium 档跑，用每个修复自带的测试打分。Carbon 和 Argon 基本打平，Carbon 输出的 token 更多。
- **发布在:** 博客
- **工具:** Antigravity CLI
- **作者公布的数字:** runs passing every test: Carbon 17/20 vs Argon 16/20 · new tests fixed: 96% vs 98% · Carbon about 30 min per fix (max 46) · output tokens 1.82M vs 1.37M · list cost $60.38 vs $57.68 · 4 parallel sessions on a $99.99 Google AI Ultra plan · Ultra quota stopped all four sessions after about 2 hours (13 runs finished, 4 died mid-fix)
- **对比对象:** Argon。基本打平；按作者的说法，Carbon 就是花得更多的 Argon。
- **提示词:** 这里没有公开。我们不替作者补写没公开的提示词。
- **备注:** 页面上没有署名作者。早先的 Argon 测试是通过第三方 API 在 Claude Code 里跑的。

自己用 Carbon:[Gemini 4 Carbon 怎么用](https://apimodels.app/zh/how-to-use-gemini-4-carbon)讲了哪里能用、哪些参数要改、要花多少钱。

---

← [Patching an abandoned fishing game's binary for diamond fish](207-patching-an-abandoned-fishing-game-s-binary-for-diamond-fish.md) · [All 223 cases](../../README.md) · [Long agentic coding sessions: Carbon vs Opus 5.5 vs Fable 5.2](209-long-agentic-coding-sessions-carbon-vs-opus-5-5-vs-fable-5-2.md) →

Collected by [apimodels.app](https://apimodels.app), the API platform that maintains this repository. The work belongs to its creator; our write-up is [CC BY 4.0](../../LICENSE). Call Gemini 4 Carbon through apimodels.app: [model page](https://apimodels.app/models/gemini-4-carbon).
