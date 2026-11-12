# Gemini 4 Carbon 提示词与案例:223 个真实案例

[English](README.md) · 简体中文

Gemini 4 Carbon 发布头几周,大家用它做出、测出、比出来的 223 个案例:用代码做的 3D 场景、游戏、模拟、影片和音乐,真实代码库里的修 bug 和科研,还有几十场和 Claude Fable 5.2、Gemini 4 Argon 等模型的同题对比。每个都署名原作者、链回原帖;作者公开了提示词的一并收录。

说明:这个合集由 [apimodels.app](https://apimodels.app) 整理,我在这个 API 平台工作。apimodels.app 是多模型 API 聚合平台:一个 key,用 Anthropic、OpenAI 兼容接口和原生 Gemini 格式调用 Gemini 4 Carbon 和另外 150 多个图像、视频、音频、语言模型。[cases/](cases) 里都是别人的作品,由我们整理介绍。能直接播放视频的版本在 [apimodels.app 的 Gemini 4 Carbon 案例库](https://apimodels.app/zh/gemini-4-carbon-prompts)。

## 一段话说清楚

Gemini 4 Carbon(模型 ID `gemini-4-carbon`)是 Gemini 4 里推理更深的一档。谷歌说它基于 Gemini 4 Argon,区别在每轮花更多思考 token;2026 年 10 月 28 日先开放给经过审核的网络安全防御方,11 月 10 日向所有付费 Gemini API 开发者开放。它能读文字、图片、视频、音频和 PDF,上下文 1,048,576 token,输出文字,默认最多 65,536 token。和其他语言模型一样,它自己不出像素也不出声音:下面的场景、游戏和影片都是它写的代码(Three.js、WebGL、Blender Python、CUDA C++、Web Audio),大多由 agent 去跑,最常见的是谷歌的 Antigravity。这 223 个案例发布于 2026-10-21 到 2026-11-12,早期的来自 Arena 测试和抢先体验。其中 18 个附了作者公开的提示词,33 个只有作者的需求或转述,172 个没有提示词;没公开的我们一律不补写。在 apimodels.app 上,Carbon 11 月 30 日前每百万输入 token $1.10、输出 $5.50,12 月 1 日起 $2.20 / $11;谷歌官方价是 $2 / $10 和 $4 / $20。

## 目录

- [同题对比实测](#同题对比实测)(96 个)
- [3D 场景、Blender 与原生代码](#3d-场景blender-与原生代码)(39 个)
- [可玩的游戏](#可玩的游戏)(20 个)
- [仿真、科学与工程](#仿真科学与工程)(7 个)
- [用代码做影片、MV 与音乐](#用代码做影片mv-与音乐)(22 个)
- [SVG、绘画与 2D 动画](#svg绘画与-2d-动画)(16 个)
- [应用、真实代码库与工具](#应用真实代码库与工具)(12 个)
- [智能体、科研与写作](#智能体科研与写作)(11 个)
- [先看这 10 个:X 上浏览最多](#先看这-10-个x-上浏览最多)
- [管用的提示词有什么共同点](#管用的提示词有什么共同点)
- [同题对比里 Carbon 表现如何](#同题对比里-carbon-表现如何)
- [自己跑一个](#自己跑一个)
- [常见问题](#常见问题)
- [署名、版权与许可](#署名版权与许可)

每个案例在 [cases/](cases) 下有单独一页:作者、原帖、做了什么、用什么工具、作者公布的数字,公开了的附提示词。X 的浏览和点赞截至 2026-11-12。全部数据另有一份 [data/cases.json](data/cases.json)。

## 先看这 10 个:X 上浏览最多

1. [智能体集群为核聚变方程找到新精确解](cases/research/213-agent-teams-find-new-exact-solutions-for-fusion-equations.md#中文),@lucasjvds,约 24.8 万 浏览
2. [飞机剖面：Carbon 对 Opus 5.5](cases/head-to-head/001-airplane-cutaway-in-3d-carbon-vs-opus-5-5.md#中文),@Mr_Salio,约 19.8 万 浏览
3. [iPhone 跑起 Windows 11 桌面](cases/code/201-windows-11-running-locally-on-a-foldable-iphone.md#中文),@ammaar,约 11.5 万 浏览
4. [Chrome 小恐龙四模型重制对比](cases/head-to-head/007-chrome-dino-remake-across-carbon-opus-astra-and-terra.md#中文),@noclipepe,约 11.3 万 浏览
5. [CUDA 和 C++ 手写的 5.2 万根草甸](cases/3d/105-grass-meadow-with-52k-blades-in-cuda-and-c.md#中文),@GlitterPixely,约 10.9 万 浏览
6. [三款 Gemini 4 的体素王国对比](cases/head-to-head/004-voxel-castle-kingdom-across-krypton-carbon-and-argon.md#中文),@lyraxana,约 10.2 万 浏览
7. [可切、可钉、可烧的彩虹果冻](cases/head-to-head/003-rainbow-jelly-you-can-cut-nail-and-torch.md#中文),@0xRhinoX,约 9.5 万 浏览
8. [9 缸星型发动机动态剖面](cases/head-to-head/009-animated-cutaway-of-a-nine-cylinder-radial-engine.md#中文),@olezhavich,约 8.8 万 浏览
9. [会眨眼对焦、再炸开成零件的机械眼](cases/3d/101-robotic-eye-that-blinks-focuses-then-explodes-into-parts.md#中文),@noclipepe,约 8.5 万 浏览
10. [自写 CUDA 引擎渲染的海底鱼群](cases/3d/099-underwater-scene-from-a-cuda-c-vfx-engine-carbon-wrote.md#中文),@fofrAI,约 7.1 万 浏览

## 管用的提示词有什么共同点

- **写需求说明,别许愿。**只给一句模糊需求的,结果大多一般。做了 15 个项目的亚里说得很直接:别对它许愿。出彩的作品,提示词都写明了技术栈、交付物和做完的标准;有位作者为一部 3 分钟的小提琴音乐会影片写了约 1 万字的规格说明。
- **给它看参考。**Carbon 能看视频。有人把 Claude Fable 5.2 做的射击游戏的实机视频交给它,要求做一个一样或更好的;也有人把 Anthropic 官方的 Fable 5.2 演示视频给它,让它复刻成网页。
- **让它看自己的成果。**那个射击游戏复刻用无头 Chrome 截图自检,自己抓出并修掉 3 个问题,48 分钟花了 $3.82。另一位作者让 Carbon 像视效总监一样审自己的截图,4 轮共约 2 小时、$7.40,把一堆体素方块变成了像样的恐龙。
- **说清楚交付格式。**5,000 架无人机灯光秀那条提示词,后半句就是「One HTML file. No external assets.」。Simon Willison 也是追加了一句「build that into a standalone HTML file」,才拿到能单独打开的网页。
- **大活拆给多个 agent。**最大的几个作品用了 Antigravity 的多 agent /swarm 模式:一个小景搭建游戏 9 个 agent、22,910 行代码,用了 1 小时 41 分钟;一个开放世界游戏做了 5 轮 agent 互评。
- **要追问。**有位作者贴出同一座岛和城堡在第一轮和追问三轮之后的样子:火从 9 个橙色方块变得几乎以假乱真。按作者的说法,差距来自追问。
- **核对它说做完了的东西。**一次 6 个应用的测试里,Carbon 每一次的收尾总结都至少有一个功能其实是坏的或被夸大了。让它先在浏览器里把成果点一遍再汇报。

## 同题对比里 Carbon 表现如何

合集里有 96 个同题对比,对手主要是 Claude Fable 5.2 和 Gemini 4 Argon。对 **Fable 5.2**,作者们通常觉得 Fable 的画面、动画和完成度更好,而 Carbon 的花费只是零头:一次测试三件活 $7.54 对 $41.71(Carbon 还赢了其中两件),另一次三个长构建 $27.68 对 $883.30,一个 6 个应用的评测里则是 Fable 以 70% 对 53.3% 胜出。对 **Gemini 4 Argon**,Carbon 通常更好,但更慢、写得更多:一次 Blender 测试里 Carbon 用了 81 分钟、18.6 万输出 token,Argon 14 分钟、1.1 万 token,而 Argon 那次没做成。这些都是不同的人在不同工具里各跑一次,当一线实测参考。完整数字在各案例页里,我们的对比页把它们和跑分放在一起:[Gemini 4 Carbon 和 Argon 怎么选](https://apimodels.app/zh/gemini-4-carbon-vs-argon)、[Claude Fable 5.2 和 Gemini 4 Carbon 怎么选](https://apimodels.app/zh/claude-fable-5-2-vs-gemini-4-carbon)。

## 同题对比实测

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/head-to-head](https://apimodels.app/zh/gemini-4-carbon-prompts/head-to-head)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 1 | [飞机剖面：Carbon 对 Opus 5.5](cases/head-to-head/001-airplane-cutaway-in-3d-carbon-vs-opus-5-5.md#中文) | [@Mr_Salio](https://x.com/Mr_Salio) | 未公开 | X,19.8 万 浏览 |
| 2 | [奔跑长颈鹿：Opus 5.5 对 Carbon](cases/head-to-head/002-low-poly-running-giraffe-opus-5-5-vs-carbon.md#中文) | [@Haleeeemahh](https://x.com/Haleeeemahh) | 未公开 | X,6.4 万 浏览 |
| 3 | [可切、可钉、可烧的彩虹果冻](cases/head-to-head/003-rainbow-jelly-you-can-cut-nail-and-torch.md#中文) | [@0xRhinoX](https://x.com/0xRhinoX) | 只有需求 | X,9.5 万 浏览 |
| 4 | [三款 Gemini 4 的体素王国对比](cases/head-to-head/004-voxel-castle-kingdom-across-krypton-carbon-and-argon.md#中文) | [@lyraxana](https://x.com/lyraxana) | 未公开 | X,10.2 万 浏览 |
| 5 | [剪同一段路演视频：Fable 对 Carbon](cases/head-to-head/005-editing-a-founders-pitch-clip-fable-5-2-vs-carbon.md#中文) | [@motion_so](https://x.com/motion_so) | 未公开 | X,4.9 万 浏览 |
| 6 | [公路骑行动画：Carbon 对 Argon](cases/head-to-head/006-animated-road-cyclist-carbon-vs-argon-vs-gpt-6-astra.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,6.6 万 浏览 |
| 7 | [Chrome 小恐龙四模型重制对比](cases/head-to-head/007-chrome-dino-remake-across-carbon-opus-astra-and-terra.md#中文) | [@noclipepe](https://x.com/noclipepe) | 未公开 | X,11.3 万 浏览 |
| 8 | [果冻版 DVD 屏保对比](cases/head-to-head/008-jelly-dvd-screensaver-where-opus-swapped-in-the-claude-logo.md#中文) | [@0xRhinoX](https://x.com/0xRhinoX) | 只有需求 | X,2.6 万 浏览 |
| 9 | [9 缸星型发动机动态剖面](cases/head-to-head/009-animated-cutaway-of-a-nine-cylinder-radial-engine.md#中文) | [@olezhavich](https://x.com/olezhavich) | 只有需求 | X,8.8 万 浏览 |
| 10 | [工具码头上的 9 个小捣蛋](cases/head-to-head/010-nine-tiny-troublemakers-on-a-dock-full-of-tools.md#中文) | [@0xPorterio](https://x.com/0xPorterio) | 只有需求 | X,4.2 万 浏览 |
| 11 | [骑行动画：Fable 5.5 略胜 Carbon](cases/head-to-head/011-animated-road-cyclist-fable-5-5-vs-carbon-in-arena.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,2.7 万 浏览 |
| 12 | [火柴人打架：DeepSeek 对 Carbon](cases/head-to-head/012-stickman-fight-animation-deepseek-v4-1-flash-vs-carbon.md#中文) | [@leo114119](https://x.com/leo114119) | 未公开 | X,4.7 万 浏览 |
| 13 | [夜城 SUV 三方对比，含 Fable 5.2](cases/head-to-head/013-night-city-suv-scene-fable-5-2-vs-carbon-vs-argon.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,2.1 万 浏览 |
| 14 | [照电影片段重建体素格鲁躲火箭](cases/head-to-head/014-voxel-gru-dodging-rockets-rebuilt-from-a-movie-clip.md#中文) | [@atomic_chat_hq](https://x.com/atomic_chat_hq) | 未公开 | X,3.4 万 浏览 |
| 15 | [用 Three.js 建白宫的同题对比](cases/head-to-head/015-u-s-white-house-in-three-js-carbon-vs-opus-5-5.md#中文) | [@exploraX_](https://x.com/exploraX_) | 未公开 | X,2.1 万 浏览 |
| 16 | [鹈鹕骑车：Carbon 对 Fable 5.5](cases/head-to-head/016-pelican-on-a-bicycle-carbon-vs-fable-5-5-in-testing.md#中文) | [@leo114119](https://x.com/leo114119) | 未公开 | X,5.4 万 浏览 |
| 17 | [火箭场景四模型对比](cases/head-to-head/017-rocket-scene-across-carbon-fable-5-2-opus-5-5-and-astra.md#中文) | [@Bhavani_00007](https://x.com/Bhavani_00007) | 未公开 | X,2.1 万 浏览 |
| 18 | [彩虹果冻再战 Fable 5.5](cases/head-to-head/018-rainbow-jelly-rematch-against-fable-5-5.md#中文) | [@0xRhinoX](https://x.com/0xRhinoX) | 只有需求 | X,2.8 万 浏览 |
| 19 | [海上帆船：Fable 5.2 对 Carbon](cases/head-to-head/019-sailing-ship-at-sea-fable-5-2-vs-carbon.md#中文) | [@Da7_Tech](https://x.com/Da7_Tech) | 未公开 | X,1.3 万 浏览 |
| 20 | [奔跑老虎：Carbon 对 Opus 5.5](cases/head-to-head/020-running-tiger-carbon-vs-opus-5-5-vs-argon-in-arena.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,1.2 万 浏览 |
| 21 | [浮空岛与吃草奶牛：Opus 对 Carbon](cases/head-to-head/021-floating-island-with-a-grazing-cow-opus-5-5-vs-carbon.md#中文) | [@Haleeeemahh](https://x.com/Haleeeemahh) | 未公开 | X,1.2 万 浏览 |
| 22 | [火柴人打架：Carbon 对 Fable 5.2](cases/head-to-head/022-stickman-fight-animation-carbon-vs-fable-5-2.md#中文) | [@DanielZambrini](https://x.com/DanielZambrini) | 未公开 | X,2.3 万 浏览 |
| 23 | [庄园割草：Fable 5.2 对 Carbon](cases/head-to-head/023-country-estate-mower-scene-fable-5-2-vs-carbon.md#中文) | [@_MaxBlade](https://x.com/_MaxBlade) | 未公开 | X,1.4 万 浏览 |
| 24 | [骑自行车的霸王龙四模型对比](cases/head-to-head/024-t-rex-riding-a-bike-across-four-models.md#中文) | [@olezhavich](https://x.com/olezhavich) | 未公开 | X,2.7 万 浏览 |
| 25 | [直列四缸发动机四模型对比](cases/head-to-head/025-working-inline-four-engine-across-four-models.md#中文) | [@kinderlayer](https://x.com/kinderlayer) | 只有需求 | X,1.5 万 浏览 |
| 26 | [Blender 鲨鱼场景三方对比](cases/head-to-head/026-blender-sisyphus-shark-scene-with-fable-5-2-added.md#中文) | [@HeathIsidr64707](https://x.com/HeathIsidr64707) | 未公开 | X,3 万 浏览 |
| 27 | [恐龙障碍跑四模型打分](cases/head-to-head/027-dinosaur-obstacle-run-scored-across-four-models.md#中文) | [@ridark_eth](https://x.com/ridark_eth) | 只有需求 | X,1.1 万 浏览 |
| 28 | [体素浮空王国：Opus 5.5 对 Carbon](cases/head-to-head/028-voxel-floating-kingdom-opus-5-5-vs-carbon.md#中文) | [@marcthecreatorr](https://x.com/marcthecreatorr) | 只有需求 | X,6,033 浏览 |
| 29 | [奔跑的狐狸：正式版对 Arena 版](cases/head-to-head/029-running-fox-released-carbon-vs-its-arena-checkpoint.md#中文) | [@srikanthvaluri](https://x.com/srikanthvaluri) | 只有需求 | X,7,251 浏览 |
| 30 | [奔跑老虎：Carbon 对 Hydrogen](cases/head-to-head/030-running-tiger-carbon-vs-gemini-4-hydrogen-in-arena.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,5,563 浏览 |
| 31 | [能雕刻、能点亮的彩虹果冻南瓜](cases/head-to-head/031-rainbow-jelly-pumpkin-you-can-carve-and-light.md#中文) | [@0xRhinoX](https://x.com/0xRhinoX) | 只有需求 | X,6,582 浏览 |
| 32 | [用笔现场画夕阳城市和老爷车](cases/head-to-head/032-sunset-city-and-muscle-car-drawn-live-with-a-pen.md#中文) | [@olezhavich](https://x.com/olezhavich) | 只有需求 | X,2.3 万 浏览 |
| 33 | [热带海岛射击游戏同题对比](cases/head-to-head/033-tropical-island-first-person-shooter-fable-5-2-vs-carbon.md#中文) | [@ValencianaAbel](https://x.com/ValencianaAbel) | 只有需求 | X,1 万 浏览 |
| 34 | [果冻钉子游戏对 Fable 5.5](cases/head-to-head/034-jelly-and-nails-game-fable-5-5-vs-carbon.md#中文) | [@0xRhinoX](https://x.com/0xRhinoX) | 未公开 | X,2.3 万 浏览 |
| 35 | [奔跑斑马四模型对比](cases/head-to-head/035-running-zebra-across-carbon-fable-5-5-opus-5-5-and-argon.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,8,951 浏览 |
| 36 | [八只触手同时做早餐的章鱼 SVG](cases/head-to-head/036-animated-svg-octopus-cooking-breakfast-with-eight-tentacles.md#中文) | [@olezhavich](https://x.com/olezhavich) | 只有需求 | X,8,711 浏览 |
| 37 | [可透视、剖切、爆炸的 V8 发动机](cases/head-to-head/037-running-v8-you-can-x-ray-cut-and-explode.md#中文) | [@dromexa](https://x.com/dromexa) | 只有需求 | X,3,257 浏览 |
| 38 | [90 年代街机格斗四模型对比](cases/head-to-head/038-90s-arcade-fighter-across-four-models.md#中文) | [@runable_hq](https://x.com/runable_hq) | 未公开 | X,1.4 万 浏览 |
| 39 | [老虎、雄鹰、跑车：Carbon 对 Argon](cases/head-to-head/039-tiger-eagle-and-sports-car-carbon-vs-argon-in-arena.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,3,345 浏览 |
| 40 | [未来水城：Fable 5.2 对 Carbon](cases/head-to-head/040-same-prompt-fable-5-2-at-18-vs-carbon-at-6-2.md#中文) | [@laopai1990](https://x.com/laopai1990) | 未公开 | X,1.7 万 浏览 |
| 41 | [可透视、剖切、爆炸的机械表](cases/head-to-head/041-mechanical-watch-you-can-x-ray-cut-and-explode.md#中文) | [@dromexa](https://x.com/dromexa) | 只有需求 | X,2,551 浏览 |
| 42 | [夕阳下的公牛：Carbon 对 Opus 5.5](cases/head-to-head/042-charging-bull-at-sunset-carbon-in-arena-vs-opus-5-5.md#中文) | [@jony_palino](https://x.com/jony_palino) | 未公开 | X,5,118 浏览 |
| 43 | [Blender 鲨鱼场景对 Opus 5.5](cases/head-to-head/043-sisyphus-shark-scene-in-blender-carbon-vs-opus-5-5.md#中文) | [@HeathIsidr64707](https://x.com/HeathIsidr64707) | 只有需求 | X,6,603 浏览 |
| 44 | [能透视爆炸、还能缝出一针的缝纫机](cases/head-to-head/044-sewing-machine-that-x-rays-explodes-and-makes-a-stitch.md#中文) | [@dromexa](https://x.com/dromexa) | 只有需求 | X,3,745 浏览 |
| 45 | [孔雀 SVG 动画同题对比](cases/head-to-head/045-animated-peacock-svg-fable-5-2-vs-carbon.md#中文) | [@SahilPanhotra](https://x.com/SahilPanhotra) | 未公开 | X,2,011 浏览 |
| 46 | [鲸鱼跃出水面：Carbon 对 Opus 5.5](cases/head-to-head/046-whale-breaching-scene-carbon-vs-opus-5-5.md#中文) | [@Bhavani_00007](https://x.com/Bhavani_00007) | 只有需求 | X,3,562 浏览 |
| 47 | [纯前端 3D 可乐动画：对 Fable 5.5](cases/head-to-head/047-3d-soda-animation-in-pure-front-end-code-fable-5-5-vs-carbon.md#中文) | [@leo114119](https://x.com/leo114119) | 未公开 | X,3,143 浏览 |
| 48 | [法师斗龙：Sonnet 5.5 对 Carbon](cases/head-to-head/048-mage-versus-dragon-game-sonnet-5-5-vs-carbon.md#中文) | [@IndependentEco](https://x.com/IndependentEco) | 未公开 | X,3,143 浏览 |
| 49 | [下颌杠杆力学图：Carbon 对 Fable](cases/head-to-head/049-jaw-lever-biomechanics-diagram-carbon-vs-fable-5-2.md#中文) | [@aiZttt__](https://x.com/aiZttt__) | 未公开 | X,6,667 浏览 |
| 50 | [废墟机器人：Carbon 对 Fable 5.2](cases/head-to-head/050-ruined-robot-animation-carbon-vs-fable-5-2.md#中文) | [@itsPaulAi](https://x.com/itsPaulAi) | 未公开 | X,1.1 万 浏览 |
| 51 | [三款 Gemini 4 的鹈鹕骑车对比](cases/head-to-head/051-pelican-on-a-bicycle-across-krypton-carbon-and-argon.md#中文) | [@srikanthvaluri](https://x.com/srikanthvaluri) | 未公开 | X,2,314 浏览 |
| 52 | [能变形成汽车的机器人：对 Fable 5.1](cases/head-to-head/052-robot-that-transforms-into-a-car-carbon-vs-fable-5-1.md#中文) | [@dromexa](https://x.com/dromexa) | 只有需求 | X,2,944 浏览 |
| 53 | [玄凤鹦鹉：Qwen 4-Max 对 Carbon](cases/head-to-head/053-cockatiel-on-a-branch-qwen-4-max-vs-carbon.md#中文) | [@DrstaOne](https://x.com/DrstaOne) | 未公开 | X,3,441 浏览 |
| 54 | [单文件雪花水晶球：对 Fable 5.2](cases/head-to-head/054-snow-globe-in-one-html-file-fable-5-2-vs-carbon.md#中文) | [@SahilPanhotra](https://x.com/SahilPanhotra) | 未公开 | X,1,821 浏览 |
| 55 | [上海外滩同题四模型对比](cases/head-to-head/055-shanghai-bund-scene-across-carbon-argon-fable-5-2-and-opus-5.md#中文) | [@NFT_Chen](https://x.com/NFT_Chen) | 未公开 | X,1.1 万 浏览 |
| 56 | [浮空岛奶牛：Fable 5.2 对 Carbon](cases/head-to-head/056-floating-island-with-a-cow-fable-5-2-vs-carbon.md#中文) | [@Haleeeemahh](https://x.com/Haleeeemahh) | 未公开 | X,2,199 浏览 |
| 57 | [CPU 与显卡讲解视频同题对比](cases/head-to-head/057-cpu-versus-graphics-card-explainer-video-fable-5-2-vs-carbon.md#中文) | [@getviewgum](https://x.com/getviewgum) | 未公开 | X,3,384 浏览 |
| 58 | [黑洞模拟：Carbon 对 Hydrogen](cases/head-to-head/058-black-hole-simulation-carbon-vs-gemini-4-hydrogen.md#中文) | [@leo114119](https://x.com/leo114119) | 未公开 | X,3,209 浏览 |
| 59 | [Three.js 宾利侧视图对 Opus 5.5](cases/head-to-head/059-bentley-side-view-in-three-js-carbon-vs-opus-5-5.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,1,177 浏览 |
| 60 | [自行车骑鹈鹕飞上天：对 Fable 5.5](cases/head-to-head/060-bicycle-riding-a-pelican-through-the-sky-carbon-vs-fable-5-5.md#中文) | [@Haleeeemahh](https://x.com/Haleeeemahh) | 未公开 | X,3,041 浏览 |
| 61 | [把 Fable 5.2 官方演示复刻成网页](cases/head-to-head/061-rebuilding-anthropic-s-fable-5-2-launch-demo-as-a-web-page.md#中文) | [@akokoi1](https://x.com/akokoi1) | 未公开 | X,4,822 浏览 |
| 62 | [电机发电机演示：对 Fable 5.2](cases/head-to-head/062-motor-and-generator-demo-carbon-vs-a-fable-5-2-run.md#中文) | [@akokoi1](https://x.com/akokoi1) | 未公开 | X,2,353 浏览 |
| 63 | [夜东京无人机收金币游戏三方对比](cases/head-to-head/063-night-tokyo-drone-coin-game-across-carbon-fable-and-opus.md#中文) | [@muku_sns](https://x.com/muku_sns) | 只有需求 | X,396 浏览 |
| 64 | [数字小花园：Fable 5.2 对 Carbon](cases/head-to-head/064-interactive-digital-garden-fable-5-2-vs-carbon.md#中文) | [@HIX_AI_](https://x.com/HIX_AI_) | 未公开 | X,366 浏览 |
| 65 | [景福宫模拟器同题对比](cases/head-to-head/065-gyeongbokgung-palace-simulator-fable-5-2-vs-carbon.md#中文) | [@msdkim](https://x.com/msdkim) | 未公开 | X,277 浏览 |
| 66 | [环球音乐之旅动画：Carbon 对 Fable](cases/head-to-head/066-world-music-tour-animated-video-carbon-vs-fable-5-2.md#中文) | [@Gorden_Sun](https://x.com/Gorden_Sun) | 未公开 | X,2,105 浏览 |
| 67 | [雨中拉面摊：三模型 Blender 对比](cases/head-to-head/067-ramen-stall-in-the-rain-in-blender-across-three-models.md#中文) | [@colerepo](https://x.com/colerepo) | 只有需求 | X,287 浏览 |
| 68 | [Antigravity 实测 15 个项目](cases/head-to-head/068-15-antigravity-projects-from-a-gta-style-game-to-an-ink-page.md#中文) | 亚里 Yari | 完整提示词 | YouTube |
| 69 | [四个模型三项高难任务对比](cases/head-to-head/069-three-hard-builds-with-full-cost-receipts-across-four-models.md#中文) | Pat Simmons (AI for Mortals) | 未公开 | YouTube |
| 70 | [KingBench 4 六项应用评测](cases/head-to-head/070-kingbench-4-six-app-builds-carbon-vs-fable-5-2.md#中文) | AICodeKing | 未公开 | YouTube |
| 71 | [五项构建与游戏对比](cases/head-to-head/071-five-builds-and-games-carbon-vs-fable-5-2.md#中文) | The Token Desk | 未公开 | YouTube |
| 72 | [霓虹赛车、夜市体素与频道片头](cases/head-to-head/072-neon-arcade-racer-night-market-voxel-diorama-and-channel.md#中文) | KostiKoNeuro | 节选 | GitHub |
| 73 | [恐怖游戏、电动车落地页与 3D 公寓](cases/head-to-head/073-horror-game-ev-landing-page-and-walkable-3d-loft.md#中文) | Kami | 未公开 | YouTube |
| 74 | [同样三项任务对比 Opus 5.5](cases/head-to-head/074-korean-learning-app-automation-dashboard-animated-explainer.md#中文) | Dan Buica / AI Automation | 未公开 | YouTube |
| 75 | [Antigravity CLI 六个项目实测](cases/head-to-head/075-six-projects-in-the-antigravity-cli-with-real-api-cost.md#中文) | Matheus Battisti - Hora de Codar | 未公开 | YouTube |
| 76 | [5 小时写实 Minecraft 类游戏](cases/head-to-head/076-ultra-realistic-minecraft-style-game-in-three-js-after-5.md#中文) | Vini Lana | 未公开 | YouTube |
| 77 | [Antigravity CLI 九项复杂任务](cases/head-to-head/077-nine-complex-builds-in-the-antigravity-cli-at-medium-effort.md#中文) | AI超元域 | 未公开 | YouTube |
| 78 | [对比 Argon 的四项实测](cases/head-to-head/078-carbon-vs-argon-novel-writing-front-end-code-svg-animated.md#中文) | 碳基生物退役指南 | 未公开 | YouTube |
| 79 | [Carbon 对 Argon 五维度评测](cases/head-to-head/079-carbon-vs-argon-across-five-dimensions-including-security.md#中文) | Piningillness | 未公开 | B 站 |
| 80 | [长句约束、射箭 SVG 与网页系统](cases/head-to-head/080-constrained-sentences-archery-svg-and-browser-os-ui-carbon.md#中文) | AI产品狙击手 | 未公开 | B 站 |
| 81 | [Bench V3 七项测试](cases/head-to-head/081-bench-v3-seven-tests-at-max-reasoning-through-a-third-party.md#中文) | Matt Johnston | 未公开 | YouTube |
| 82 | [复用 Fable 5.2 的五项测试](cases/head-to-head/082-same-five-tests-as-fable-5-2-plus-a-ship-simulator.md#中文) | Uğur Keşkekçi | 未公开 | YouTube |
| 83 | [同样三项任务对比 Fable 5.2](cases/head-to-head/083-duolingo-style-app-automation-plan-animated-explainer-carbon.md#中文) | Dan Buica / AI Automation | 未公开 | YouTube |
| 84 | [直播实测：工单、建模与界面](cases/head-to-head/084-live-vibe-check-notion-backlog-blender-room-rebuild-ui-suite.md#中文) | Every (Dan Shipper and team) | 未公开 | YouTube |
| 85 | [抢先体验：开放世界到古堡重建](cases/head-to-head/085-early-access-builds-open-world-sdf-dragon-fort-rebuilt-over.md#中文) | Prompt Engineering | 未公开 | YouTube |
| 86 | [两周抢先体验全方位实测](cases/head-to-head/086-two-weeks-of-early-access-across-games-apps-and-video.md#中文) | Paul J Lipsky | 未公开 | YouTube |
| 87 | [3D 金沙酒店与番茄钟 Mac 应用](cases/head-to-head/087-3d-marina-bay-sands-pomodoro-mac-app-bear-obsidian-mash-up.md#中文) | Sam Witteveen | 未公开 | YouTube |
| 88 | [网页系统、C++ 滑板游戏等实测](cases/head-to-head/088-browser-os-c-skate-game-subway-fps-and-3d-printing-tests.md#中文) | Bijan Bowen | 未公开 | YouTube |
| 89 | [一天五项：机场、缆车与金门大桥](cases/head-to-head/089-blender-airport-cable-car-game-golden-gate-build-and-lease.md#中文) | AI with Surya | 未公开 | YouTube |
| 90 | [Cursor 和 Droid 七项实测](cases/head-to-head/090-seven-tests-via-cursor-and-droid-including-a-mooncake-gift.md#中文) | NiceKate AI (kate人不错) | 未公开 | YouTube |
| 91 | [3D 海盗船与牛顿摆同题对比](cases/head-to-head/091-3d-pirate-ship-rube-goldberg-machine-and-newton-s-cradle.md#中文) | Ömer Göçmen | 未公开 | YouTube |
| 92 | [看视频提剪辑建议等多项实测](cases/head-to-head/092-video-feedback-3d-games-and-slides-via-the-api-and-cursor.md#中文) | まさおAIじっくり解説ch | 未公开 | YouTube |
| 93 | [反向动力学鹈鹕与 3D 代码演示](cases/head-to-head/093-pelican-svg-with-inverse-kinematics-and-other-code-native-3d.md#中文) | dotAI情报站 | 未公开 | B 站 |
| 94 | [六道固定题目一次性实测](cases/head-to-head/094-six-fixed-one-shot-prompts-through-a-third-party-api-from.md#中文) | hype or code | 完整提示词 | 网页 |
| 95 | [酒店网站、广告与阿波罗 11 号任务钟](cases/head-to-head/095-hotel-website-skillet-launch-ad-and-apollo-11-mission-clock.md#中文) | Runable | 未公开 | YouTube |
| 96 | [3D 地标、绘画世界与 UI 初评](cases/head-to-head/096-first-impressions-3d-landmarks-painting-worlds-visual.md#中文) | Arena | 未公开 | YouTube |

## 3D 场景、Blender 与原生代码

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/3d](https://apimodels.app/zh/gemini-4-carbon-prompts/3d)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 97 | [Three.js 机械花，还自己加了只蜜蜂](cases/3d/097-mechanical-flower-in-three-js-with-an-unprompted-bee.md#中文) | [@thtbee_](https://x.com/thtbee_) | 未公开 | X,5.9 万 浏览 |
| 98 | [看一段视频，用 Three.js 复刻出来](cases/3d/098-three-js-recreation-of-a-train-cab-video-clip.md#中文) | [@emollick](https://x.com/emollick) | 未公开 | X,6.1 万 浏览 |
| 99 | [自写 CUDA 引擎渲染的海底鱼群](cases/3d/099-underwater-scene-from-a-cuda-c-vfx-engine-carbon-wrote.md#中文) | [@fofrAI](https://x.com/fofrAI) | 未公开 | X,7.1 万 浏览 |
| 100 | [一个控件带动齿轮和花瓣的天象仪](cases/3d/100-orrery-where-one-control-drives-gears-and-petals.md#中文) | [@kimmonismus](https://x.com/kimmonismus) | 未公开 | X,5.3 万 浏览 |
| 101 | [会眨眼对焦、再炸开成零件的机械眼](cases/3d/101-robotic-eye-that-blinks-focuses-then-explodes-into-parts.md#中文) | [@noclipepe](https://x.com/noclipepe) | 只有需求 | X,8.5 万 浏览 |
| 102 | [纯 C++ 写的山谷场景，零复用素材](cases/3d/102-open-valley-scene-in-custom-c-with-no-reused-assets.md#中文) | [@Lentils80](https://x.com/Lentils80) | 未公开 | X,9,430 浏览 |
| 103 | [不用现成素材的 3D 篮球场](cases/3d/103-3d-basketball-court-built-without-premade-assets.md#中文) | [@LexnLin](https://x.com/LexnLin) | 未公开 | X,8,904 浏览 |
| 104 | [在 Blender 里雕刻并做动画的珠宝海马](cases/3d/104-jeweled-sea-creature-sculpted-and-animated-in-blender.md#中文) | [@Stefan_3D_AI](https://x.com/Stefan_3D_AI) | 未公开 | X,1.3 万 浏览 |
| 105 | [CUDA 和 C++ 手写的 5.2 万根草甸](cases/3d/105-grass-meadow-with-52k-blades-in-cuda-and-c.md#中文) | [@GlitterPixely](https://x.com/GlitterPixely) | 未公开 | X,10.9 万 浏览 |
| 106 | [岛屿城堡与龙：首轮 vs 追问三轮](cases/3d/106-island-castle-and-dragon-first-prompt-vs-three-follow-ups.md#中文) | [@semichenkko](https://x.com/semichenkko) | 未公开 | X,2.5 万 浏览 |
| 107 | [经典「三维马」提示词跑出的写实马](cases/3d/107-realistic-interactive-3d-horse-from-the-classic-horse-prompt.md#中文) | [@kasmiyouness1](https://x.com/kasmiyouness1) | 完整提示词 | X,5,033 浏览 |
| 108 | [多工具流水线做出的整缸水族箱](cases/3d/108-aquarium-with-angelfish-snail-and-shrimp-from-a-multi-tool.md#中文) | [@ai_for_success](https://x.com/ai_for_success) | 未公开 | X,4,332 浏览 |
| 109 | [有倒影和游鱼的锦鲤庭院](cases/3d/109-koi-courtyard-with-water-reflections-and-swimming-fish.md#中文) | [@SahilPanhotra](https://x.com/SahilPanhotra) | 未公开 | X,3,777 浏览 |
| 110 | [一个着色器画出的可乐瓶](cases/3d/110-coca-cola-bottle-drawn-entirely-in-one-shader.md#中文) | [@karanC_12](https://x.com/karanC_12) | 未公开 | X,3,927 浏览 |
| 111 | [Three.js 版 Minecraft 测试](cases/3d/111-minecraft-style-test-in-three-js-using-antigravity-voice.md#中文) | [@oviniciuslana](https://x.com/oviniciuslana) | 未公开 | X,2,376 浏览 |
| 112 | [单个 HTML 里的千万级体素城](cases/3d/112-11-3-million-voxels-at-60fps-in-one-html-file.md#中文) | [@Adidotdev](https://x.com/Adidotdev) | 未公开 | X,2,242 浏览 |
| 113 | [用旧平面图和照片重建考文垂大教堂](cases/3d/113-destroyed-coventry-cathedral-rebuilt-from-floorplans-and.md#中文) | [@LeslieNooteboom](https://x.com/LeslieNooteboom) | 未公开 | X,6,870 浏览 |
| 114 | [胸口装着机芯的程序化机械隼](cases/3d/114-procedural-mechanical-falcon-with-a-working-watch-movement.md#中文) | [@Adidotdev](https://x.com/Adidotdev) | 未公开 | X,1,386 浏览 |
| 115 | [超过 300 万体素的浮空王国](cases/3d/115-voxel-floating-kingdom-with-over-three-million-voxels.md#中文) | [@marcthecreatorr](https://x.com/marcthecreatorr) | 只有需求 | X,1,732 浏览 |
| 116 | [用老图纸和照片建出的埃菲尔铁塔](cases/3d/116-eiffel-tower-model-built-from-old-drawings-and-photos.md#中文) | [@cobley_ben](https://x.com/cobley_ben) | 未公开 | X,1,497 浏览 |
| 117 | [只用代码加 Blender 做的宇宙视频](cases/3d/117-space-video-made-with-code-and-blender.md#中文) | [@RJasonHA](https://x.com/RJasonHA) | 未公开 | X,2,475 浏览 |
| 118 | [有行星、银河和流星的小宇宙](cases/3d/118-little-universe-with-planets-milky-way-and-shooting-stars.md#中文) | [@doe_naps](https://x.com/doe_naps) | 未公开 | X,592 浏览 |
| 119 | [Blender 脚本里超跑追蒸汽火车](cases/3d/119-supercar-chasing-a-steam-train-scripted-in-blender.md#中文) | [@HeathIsidr64707](https://x.com/HeathIsidr64707) | 未公开 | X,2,122 浏览 |
| 120 | [扬克斯变身机甲踏遍纽约](cases/3d/120-yonkers-stands-up-as-a-giant-mech-over-new-york.md#中文) | [@simonw](https://x.com/simonw) | 完整提示词 | X,410 浏览 |
| 121 | [骑着金雕飞行的自行车手](cases/3d/121-cyclist-riding-a-golden-eagle-one-shot-in-three-js.md#中文) | [@AI_Screening](https://x.com/AI_Screening) | 未公开 | X,1,396 浏览 |
| 122 | [单个 HTML 文件里的纽约游船之旅](cases/3d/122-interactive-new-york-city-cruise-tour-in-one-html-file.md#中文) | [@StatsWire](https://x.com/StatsWire) | 未公开 | X,735 浏览 |
| 123 | [迭代 5 轮的 Three.js 冰岛黑沙滩](cases/3d/123-icelandic-black-sand-beach-in-three-js-over-five-rounds.md#中文) | [@RJasonHA](https://x.com/RJasonHA) | 未公开 | X,757 浏览 |
| 124 | [每级台阶都会发声的无尽弹珠塔](cases/3d/124-endless-marble-run-tower-where-every-step-plays-a-note.md#中文) | [@sunset_evm](https://x.com/sunset_evm) | 只有需求 | X,1,072 浏览 |
| 125 | [在 Antigravity 里建模的烧烤摊](cases/3d/125-barbecue-stall-modeled-in-antigravity.md#中文) | [@marcus_s_deng](https://x.com/marcus_s_deng) | 未公开 | X,1,860 浏览 |
| 126 | [Three.js 做的奔跑斑马](cases/3d/126-running-zebra-in-three-js.md#中文) | [@ai_funss](https://x.com/ai_funss) | 未公开 | X,1,652 浏览 |
| 127 | [Blender 里零下载素材的步枪组装与弹道](cases/3d/127-rifle-assembly-and-ballistics-scene-in-blender-with-no.md#中文) | [@vipinxtwt](https://x.com/vipinxtwt) | 未公开 | X,520 浏览 |
| 128 | [夜色水岸上的 5000 架无人机灯光秀](cases/3d/128-5-000-drone-light-show-over-a-night-waterfront.md#中文) | [@sunset_evm](https://x.com/sunset_evm) | 完整提示词 | X,906 浏览 |
| 129 | [Carbon 智能体群做的超跑](cases/3d/129-hypercar-built-by-a-swarm-of-carbon-agents.md#中文) | [@SimonasLTU1](https://x.com/SimonasLTU1) | 未公开 | X,781 浏览 |
| 130 | [Gemini 手机 App 里 9 分钟做的帆船](cases/3d/130-sailing-boat-scene-made-in-the-gemini-mobile-app.md#中文) | [@EdwinCh43136084](https://x.com/EdwinCh43136084) | 未公开 | X,545 浏览 |
| 131 | [纯 CUDA 光线追踪：雨落荷塘](cases/3d/131-pure-cuda-c-20-ray-tracer-raindrops-on-a-lotus-pond.md#中文) | Jian Zhang (GitHub opdaer, X @jianzhang1987) | 未公开 | GitHub |
| 132 | [181 件榫卯宋代亭子拆解动画](cases/3d/132-181-part-song-dynasty-mortise-and-tenon-pavilion-with.md#中文) | Jian Zhang (GitHub opdaer) | 未公开 | GitHub |
| 133 | [用 tscircuit 设计 PCB 电路板](cases/3d/133-pcb-design-in-tscircuit-fable-5-2-vs-carbon.md#中文) | Seve | 完整提示词 | YouTube |
| 134 | [参考图 3D 建模与连锁机关](cases/3d/134-reference-image-3d-modelling-and-a-rube-goldberg-machine-vs.md#中文) | EWIY | 未公开 | B 站 |
| 135 | [Blender 建模派蒙，跑了 6 小时](cases/3d/135-paimon-3d-model-in-blender-over-a-6-hour-run.md#中文) | 连接实验室 | 未公开 | B 站 |

## 可玩的游戏

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/games](https://apimodels.app/zh/gemini-4-carbon-prompts/games)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 136 | [四轮自我审片后的 Chrome 小恐龙](cases/games/136-chrome-dino-upgraded-by-four-rounds-of-self-review.md#中文) | [@noclipepe](https://x.com/noclipepe) | 未公开 | X,1.3 万 浏览 |
| 137 | [完全在 AI Studio 里做的治愈解谜游戏](cases/games/137-cozy-puzzle-game-built-entirely-in-ai-studio.md#中文) | [@chanelluuh](https://x.com/chanelluuh) | 未公开 | X,4.6 万 浏览 |
| 138 | [单文件 HTML 的 V12 超跑海岸赛车](cases/games/138-playable-v12-hypercar-coastal-racing-game-in-one-html-file.md#中文) | [@StatsWire](https://x.com/StatsWire) | 未公开 | X,1,871 浏览 |
| 139 | [无限海洋随机生成岛屿的水上飞机游戏](cases/games/139-seaplane-game-with-an-infinite-ocean-and-random-islands.md#中文) | [@RoundtableSpace](https://x.com/RoundtableSpace) | 未公开 | X,5.4 万 浏览 |
| 140 | [骑车鹈鹕漫游谷歌园区的开放世界游戏](cases/games/140-open-world-pelican-bike-game-across-google-s-campus.md#中文) | [@agenticjay](https://x.com/agenticjay) | 未公开 | X,1,249 浏览 |
| 141 | [能听声音玩的玻璃叠叠乐物理游戏](cases/games/141-glassy-jenga-physics-game-you-can-play-by-sound.md#中文) | [@AI_Andrew](https://x.com/AI_Andrew) | 未公开 | X,1.8 万 浏览 |
| 142 | [看实机视频复刻 Fable 做的射击游戏](cases/games/142-rebuilding-a-fable-made-shooter-from-its-gameplay-video.md#中文) | [@mylifcc](https://x.com/mylifcc) | 只有需求 | X,7,165 浏览 |
| 143 | [一句提示词做出的水上赛艇游戏](cases/games/143-boat-racing-game-from-a-single-prompt.md#中文) | [@athrix_codes](https://x.com/athrix_codes) | 未公开 | X,1,176 浏览 |
| 144 | [把鹈鹕骑自行车做成了游戏](cases/games/144-pelican-riding-a-bicycle-turned-into-a-game.md#中文) | [@xluchuan](https://x.com/xluchuan) | 未公开 | X,1,879 浏览 |
| 145 | [照着 Omni 视频复刻却做成了新游戏](cases/games/145-game-rebuild-from-an-omni-video-that-became-a-new-game.md#中文) | [@gigabit_million](https://x.com/gigabit_million) | 未公开 | X,779 浏览 |
| 146 | [Vertex AI 一次生成马里奥式箱庭](cases/games/146-one-shot-mario-style-3d-platformer-via-vertex-ai.md#中文) | [@Delroy715](https://x.com/Delroy715) | 未公开 | X,4,366 浏览 |
| 147 | [首测做出的完成度很高的赛车游戏](cases/games/147-simple-racing-game-from-a-first-test.md#中文) | [@bei351009016](https://x.com/bei351009016) | 未公开 | X,2,087 浏览 |
| 148 | [浏览器里的桌面迷你卡丁车游戏](cases/games/148-desk-racer-a-miniature-kart-game-in-the-browser.md#中文) | [@anuragdotdev](https://x.com/anuragdotdev) | 只有需求 | X,1,022 浏览 |
| 149 | [雨夜赛车：Carbon vs Fable 5.2](cases/games/149-nightshift-highway-racing-game-built-twice-carbon-vs-fable-5.md#中文) | Ediz Ege Mercan (GitHub EddizEge) | 未公开 | 博客 |
| 150 | [单个 HTML 文件的中世纪造景游戏](cases/games/150-cozy-medieval-diorama-builder-in-a-single-930-kb-html-file.md#中文) | FireTable | 完整提示词 | GitHub |
| 151 | [第一人称战斗法师游戏盲评](cases/games/151-first-person-battle-mage-game-judged-blind-fable-5-2-vs.md#中文) | Sound Human : Stop Slop | 完整提示词 | YouTube |
| 152 | [$7 封顶：餐桌上的 3D 卡丁车](cases/games/152-3d-kart-racer-on-a-giant-dinner-table-7-per-model.md#中文) | AI That Works | 只有需求 | YouTube |
| 153 | [一句话做出网页 FPS 游戏](cases/games/153-browser-playable-fps-game-from-a-one-sentence-prompt.md#中文) | SmartDeng_ | 未公开 | B 站 |
| 154 | [Antigravity 里重跑造桥比赛](cases/games/154-bridge-building-contest-re-run-with-gemini-models-in.md#中文) | tzt诶喂 | 未公开 | B 站 |
| 155 | [Fall Guys 风格派对游戏三方对比](cases/games/155-fall-guys-style-party-game-from-scratch-carbon-vs-argon-vs.md#中文) | GameAGI | 未公开 | YouTube |

## 仿真、科学与工程

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/simulations](https://apimodels.app/zh/gemini-4-carbon-prompts/simulations)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 156 | [有限元分析驱动 CAD 的闭环设计](cases/simulations/156-closed-loop-fea-to-cad-part-design.md#中文) | [@adamdotnew](https://x.com/adamdotnew) | 未公开 | X,1.7 万 浏览 |
| 157 | [一张参考图做出的 19 世纪巴黎物理实验室](cases/simulations/157-interactive-19th-century-parisian-physics-lab-from-one.md#中文) | [@thebuggeddev](https://x.com/thebuggeddev) | 未公开 | X,5.1 万 浏览 |
| 158 | [纯代码写的电影感黑洞模拟](cases/simulations/158-cinematic-3d-black-hole-simulation-in-pure-code.md#中文) | [@pankajkumar_dev](https://x.com/pankajkumar_dev) | 只有需求 | X,3,564 浏览 |
| 159 | [一句话做出的人形机器人 3D 仿真](cases/simulations/159-humanoid-robot-simulation-with-six-motion-modes.md#中文) | [@masahirochaen](https://x.com/masahirochaen) | 完整提示词 | X,1.1 万 浏览 |
| 160 | [High 档跑 3 小时的电机与发电机演示](cases/simulations/160-electric-motor-and-generator-demo-after-a-three-hour-run.md#中文) | [@akokoi1](https://x.com/akokoi1) | 未公开 | X,8,747 浏览 |
| 161 | [带第一视角和乘客上下车的地铁模拟器](cases/simulations/161-city-subway-simulator-with-pov-mode-and-passengers.md#中文) | [@jerrod_lew](https://x.com/jerrod_lew) | 未公开 | X,1,033 浏览 |
| 162 | [Carbon 做的元素周期表](cases/simulations/162-periodic-table-of-the-elements-made-with-carbon.md#中文) | [@mylifcc](https://x.com/mylifcc) | 未公开 | X,1,411 浏览 |

## 用代码做影片、MV 与音乐

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/film-music](https://apimodels.app/zh/gemini-4-carbon-prompts/film-music)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 163 | [完全用代码做出的整支 MV](cases/film-music/163-full-music-video-made-with-only-code.md#中文) | [@kickingkeys](https://x.com/kickingkeys) | 未公开 | X,1.2 万 浏览 |
| 164 | [一张参考图变成动画，纯 JS 加 Python](cases/film-music/164-animated-scene-from-one-reference-image-in-pure-js-and.md#中文) | [@devteamdrew](https://x.com/devteamdrew) | 未公开 | X,1.4 万 浏览 |
| 165 | [带立体声的 50 秒万圣节漫步动画](cases/film-music/165-fifty-second-halloween-walk-with-stereo-audio.md#中文) | [@abhinavflac](https://x.com/abhinavflac) | 未公开 | X,1.2 万 浏览 |
| 166 | [3 分钟无缝循环的小提琴独奏音乐会影片](cases/film-music/166-three-minute-looping-solo-violin-concert-film-from-a-long.md#中文) | [@IamEmily2050](https://x.com/IamEmily2050) | 节选 | X,5,050 浏览 |
| 167 | [用日常声音做音乐的原型](cases/film-music/167-music-prototype-built-from-everyday-sounds.md#中文) | [@alexanderchen](https://x.com/alexanderchen) | 未公开 | X,1.7 万 浏览 |
| 168 | [纯代码做出的一段短片](cases/film-music/168-short-film-made-with-plain-code.md#中文) | [@jony_palino](https://x.com/jony_palino) | 未公开 | X,4,501 浏览 |
| 169 | [Carbon 加云端 GPU 做的原创歌曲 MV](cases/film-music/169-original-song-and-music-video-with-carbon-and-a-cloud-gpu.md#中文) | [@shengtang135754](https://x.com/shengtang135754) | 未公开 | X,4,728 浏览 |
| 170 | [AI Studio 一句话生成的炫技 MV](cases/film-music/170-music-video-showing-off-carbon-from-a-one-line-prompt.md#中文) | [@itnavi2022](https://x.com/itnavi2022) | 完整提示词 | X,3,306 浏览 |
| 171 | [3 分钟钢琴独奏音乐会影片](cases/film-music/171-three-minute-solo-piano-concert-film-of-beethoven-s.md#中文) | [@IamEmily2050](https://x.com/IamEmily2050) | 只有需求 | X,3,010 浏览 |
| 172 | [一句话生成的 ETH 对比 BTC 视频](cases/film-music/172-eth-versus-btc-since-2015-video-rendered-in-c.md#中文) | [@losingle](https://x.com/losingle) | 完整提示词 | X,704 浏览 |
| 173 | [Carbon 总控制作的古装短片](cases/film-music/173-period-drama-short-film-with-carbon-directing-the-pipeline.md#中文) | [@shengtang135754](https://x.com/shengtang135754) | 未公开 | X,2,829 浏览 |
| 174 | [Blender 制作明日方舟玫兰莎 MV](cases/film-music/174-arknights-melantha-narrative-music-video-built-in-blender.md#中文) | xplunger1337 | 完整提示词 | B 站 |
| 175 | [Higgsfield 积分拍短片对决](cases/film-music/175-short-films-from-2-000-higgsfield-credits-fable-5-2-vs.md#中文) | Adam Campbell Cinema | 未公开 | YouTube |
| 176 | [30 秒恐龙涂鸦变 30 秒短片](cases/film-music/176-from-a-30-second-dinosaur-doodle-to-a-30-second-film.md#中文) | Forn AI | 未公开 | YouTube |
| 177 | [纯代码短片《刹那》](cases/film-music/177-pure-code-short-film-answering-a-fable-5-2-film.md#中文) | 花家颜 | 未公开 | B 站 |
| 178 | [火柴人武侠打斗动画](cases/film-music/178-stickman-wuxia-fight-animation-fable-5-2-vs-carbon.md#中文) | Vzerolin | 未公开 | B 站 |
| 179 | [Claude 娘舞蹈 MV](cases/film-music/179-dance-music-video-for-claude-chan-led-by-carbon.md#中文) | hero1157 | 未公开 | B 站 |
| 180 | [复刻 Fable 视频《雨后唐人街》](cases/film-music/180-recreating-a-fable-made-video-chinatown-after-the-rain.md#中文) | 法斯特咱有 | 未公开 | B 站 |
| 181 | [同提示词 3D 火箭发射动画盲测](cases/film-music/181-same-prompt-3d-rocket-launch-animation-judged-blind-by.md#中文) | 白色so | 未公开 | B 站 |
| 182 | [/swarm 创作：鹈鹕骑车 6,000 年](cases/film-music/182-swarm-art-piece-6-000-years-of-pelicans-riding-bicycles.md#中文) | orbitooo | 完整提示词 | B 站 |
| 183 | [扬克斯变身机甲踩遍纽约](cases/film-music/183-yonkers-stands-up-as-a-mech-and-stomps-around-nyc.md#中文) | Simon Willison (simonw) | 完整提示词 | 博客 |
| 184 | [一句话出视频，全工具开放](cases/film-music/184-one-sentence-video-in-antigravity-with-every-tool-enabled.md#中文) | LRN095 | 未公开 | B 站 |

## SVG、绘画与 2D 动画

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/svg-2d](https://apimodels.app/zh/gemini-4-carbon-prompts/svg-2d)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 185 | [照着照片一笔笔画肖像的绘画程序](cases/svg-2d/185-painting-app-that-paints-a-portrait-from-a-photo.md#中文) | [@CodeByPoonam](https://x.com/CodeByPoonam) | 未公开 | X,5.1 万 浏览 |
| 186 | [雨中女孩 SVG 加原创配乐的助眠循环](cases/svg-2d/186-rainy-night-svg-girl-with-an-original-music-loop.md#中文) | [@chetaslua](https://x.com/chetaslua) | 未公开 | X,3.3 万 浏览 |
| 187 | [「香蕉测试」：香蕉贡多拉插画](cases/svg-2d/187-banana-gondola-illustration-for-the-banana-test.md#中文) | [@AdamHoltererer](https://x.com/AdamHoltererer) | 未公开 | X,5,673 浏览 |
| 188 | [螃蟹逼近骑车鹈鹕的 SVG](cases/svg-2d/188-svg-of-crabs-closing-in-on-a-cycling-pelican.md#中文) | [@HarshithLucky3](https://x.com/HarshithLucky3) | 只有需求 | X,3,123 浏览 |
| 189 | [带背景音乐的程肖宇 SVG 画像](cases/svg-2d/189-svg-portrait-of-sung-jinwoo-with-background-music.md#中文) | [@notjazii](https://x.com/notjazii) | 只有需求 | X,1.3 万 浏览 |
| 190 | [奔跑的像素画骏马](cases/svg-2d/190-galloping-horse-in-pixel-art.md#中文) | [@AdamHoltererer](https://x.com/AdamHoltererer) | 未公开 | X,1,969 浏览 |
| 191 | [骑车杂耍穿越四季的狮子](cases/svg-2d/191-lion-juggling-on-a-bicycle-through-four-seasons.md#中文) | [@SahilPanhotra](https://x.com/SahilPanhotra) | 只有需求 | X,1,720 浏览 |
| 192 | [Gemini App 里的鹈鹕骑车测试](cases/svg-2d/192-pelican-on-a-bicycle-in-the-gemini-app.md#中文) | [@leo114119](https://x.com/leo114119) | 未公开 | X,1,956 浏览 |
| 193 | [边牧骑斑马骑自行车的 SVG 动画](cases/svg-2d/193-svg-of-a-border-collie-riding-a-zebra-riding-a-bicycle.md#中文) | [@xueyu1125](https://x.com/xueyu1125) | 完整提示词 | X,1,331 浏览 |
| 194 | [鹈鹕骑车动画，自动演示并导出 MP4](cases/svg-2d/194-pelican-animation-with-auto-click-demo-exported-to-mp4.md#中文) | [@xluchuan](https://x.com/xluchuan) | 未公开 | X,856 浏览 |
| 195 | [Gemini App 高档位的鹈鹕骑车](cases/svg-2d/195-detailed-pelican-on-a-bicycle-on-high-in-the-gemini-app.md#中文) | [@EdwinCh43136084](https://x.com/EdwinCh43136084) | 未公开 | X,2,207 浏览 |
| 196 | [经 DeepSeek 套壳反代后跑崩的鹈鹕](cases/svg-2d/196-broken-pelican-output-through-a-deepseek-harness-proxy.md#中文) | [@leo114119](https://x.com/leo114119) | 未公开 | X,697 浏览 |
| 197 | [复用 Opus 5.5 的鹈鹕提示词](cases/svg-2d/197-reusing-an-opus-5-5-6-000-years-of-pelicans-prompt-on-carbon.md#中文) | 羽升AI实践分享 | 未公开 | B 站 |
| 198 | [4 种环境的鹈鹕骑车对比站](cases/svg-2d/198-pelican-on-a-bicycle-comparison-site-across-four-harnesses.md#中文) | CrazyRock114 | 未公开 | GitHub |
| 199 | [鹈鹕测试：Fable 对 Carbon](cases/svg-2d/199-pelican-test-fable-5-2-max-vs-carbon.md#中文) | Lovely_Chuxue | 未公开 | B 站 |
| 200 | [鹈鹕骑马：GPT 灰度模型对 Carbon](cases/svg-2d/200-pelican-riding-a-horse-gpt-gray-test-model-vs-carbon-high.md#中文) | 不发光的偏方三八面体 | 未公开 | B 站 |

## 应用、真实代码库与工具

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/code](https://apimodels.app/zh/gemini-4-carbon-prompts/code)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 201 | [iPhone 跑起 Windows 11 桌面](cases/code/201-windows-11-running-locally-on-a-foldable-iphone.md#中文) | [@ammaar](https://x.com/ammaar) | 未公开 | X,11.5 万 浏览 |
| 202 | [给户型图生成器加新功能](cases/code/202-new-features-for-a-floor-plan-generator.md#中文) | [@chirovisuals](https://x.com/chirovisuals) | 未公开 | X,4,256 浏览 |
| 203 | [Unity 影绘视频的着色器修正与验收](cases/code/203-shader-fixes-and-qa-for-a-unity-shadow-play-video.md#中文) | [@ShadeLurk](https://x.com/ShadeLurk) | 未公开 | X,808 浏览 |
| 204 | [在真实业务代码上重跑 7 个 Issue](cases/code/204-rerunning-seven-real-business-code-issues.md#中文) | [@luoleiorg](https://x.com/luoleiorg) | 未公开 | X,1 万 浏览 |
| 205 | [失败案例：一行代码都没改](cases/code/205-antigravity-run-that-never-edited-a-line-of-code.md#中文) | weiyunjun | 未公开 | V2EX |
| 206 | [Factory 托管版缓存命中率 44%](cases/code/206-44-prompt-cache-hit-rate-for-factory-hosted-gemini-4-carbon.md#中文) | marovole | 未公开 | GitHub |
| 207 | [逆向修改停更的钓鱼游戏](cases/code/207-patching-an-abandoned-fishing-game-s-binary-for-diamond-fish.md#中文) | gbolcer | 未公开 | GitHub |
| 208 | [6 个线上修复重放 20 次](cases/code/208-six-merged-production-fixes-replayed-20-times-carbon-vs.md#中文) | paddo.dev | 未公开 | 博客 |
| 209 | [生产服务长会话编码评测](cases/code/209-long-agentic-coding-sessions-carbon-vs-opus-5-5-vs-fable-5-2.md#中文) | Bito | 未公开 | 博客 |
| 210 | [Strands SDK 集成测试实跑](cases/code/210-strands-sdk-integration-tests-run-against-gemini-4-carbon.md#中文) | strandly-the-agent | 未公开 | GitHub |
| 211 | [在 Codex 里调用 Carbon 做设计评审](cases/code/211-mcp-connector-for-carbon-design-reviews-from-inside-codex.md#中文) | wpv-chan | 未公开 | GitHub |
| 212 | [4.5 小时按 PRD 做语音助手](cases/code/212-voice-assistant-from-a-prd-in-4-5-hours-plus-bug-fixes.md#中文) | codeSTACKr | 未公开 | YouTube |

## 智能体、科研与写作

带视频浏览这一类:[https://apimodels.app/zh/gemini-4-carbon-prompts/research](https://apimodels.app/zh/gemini-4-carbon-prompts/research)

| # | 案例 | 作者 | 提示词 | 来源 |
| --- | --- | --- | --- | --- |
| 213 | [智能体集群为核聚变方程找到新精确解](cases/research/213-agent-teams-find-new-exact-solutions-for-fusion-equations.md#中文) | [@lucasjvds](https://x.com/lucasjvds) | 未公开 | X,24.8 万 浏览 |
| 214 | [Carbon 拆任务给本地模型并行完成](cases/research/214-carbon-splitting-a-scene-into-tasks-for-a-local-model.md#中文) | [@atomicagent_io](https://x.com/atomicagent_io) | 未公开 | X,1.3 万 浏览 |
| 215 | [在帆船模拟器里让模型比赛](cases/research/215-racing-language-models-in-a-sailing-simulator.md#中文) | [@shekitup](https://x.com/shekitup) | 未公开 | X,1.4 万 浏览 |
| 216 | [基于公开数据的 14 个垂直应用](cases/research/216-fourteen-vertical-data-apps-from-public-datasets.md#中文) | [@giyu_codes](https://x.com/giyu_codes) | 只有需求 | X,3.1 万 浏览 |
| 217 | [机械手完成 3 步方块转动](cases/research/217-three-cube-moves-performed-with-robot-hands.md#中文) | [@PhysAIAnalysis](https://x.com/PhysAIAnalysis) | 未公开 | X,499 浏览 |
| 218 | [五指机械手捏住果柄提起苹果](cases/research/218-five-finger-hand-picking-up-an-apple-by-its-stem.md#中文) | [@PhysAIAnalysis](https://x.com/PhysAIAnalysis) | 未公开 | X,746 浏览 |
| 219 | [把苹果越过墙放到盘子上](cases/research/219-moving-an-apple-over-a-wall-onto-a-plate.md#中文) | [@PhysAIAnalysis](https://x.com/PhysAIAnalysis) | 未公开 | X,499 浏览 |
| 220 | [让真机器人叠毛巾，暂未成功](cases/research/220-real-robot-told-to-fold-a-towel-without-success.md#中文) | [@sanatem](https://x.com/sanatem) | 完整提示词 | X,344 浏览 |
| 221 | [五种题材网文开篇实测](cases/research/221-five-web-novel-openings-across-five-genres.md#中文) | rbbbc | 未公开 | B 站 |
| 222 | [一道难数独，各解五次](cases/research/222-one-hard-sudoku-five-tries-each-carbon-vs-argon.md#中文) | Singularity Feed (GitHub gnana70) | 未公开 | YouTube |
| 223 | [审阅一份未完成的论文草稿](cases/research/223-reviewing-an-unfinished-paper-draft-against-other-top-models.md#中文) | 5555watch | 未公开 | Hacker News |

## 自己跑一个

在 apimodels.app 上用 OpenAI 兼容格式调 `gemini-4-carbon`。Carbon 开口前要想一阵,输出上限要调高、用流式、超时放长(命令见英文版)。也可以用原生 Gemini 格式:`POST https://api.apimodels.app/v1beta/models/gemini-4-carbon:generateContent`。Carbon 还能在哪用、为什么有时用不了、哪些参数要改,见 [Gemini 4 Carbon 怎么用](https://apimodels.app/zh/how-to-use-gemini-4-carbon)。

## 常见问题

### Gemini 4 Carbon 能自己做出 3D 场景、游戏或视频吗?

不能直接做出来。Carbon 输入文字、图片、视频、音频和 PDF,输出文字。这里每个场景、游戏和影片都是它写的代码渲染出来的:Three.js 和 WebGL 网页、Blender Python、CUDA 或 C++ 程序,声音用 Web Audio。在聊天窗口里你拿到的是代码或一个 HTML 文件;Antigravity、Cursor、GitHub Copilot 这类 agent 才能帮你运行、渲染和测试。

### 大家用的是什么工具?

大多是谷歌的 Antigravity,经常配合它的多 agent /swarm 模式;也有人用 Cursor、GitHub Copilot、AI Studio、Vertex AI,或者在自己的 agent 里调 API。作者说了用什么的,案例页里都写了。

### 做这类东西,Carbon 比 Claude Fable 5.2 强吗?

论质量通常不如,论花费常常更划算。这里的大多数同题对比里,Fable 5.2 做出来的更好看、更完整;Carbon 的花费只是零头,也有几次直接赢了。Carbon 还能看视频,好几位作者就是靠给它看参考视频。

### Carbon 比 Gemini 4 Argon 强吗?

大多数时候更强,代价是时间和 token。两者每 token 同价;这些测试里 Carbon 通常做得更好,用时则是 Argon 的好几倍。谷歌仍然推荐日常编程用 Argon。

### 做这些花了多少钱?

按作者自己公布的:一个 2,599 行的 3D 平台跳跃游戏一次生成 $0.45,射击游戏复刻 $3.82,4 轮自审约 $7.40,一次对比里三件活 $7.54,另一次三个长构建 $27.68。花费取决于思考档位和 agent 跑多久。

### 这些提示词能拿来用吗?

作品归原作者所有,每个案例都链回原帖或原页面。提示词带署名引用:短的全文、长的节选,没公开的不补写。商用前请先看原帖说明。

## 署名、版权与许可

- **作品归原作者所有。**本仓库不存放他们的视频、图片或代码,每个案例都链到原帖或原页面。
- **提示词署名并附链接。**400 字符以内的公开提示词全文收录;更长的只放节选并链到全文;没公开的不补写。
- 有些案例复刻或致敬了已有的游戏、影视、产品或地点,有些来自公司展示自家产品,案例备注里都写了;这些素材的权利归其所有者。
- **我们自己写的内容**(案例介绍、上面的总结和 `data/cases.json`)采用 [CC BY 4.0](LICENSE) 许可,转用请署名 apimodels.app 并附链接。
- 如果你是其中某个作品的作者,想撤下或更正署名,开一个 issue,我们会尽快处理。

通过 apimodels.app 调用 Gemini 4 Carbon:[模型页](https://apimodels.app/zh/models/gemini-4-carbon) · [怎么用](https://apimodels.app/zh/how-to-use-gemini-4-carbon) · [API 文档](https://apimodels.app/zh/docs/llm)
